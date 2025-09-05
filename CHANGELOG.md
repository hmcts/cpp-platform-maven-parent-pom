# Change Log
All notable changes to this project will be documented in this file, which follows the guidelines
on [Keep a CHANGELOG](http://keepachangelog.com/). This project adheres to
[Semantic Versioning](http://semver.org/).

## [Unreleased]
### Changed
- Remove distribution management from pom.xml and prepare for public repo migration

## [17.10.11] - 2024-10-21
### Changed
- service parent pom enforcer rule now checks for latest major and minor versions and ignores patch version

## [17.10.10] - 2024-08-02
### Added
- Provide capability to configure jgitflow develop branch name through 'jgitflow.maven.developBranchName' property

## [17.10.9] - 2024-07-16
### Added
- Add enforcer rules to verify core domain and service parent pom are on latest release version

## [17.10.8] - 2024-07-01
### Added
- Moved camunda version and its associated plugin dependencies here, so they can be seen by plugin dependency management
  - cpp.camunda.version: 7.17.0
  - org.mapstruct.version: 1.5.5.Final
  - lombok.mapstruct.binding.version: 0.2.0
  - org.projectlombok.version: 1.18.26

## [17.10.7] - 2024-06-20
- Remove duplicate jgitflow maven property

## [17.10.6] - 2024-06-20
- Remove duplicate jgitflow maven plugin

## [17.10.5] - 2024-06-20
- Add sonar-maven-plugin to lock version

## [17.10.4] - 2024-06-17
- Add jgitflow maven plugin

## [17.10.3] - 2023-08-02
- Update surefire and failsafe plugin versions to 3.1.2 (junit5)

## [17.10.1] - 2023-07-06
### Changed
- Remove command line arguments from surefire plugin in order to fix jacoco coverage generation issue

## [17.0.0] - 2023-05-23
### Changed
- Update to Java 17
- Update to Jee 8.0
- Update maven compiler to 3.8.0
- Force maven to use Java 17+ compiler
- Upgrade Liquibase version to 4.10.0
- Update plugins.jaxb2.version to 0.15.2
- Update maven.enforcer.plugin to 3.0.0-M3
- Update require-latest-versions-enforcer-rule.plugin to 17.0.0
- Update maven surefire plugin to 2.22.2
- Update maven jacoco plugin to 0.8.4
### Added
- Added `--illegal-access=permit` to maven surefire plugin
- Added `--illegal-access=permit` to maven failsafe plugin
- Add 'javaee-api.version' property of 8.0.1

## [8.0.1] - 2021-10-11
### Changed
- Downgrade liquibase to 3.5.3 to match the version in the framework

## [8.0.0] - 2021-10-05
### Changed
- Update to framework 8.0.0 as the final Java 8 version of the framework
- Bump version to 8 to match framework 8 version   
- Update maven-super-pom to 2.0.0

## [2.5.7] - 2019-06-24
### Changed
- Update plugins.require-latest-versions-enforcer-rule.version to version 1.2.0, to fix enforcer not checking all framework plugins issue

## [2.5.6] - 2018-06-20
### Changed
- Reverted:
    maven-enforcer-plugin: 3.0.0-M2 -> 3.0.0-M1
  due to failure to process parent-pom plugins

## [2.5.5] - 2018-06-19
### Changed
- Liquibase updated to latest version:
    liquibase-core: 3.5.2 -> 3.6.1
    liquibase-maven-plugin: 3.5.3 -> 3.6.1

- Plugins updated to latest version:
    maven-javadoc-plugin: 3.0.0 -> 3.0.1
    maven-surefire-plugin: 2.21.0 -> 2.22.0
    maven-failsafe-plugin: 2.21.0 -> 2.22.0
    maven-wagon-plugin: 3.0.0 -> 3.1.0
    dependency-check-maven-plugin: 3.1.2 -> 3.2.1
    maven-scm-plugin: 1.9.5 -> 1.10.0
    maven-war-plugin: 3.2.0 -> 3.2.2
    maven-enforcer-plugin: 3.0.0-M1 -> 3.0.0-M2
    maven-dependency-plugin: 3.1.0 -> 3.1.1
    jaxb2-maven-plugin: 0.13.3 -> 0.14.0
    maven-resources-plugin: 3.0.2 -> 3.1.0
    maven-site-plugin: 3.7 -> 3.7.1
    pitest-maven-plugin: 1.3.2 -> 1.4.0

## [2.5.4] - 2018-04-18

### Added
- GPG Signature capability (maven-gpg-plugin, pgp-maven-plugin)
- JAR Signature capabiilty (maven-jarsigner-plugin)

### Changed
- Plugins updated to latest versions
    maven-clean-plugin: 3.0.0 -> 3.1.0
    maven-dependency-version: 3.0.2 -> 3.1.0
    maven-jar-plugin: 3.0.2 -> 3.1.0
    maven-shade-plugin: 3.1.0 -> 3.1.1
    maven-surefire-plugin / maven-failsafe-plugin:  2.20.1 -> 2.21.0
    dependency-check-maven plugin: 3.1.0 -> 3.1.2
    jacoco-maven-plugin: 0.8.0 -> 0.8.1
    pitest-maven-plugin: 1.3.1 -> 1.3.2

## [2.5.3] - 2018-04-18 [YANKED]

### Changed
- testing GPG signing process

## [2.5.2] - 2018-04-18 [YANKED]

### Changed
- testing GPG signing process

## [2.5.1] - 2018-04-18 [YANKED]

### Changed
- testing GPG signing process

## [2.5.0] - 2018-04-18 [YANKED]

### Changed
- testing GPG signing process

## [2.4.1] - 2018-01-22

### Fixed
- Reinstated liquibase.core.version property

## [2.4.0] - 2018-01-18

### Fixed
- Make JGitFlow's pushReleases a normal maven property so it can be overidden on the command line.
  This allows us to disable the pushReleases functionality in test environments
- Automatically add site descriptor if present in usual location
- Fixup default site descriptor so menus are generated correctly

### Changed
- Minimum Maven version set to 3.3.9
- Plugins updated to latest versions
    maven-site-plugin: 3.6 -> 3.7
    maven-wagon-plugin: 2.12 -> 3.0.0 (used to upload site)
    maven-war-plugin 3.1.0 -> 3.2.0 (bug fix)
    maven-versions-plugin: 2.4 -> 2.5
    maven-javadoc-plugin: 3.0.0-M1 -> 3.0.0
    pitest-maven plugin: 1.2.4 -> 1.3.1
    wildfly-maven-plugin: 1.2.0.Final -> 1.2.1.Final
    org.jvnet.jaxb2.maven2:maven-jaxb2-plugin: 0.13.2 -> 0.13.3
    dependency-check-maven: 2.1.1 -> 3.0.2 (this brings it in line with existing implementation)

### Removed
- liquibase.core.version was not used

## [v2.1.0]

### Changed
- Optional hook capability: fixup-versions, defaults to disabled.
  Used to fixate a property with the pom's version, used in inherited poms to import BOMs
  Normally only set in the release build. Requires xmlstarlet tool.
