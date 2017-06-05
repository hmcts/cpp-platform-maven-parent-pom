# Change Log
All notable changes to this project will be documented in this file, which follows the guidelines
on [Keep a CHANGELOG](http://keepachangelog.com/). This project adheres to
[Semantic Versioning](http://semver.org/).

## [Unreleased]

### Changed
- Optional hook capability: fixup-versions, defaults to disabled.
  Used to fixate a property with the pom's version, used in inherited poms to import BOMs
  Normally only set in the release build. Requires xmlstarlet tool.
