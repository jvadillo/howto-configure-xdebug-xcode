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

### Step 2: Xdebug configuration
Add the following lines to your `php.ini`:
```
zend_extension = C:\xampp\php\ext\php_xdebug-3.1.5-8.1-vs16-x86_64.dll
xdebug.mode = debug
xdebug.start_with_request = yes
xdebug.discover_client_host 
```

### Step 2: VS Code configuration
You will need the [PHP Debug](https://marketplace.visualstudio.com/items?itemName=xdebug.php-debug) extension for VS Code. After installing it 

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
