# PHP CodeSniffer Configuration for MainWP Child

This repository includes a PHP_CodeSniffer (PHPCS) configuration file (`phpcs.xml`) that helps maintain consistent code style across the MainWP Child plugin codebase.

## Features

The PHPCS configuration includes rules for:

- **Equals Sign Alignment**: Ensures consistent spacing around equals signs in assignments
- **Indentation**: Uses 4 spaces for indentation (no tabs)
- **Yoda Conditions**: Enforces Yoda conditions for comparisons
- **Line Endings**: Ensures consistent line endings
- **Comment Punctuation**: Enforces proper punctuation in comments

## Usage

### Installing PHP_CodeSniffer

If you don't have PHP_CodeSniffer installed, you can install it globally using Composer:

```bash
composer global require squizlabs/php_codesniffer
```

Or locally in your project:

```bash
composer require --dev squizlabs/php_codesniffer
```

### Running PHPCS to Check Code Style

To check your code against the coding standards:

```bash
# Using global installation
phpcs --standard=phpcs.xml path/to/files

# Using local installation
vendor/bin/phpcs --standard=phpcs.xml path/to/files
```

### Running PHPCBF to Automatically Fix Issues

To automatically fix many coding standard violations:

```bash
# Using global installation
phpcbf --standard=phpcs.xml path/to/files

# Using local installation
vendor/bin/phpcbf --standard=phpcs.xml path/to/files
```

## Common Use Cases

### Fix Equals Sign Alignment Issues

One of the most common issues is equals sign alignment. To fix these issues across the codebase:

```bash
phpcbf --standard=phpcs.xml .
```

### Check a Specific File or Directory

```bash
phpcs --standard=phpcs.xml class/class-mainwp-child.php
phpcs --standard=phpcs.xml class/
```

## Integration with IDEs

Many IDEs support PHP_CodeSniffer integration, allowing you to see coding standard violations directly in your editor:

- **PhpStorm**: Go to Settings → PHP → Quality Tools → PHP_CodeSniffer and configure the path to phpcs. Then in Editor → Inspections, enable PHP → Quality Tools → PHP_CodeSniffer validation.
- **Visual Studio Code**: Install the "PHP Sniffer & Beautifier" extension.
- **Sublime Text**: Install the "SublimeLinter-phpcs" package.

## Contributing

When contributing to the MainWP Child plugin, please ensure your code follows these coding standards. Running PHPCBF before submitting a pull request can help catch and fix many common issues automatically.
