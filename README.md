# PHP coding standard

Combines [EasyCodingStandard](https://github.com/Symplify/EasyCodingStandard) + [GrumPHP](https://github.com/phpro/grumphp) + custom rules to provide static analysis to your project.

## Install

```bash
composer require --dev jbieliauskas/php-standard
```

## Usage

Create `grumphp.yml` file in the root directory of your project and add:

```YAML
parameters:
  tasks:
    ecs:
      config: 'vendor/jbieliauskas/php-standard/ecs.yml'
      whitelist_patterns: ['.']
```

Notes:
- the `config` property points to the ruleset of 
this package.
- the `whitelist_patterns` is a list of directories that should be tested. Only `.php` files in those directories will be tested.

And that is it. GrumPHP won't allow to commit code that doesn't meet the standard.

## Further reading

- To bypass commit sniffing, see [here](https://github.com/phpro/grumphp/blob/master/doc/faq.md#how-can-i-bypass-grumphp).

- To run grumphp manually, see [here](https://github.com/phpro/grumphp/blob/master/doc/commands.md#run).

## Contributing

To add or remove rules, first [submit an issue](https://github.com/digitronas/akeneo-coding-standard/issues) to make sure your ideas aren't already in development and to make sure the project would approve your changes.

Clone this repository and run `composer install`. This will install ecs and grumphp. You might have to [bypass grumphp](https://github.com/phpro/grumphp/blob/master/doc/faq.md#how-can-i-bypass-grumphp), since it might not allow you to commit code if there are files that don't meet the standard.

Create a pull request to `master` branch. The changes will be merged after they pass code review.
