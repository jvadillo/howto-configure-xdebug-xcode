# Step by step guide: how to configure Xdebug and VS Code

Foobar is a Python library for dealing with word pluralization.

## Requirements (Prerequisites)

Tools and packages required to successfully install this project:
- **Apache + PHP development environment**: You can use whatever you prefer: [XAMPP](https://www.apachefriends.org/download.html), Laragon, virtual machine (e.g. Homestead), Docker containers,...
- **Visual Studio Code**: you can install it downloading from the [official website](https://code.visualstudio.com/Download)


### Step 1: Xdebug installation
Download the appropiate DLL for your PHP version:
- **Windows**: You can easily do it using the [official wizard](https://xdebug.org/wizard)
- **Linux, macOSX and others**: follow the instructions of the [official website](https://xdebug.org/docs/install).

After downloading it, move the downloaded file to the /ext folder. This is the folder where PHP keeps all of its extensions and can be found under the folder where you have installed PHP.

### Step 2: Xdebug configuration
Note: MacOSX users must follow the guidelines from the official site.
Configure PHP to use Xdebug by adding the following lines to your `php.ini`:

```
zend_extension=path/to/xdebug to your php.ini
```

Then enable remote debugging by adding the following lines to the `php.ini` file:

```
xdebug.mode = debug
xdebug.start_with_request = yes
xdebug.discover_client_host 
```
An example of the final result could be the following (for Windows):

```
zend_extension = C:\xampp\php\ext\php_xdebug-3.1.5-8.1-vs16-x86_64.dll
xdebug.mode = debug
xdebug.start_with_request = yes
xdebug.discover_client_host 
```
Restart your server in order to reload the settings. You can verify that everything is OK  by checking your phpinfo() output for an Xdebug section.

### Step 3: VS Code configuration
You will need the [PHP Debug](https://marketplace.visualstudio.com/items?itemName=xdebug.php-debug) extension for VS Code. After installing it go to the Debug section, choose PHP and click the button for creating the default configuration file.



## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
