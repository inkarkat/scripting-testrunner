# Scripting Testrunner

_Runs automated tests for some common scripting language test frameworks._

Supported languages / test frameworks:

* Bash / [bats](https://github.com/bats-core/bats-core) - Bash Automated Testing System
* Python 3 / [unittest](https://docs.python.org/dev/library/unittest.html)
* Perl / `prove`

The action assumes that the scripts-under-test are located in the `./bin` subdirectory, and tests for each component are in `./tests/<component>` directories.

# Usage

```yaml
- name: Checkout repo
  uses: actions/checkout@v4
- name: Run tests
  uses: inkarkat/scripting-testrunner@master
  with:
    include-optional-dependencies: false
    submodules: false
```
The project's `README.md` has dependencies listed like this:
```markdown
### Dependencies
* [inkarkat/shell-basics](https://github.com/inkarkat/shell-basics)
* [inkarkat/shell-tools](https://github.com/inkarkat/shell-tools) (optional)
```
