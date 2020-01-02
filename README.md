# The PHP Practitioner

My notes while learning PHP with [Laracast PHP for beginners](https://laracasts.com/series/php-for-beginners/)

**Step 1: Install PHP**

Mac OS X

macOS Catalina comes with PHP 7.3 preinstalled. You can find default PHP config in /etc/php.ini.default.

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

Linux is great choice for PHP development and comes preinstalled with PHP but you should check PHP version in distribution of your choice and upgrade to supported version.

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

To declare variable use \$ sign followed by name of variable:

```php
$name = "John";
$age = 50;
```

- A variable name must start with letter or underscore character
- A variable name cannot start with number
- A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and \_)
- Variable names are case-sensitive
- Use camelCase or underscore_case notation for naming a variable. Pick one and stick with it.

Using single quotes or literal string:

```php
$name = 'John';
```

When using single quotes you cannot concatenate variable inside single quotes. Will not parse special characters.

When using double quotes string you can concatenate variable inside double quotes. It will also parse special characters.

Use {\$var} around variable name for better readability.

```php
echo 'Hello,' . $name; //concatenate single quotes string and variabble
echo "Hello, $name"; //concatenate double quotes string and variable
echo "Hello, {$name}"; //use {} around variable for better readability
echo "{$greeting}, {$name}"; //nesting variables in sting. Must use double quotes
```

**Step 4: PHP and HTML**

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

Get value from url as key pair array:

URL: localhost:8888/?name=John

everything after ? sign is a parameter or key value pair in this case name is a key and John is a value.

```php+HTML
<header>
	<h1>
  	<?php
  		$name = $_get['name'];
  		echo "Hello, $name";
  	?>
	</h1>
</header>
```

or the same thing with concatenation:

```php+HTML
<h1>
  <?php echo "Hello, " . $_GET['name']; ?>
</h1>
```

One shorthand to remember:

Instead of

```php
<?php echo $greeting; ?>
```

we can use:

```php
<?= $greeting; ?>
```

This shorthand is a common use in template files.

To include code from another file we can use:

```php
require 'index.view.php';
```

or

```php
include 'index.view.php';
```

The difference is that require will throw fatal error if file is not found and include will give you only warning.