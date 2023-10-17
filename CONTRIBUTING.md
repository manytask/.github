# Contributing to `manytask` 

First and foremost, thank you for considering contributing to `manytask`! 😍  
We appreciate your time and expertise, and we are excited to collaborate with you.  
This document outlines the process and guidelines for contributing to our project.


## Styleguide

This part of the document describes the styleguides we use in our project. We kindly ask you to follow them when creating merge requests.

### Python styleguide

We use [PEP 8](https://www.python.org/dev/peps/pep-0008/) as a base for our styleguide.  
However, we have some additional rules:
* Line length should not exceed 100 characters with a hard limit of 120.
* All code should be typed.
* All code should be formatted with [black](https://pypi.org/project/black/).
* All imports should be sorted with [isort](https://pypi.org/project/isort/) using `black` profile.


### Commit Messages

We use [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/) for our commit messages and PR titles.  
It requires to follow some rules to make commit messages more readable and informative, indicate the type of changes, and automate the release process.

In short, the rules are (check the link above for more details):
* Use the present tense ("Add feature" not "Added feature")
* Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
* Limit the first line to 72 characters or fewer
* Reference issues and pull requests in commit body
* When only changing documentation, include `[ci skip]` tag in the commit title
* Start the commit message with an applicable tag:
    * `fix` - small bug fix
    * `docs` - docs changes 
    * `feat` - a new feature 
    * `chore` - changes that do not relate to a fix or feature and don't modify src or test files (for example updating dependencies) 
    * `refactor` - code refactor that neither fixes a bug nor adds a feature
    * `style` - changes that do not affect the meaning of the code
    * `perf` - changes that improve performance
    * `test` - including new or correcting previous tests
    * `ci` - continuous integration related
    * `revert` - revert commits and PR

For example  

Good:
* `feat: create new api endpoint for student scores reporting`
* `perf: improve performance with lazy load implementation for images`
* `chore: update flask dependency to 2.1 version`

Bad:
* `some fixes`
* `oops`
* `fixed bug on landing page`
* `style changes and update`

Additionally, scope can be added to the commit message in format `<tag>(<scope>): <description>`.  
For example, `feat(api): add new endpoint for student scores reporting`.


### Versioning

We use [Semantic Versioning 2.0.0](https://semver.org/) for our releases.
It means that each release should have a version number in the following format: `MAJOR.MINOR.PATCH`.

* `MAJOR` version when you make incompatible API changes,
* `MINOR` version when you add functionality in a backwards compatible manner, and
* `PATCH` version when you make backwards compatible bug fixes.

Additional labels for pre-release and build metadata are available as extensions in `MAJOR.MINOR.PATCH-LABEL+METADATA` format.

For example

* `1.0.0` - initial release
* `1.1.0` - new feature
* `1.1.1` - bug fix
* `2.0.0-alpha` - alpha release
* `2.0.0-rc.1` - release candidate with number
* `2.0.0-rc.1+build.1` - release candidate with build metadata
* `2.0.0` - stable release


Note: Is “v1.2.3” a semantic version? No, it is not.

