<h1>My notes while learning PHP.</h1>

These are my notes while learning PHP. Based on [Laracast The PHP Practitioner Series](https://laracasts.com/series/php-for-beginners/).

# The PHP Practitioner

My notes while learning PHP with [Laracast PHP for beginners](https://laracasts.com/series/php-for-beginners/)

**Step 1: Install PHP**

Mac OS X

macOS Catalina comes with PHP 7.3 pre installed. You can find default PHP config in /etc/php.ini.default.

You can install PHP 7.4 with Homebrew.

_PHP 5.6, PHP 7.0, and PHP 7.1 have been deprecated because they are out of support. While they are not recommended for production, there are legitimate reasons to have them installed in a development environment for testing and legacy support._

First we need to install Xcode Command Line Tools:

In terminal run

```bash
xcode-select --install
```

Install Homebrew:

In terminal run

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Install PHP:

```bash
brew install php@7.4
```

If you want to install complete development environment with Apache, MySQL and different versions of PHP you can find great step by step instructions on [GRAV blog](https://getgrav.org/blog/macos-catalina-apache-multiple-php-versions)

Windows

You can download latest PHP installer from [php.net](https://www.php.net/downloads.php).

For complete development environment the [XAMPP](https://www.apachefriends.org/index.html) is popular option.

For manual PHP install you might follow [DEVDOJO guide](https://devdojo.com/tutorials/installing-php-on-windows)

Linux

Linux is great choice for PHP development and comes pre installed with PHP but you should check PHP version in distribution of your choice and upgrade to supported version.

**Step 2: Install code editor**

There are many great options here for all major operating systems:

[VS Code](https://code.visualstudio.com/)

[Sublime Text 3](https://www.sublimetext.com/)

[Atom](https://atom.io/)

or full IDE like

[PhpStorm](https://www.jetbrains.com/phpstorm/)

**Step 3: Variables**

To get help about php command line options:

```bash
php -h


```

Run local php server with:

```bash
php -S localhost:8888
```

where :8888 is port and can be any number.

To interpret code as php start with:

```php
<?php
```

If the file contains only php code you should not close the opening php tag.

If the php code is part of html code you should end code with closing tag:

```php+HTML
<h1>Example</h1>
<?php
  echo 'Hello, World!';
?>
```
