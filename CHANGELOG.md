# Change Log
All notable changes to this project will be documented in this file, which follows the guidelines
on [Keep a CHANGELOG](http://keepachangelog.com/). This project adheres to
[Semantic Versioning](http://semver.org/).

## [Unreleased]

### Fixed
- Make JGitFlow's pushReleases a normal maven property so it can be overidden on the command line.
  This allows us to disable the pushReleases functionality in test environments
- Automatically add site descriptor if present in usual location
- Fixup default site descriptor so menus are generated correctly

### Changed
- Plugins updated to latest versions
- Minimum Maven version set to 3.3.9

### Removed
- liquibase.core.version was not used

## [v2.1.0]

### Changed
- Optional hook capability: fixup-versions, defaults to disabled.
  Used to fixate a property with the pom's version, used in inherited poms to import BOMs
  Normally only set in the release build. Requires xmlstarlet tool.
