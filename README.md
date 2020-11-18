# Framgia PHP Standards Checker by PHP CodeSniffer

## About
- **[PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)** is a set of two PHP scripts; the main phpcs script that tokenizes PHP, JavaScript and CSS files to detect violations of a defined coding standard, and a second phpcbf script to automatically correct coding standard violations. **[PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)** is an essential development tool that ensures your code remains clean and consistent.
- **[Framgia PHP Standard](https://github.com/framgia/coding-standards/blob/master/eng/README.md#php)** is a set of coding conventions used by PHP team in [Framgia Vietnam](http://framgia.vn/). It is based on the [PSR-2 Coding Style Guide](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md) with some additional rules.
- This is the Coding Standard package for Code Sniffer to check whether your codes satisfy the Framgia Standard or not.
- **New**: This standard is compatible with both PHP CodeSniffer version 2 and 3. If you are using PHP CodeSniffer 2, please use the codes in `0.2` branch. If you are using PHP CodeSniffer 3, use the codes in `master` branch.

## Install
### Install locally
You can install in each project folder:
```
composer require --dev dealerdirect/phpcodesniffer-composer-installer
composer require --dev wataridori/framgia-php-codesniffer
```

`phpcs` command will be installed to folder `vendor/bin`.

Now you can check and run phpcs:
```
./vendor/bin/phpcs -i
```
```
./vendor/bin/phpcs --standard=Framgia /path/to/your/code
```

### Install globally
- Install `PHP_CodeSniffer` globally by `composer`. Make sure you have `~/.composer/vendor/bin/` in your `PATH`.
```
composer global require "squizlabs/php_codesniffer=*"
```
- Move to **Standards** folder and clone this repository
```
// Version 2
cd ~/.composer/vendor/squizlabs/php_codesniffer/CodeSniffer/Standards
git clone -b 0.2 git@github.com:wataridori/framgia-php-codesniffer.git Framgia

// Version 3
cd ~/.composer/vendor/squizlabs/php_codesniffer/src/Standards
git clone git@github.com:wataridori/framgia-php-codesniffer.git Framgia
```
- Check whether the Framgia Standard has been installed succesfully or not
```
phpcs -i
```
- Check your code using Framgia Standard
```
phpcs --standard=Framgia /path/to/your/code
```
- If you do not want to install this package inside **CodeSniffer Standards** folder, you can clone it to everywhere you want and specify the installed folder when you run `phpcs` command.
```
phpcs --standard=/path/to/your/framgia-php-codesniffer /path/to/your/code
```
- It's a pity that the default encoding used by PHP_CodeSniffer is ISO-8859-1. **Yes, it is not UTF-8**.
Therefore, you will have some problems with the words counter if you use Japanese in your codes.
You'd better change the default encoding to `UTF-8`.
```
phpcs --config-set encoding utf-8
```
Or set the encoding to `UTF-8` when running the command.
```
phpcs --standard=Framgia /path/to/your/code --encoding=utf-8
```
