# JActions

![License](https://img.shields.io/github/license/jactions/maven-version)

Simple GitHub Action for getting Maven version.

## Usage

### Basic

Simply add the following to your workflow:

```yaml
steps:
- id: get-version
  uses: jactions/maven-version@v1
```

This will output version string accessible via `${{ steps.get-version.outputs.version }}`.

You can use any valid identifier instead of `get-version`.

### Customizing Maven POM path

By default, the action uses Maven's default POM file location.
This can be overridden via `pom` input
which is equivalent to providing `--file` parameter to Maven executable:

```yaml
steps:
- id: get-version
  uses: jactions/maven-version@v1
  with:
    pom: ./custom/path/to/pom.xml
```

### Customizing Maven Settings path

By default, the action used Maven's defaults for its settings file.
This can be overridden via `settings` input
which is equivalent to providing `--settings` parameter to Maven executable:

```yaml
steps:
- id: get-version
  uses: jactions/maven-version@v1
  with:
    settings: ./custom/path/to/settings.xml
```

## License

The project is licensed under [MIT license](LICENSE).
