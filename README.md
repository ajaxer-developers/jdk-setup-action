# jdk-setup-action

GitHub action to setup JAVA  
This GitHub Action installs a specified version of OpenJDK (from 8 to 22) on the runner.

## Inputs

- `version`: (Required) Java version to install. Must be between 8 and 22. Default is `17`.

### Notes:

- Java 8, 11, and 17 are installed via `apt-get`.
- For Java 18 and newer, the action downloads the JDK from the Temurin (AdoptOpenJDK) project.

## Usage

```yaml
steps:
  - name: Install Java
    uses: ajaxer-org/jdk-setup-action@v1
    with:
      version: '22' # Install Java 22, for example
