# Change Log
All notable changes to this project will be documented in this file, which follows the guidelines
on [Keep a CHANGELOG](http://keepachangelog.com/). This project adheres to
[Semantic Versioning](http://semver.org/).

## [Unreleased]

## [11.0.5-FRAMEWORK-SNAPSHOT] - 2023-01-27
### Changed
- Update framework to 11.0.0

## [11.0.4-FRAMEWORK-SNAPSHOT] - 2022-05-24
### Changed
- Upgrade Liquibase version to 4.10.0

## [11.0.3-FRAMEWORK-SNAPSHOT] - 2022-02-25
### Changed
- Liquibase version downgraded to 3.5.3

## [11.0.2-FRAMEWORK-SNAPSHOT] - 2021-06-16
### Changed
- Add 'javaee-api.version' property of 8.0.1

## [11.0.0-FRAMEWORK-SNAPSHOT] - 2021-05-20
### Changed
- Updated to Jee 8.0
- Updated maven.enforcer.plugin to 3.0.0-M3
- Updated require-latest-versions-enforcer-rule.plugin to 11.0.0-M1

## [11.0.0] - 2021-05-01
### Changed
- Updated to Java 11
- Updated maven compiler to 3.8.0
- Updated maven surefire plugin to 2.22.2
- Updated maven jacoco plugin to 0.8.4

### Added
- Added `--illegal-access=permit` to maven surefire plugin
- Added `--illegal-access=permit` to maven failsafe plugin

### Changed
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
