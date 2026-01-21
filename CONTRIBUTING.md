# Contributing

Contributions are welcome and will be fully credited.

## Pull Requests

- **[PSR-12 Coding Standard](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-12-extended-coding-style-guide.md)** - The easiest way to apply the conventions is to run `composer cs-fix`.
- **Add tests!** - Your patch won't be accepted if it doesn't have tests.
- **Document any change in behaviour** - Make sure the `README.md` and any other relevant documentation are kept up-to-date.
- **Create feature branches** - Don't ask us to pull from your master branch.
- **One pull request per feature** - If you want to do more than one thing, send multiple pull requests.
- **Send coherent history** - Make sure each individual commit in your pull request is meaningful.

## Regenerating the SDK

This SDK is auto-generated from the OpenAPI specification. To regenerate:

1. Update the `laravel-forge-openapi.yaml` file
2. Run the generator:

```bash
openapi-generator-cli generate \
  -i laravel-forge-openapi.yaml \
  -g php \
  -o . \
  --additional-properties=invokerPackage=Dimer\\ForgeSDK
```

3. Review and test the changes
4. Submit a pull request

## Running Tests

```bash
composer test
```

## Running Static Analysis

```bash
composer analyse
```

## Fixing Code Style

```bash
composer cs-fix
```

**Happy coding!**
