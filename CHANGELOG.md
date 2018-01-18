# Change Log
All notable changes to this project will be documented in this file, which follows the guidelines
on [Keep a CHANGELOG](http://keepachangelog.com/). This project adheres to
[Semantic Versioning](http://semver.org/).

## [Unreleased]

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
