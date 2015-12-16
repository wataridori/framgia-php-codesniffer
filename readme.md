# Framgia PHP Standards Checker by PHP CodeSniffer

## About
- **[PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)** is a set of two PHP scripts; the main phpcs script that tokenizes PHP, JavaScript and CSS files to detect violations of a defined coding standard, and a second phpcbf script to automatically correct coding standard violations. **[PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)** is an essential development tool that ensures your code remains clean and consistent.
- **[Framgia PHP Standard](https://github.com/framgia/coding-standards/blob/master/eng/README.md#php)** is a set of coding conventions used by PHP team in [Framgia Vietnam](http://framgia.vn/). It is based on the [PSR-2 Coding Style Guide](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md) with some additional rules.
- This is the Coding Standard package for Code Sniffer to check whether your codes satisfy the Framgia Standard or not.

## Install
- Install `PHP_CodeSniffer` globally by `composer`. Make sure you have `~/.composer/vendor/bin/` in your `PATH`.
```
composer global require "squizlabs/php_codesniffer=*"
```
- Move to **Standards** folder and clone this repository
```
cd ~/.composer/vendor/squizlabs/php_codesniffer/CodeSniffer/Standards
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
