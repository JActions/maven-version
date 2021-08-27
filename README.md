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

### Customizing Maven path

By default, the action uses `./pom.xml` as path to your Maven configuration (`-f` flag of Maven). This can be overridden via `pom` input:

```yaml
steps:
- id: get-version
  uses: jactions/maven-version@v1
  with:
    pom: ./custom/path/to/pom.xml
```

## License

The project is licensed under [MIT license](LICENSE).
