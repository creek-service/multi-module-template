<!-- ChangeMe: replace /template in the badge urls below with the name of the repo-->
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![build](https://github.com/creek-service/template/actions/workflows/gradle.yml/badge.svg)](https://github.com/creek-service/template/actions/workflows/gradle.yml)
[![Coverage Status](https://coveralls.io/repos/github/creek-service/template/badge.svg?branch=main)](https://coveralls.io/github/creek-service/template?branch=main)

# Template Repo
Template repo used to create others

## Features

The template sets up the following:

* Multi-module Gradle Java project, including:
  * [Spotless][1] (code formatting)
  * [Spotbugs][2] (static code analysis)
  * [Checkstyle][3] (static code analysis)
  * [Axion-release][4] (release versioning)
  * [Jacoco][5] (code coverage analysis)
  * [Coveralls.io][6] (code coverage tracking)
  * Default set of test dependencies:
    * [Unit5][7]
    * [Mockito][8]
    * [Hamcrest][9]
    * [Guava TestLib][10]
    * [Log4J 2.x][11]
* Github build workflow, including:
  * Gradle build
  * [Coveralls.io][6] reporting
  * Release versioning
* Github code owners and PR template.

## Usage

### Creating a new repo from the template

1. Click the "Use this template" button on the main page and provide a name
2. Import the new repo into Coveralls.io and grab the `COVERALLS_REPO_TOKEN`,
   setting this as a secret on the new repo.
3. Customise the files in the new repo:
   1. Replace the `template` repo name with the name of the new project.
      Each place is marked with a `ChangeMe` comment. 
   2. Replace the [`example`](example) module with the repos first module.
   3. Replace this README.md
   4. Commit changes as a PR (so you can test the PR build works!)
4. Configure the main branch for the new repo:
   1. `build` and `coverage/coveralls` status checks are required before a PR can be merged.
   2. `Require approvals` is ticked.

<< TODO:  Add steps to configure the new repo in Github....>>

### Gradle commands

* `./gradlew format` will format the code using [Spotless][1].
* `./gradlew static` will run static code analysis, i.e. [Spotbugs][2] and [Checkstyle][3].
* `./gradlew check` will run all checks and tests.
* `./gradlew coverage` will generate a cross-module [Jacoco][5] coverage report.

[1]: https://github.com/diffplug/spotless
[2]: https://spotbugs.github.io/
[3]: https://checkstyle.sourceforge.io/
[4]: https://github.com/allegro/axion-release-plugin
[5]: https://www.jacoco.org/jacoco/trunk/doc/
[6]: https://coveralls.io/
[7]: https://junit.org/junit5/docs/current/user-guide/
[8]: https://site.mockito.org/
[9]: http://hamcrest.org/JavaHamcrest/index
[10]: https://github.com/google/guava/tree/master/guava-testlib
[11]: https://logging.apache.org/log4j/2.x/