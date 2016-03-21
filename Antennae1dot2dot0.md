# Changes in 1.2.0 #

**New version numbering**

Antennae versions are now being released with a more traditional version numbering system of #.#.# which translates to major.minor.patch.

**Bug fixes**

The following issues logged against Antennae have been fixed:

**Issue [2](http://code.google.com/p/antennae/issues/detail?id=2): Flex targets should be prefixed flex- instead of flex2-**

**Issue [4](http://code.google.com/p/antennae/issues/detail?id=4): adt certificate usage syntax**

**Property and target renaming**

Antennae grew out of the build process used at Allurent.  As such it inherited some naming conventions that are not found outside of Allurent. To better align Antennae with standard naming conventions many properties and targets have been renamed.

To minimize the impact on existing projects a backwards compatibility mode has been introduced. It is off by default. Antennae users are encouraged to update their projects to use the new naming conventions. Until those updates are completed the backwards compatibility mode will provide a stop-gap measure. Given the variability of situations that Antennae can be used in and the high degree to which it can be customized, the backwards compatibility mechanism has been designed to address the most common situations.

The following name changes occurred:

  * All properties and targets that used flex2 in their name have been renamed to flex.

  * All properties, targets, package names, and files that used flexunit2 in their name have been renamed to flexunit.

  * All properties, package names, and files that used arc-flexunit2 in their name have been renamed to arc-flexunit.

  * All properties and targets that used as3doc in their name have been renamed to asdoc.

  * The default of build.dir changed from build to bin.

  * The default of src.flex.dir changed from flex2 to src.

  * The default of src.java.dir changed from java to src.

  * The default of arc-flexunit.filters changed from flexunit2.filters to arc-flexunit.filters.

  * If you have code that references ARCTestRunner or AllTestsFileGenerator, it will need to be updated to reflect the new package name.

Full details of the backwards compatibility mechanism and the renaming changes are detailed below.

**Behavior changes**

The flex.dir property is no longer defaulted in build-common-properties.xml. This property is designed to be set in build-user.properties.

A property named air.certificate.type has been added with a default value of pkcs12. This property is used by AIR when creating a signed .air file.

# New Files #

**tools/compat-build.xml**
> This provides a single file that can be imported to trigger the
> backwards compatibility settings. Notes on including this file can
> be found in tools/build-common-imports.xml.

# Updated Files #

**build-user.properties.mac**
> Updated to new property naming convention.

**build-user.properties.win**
> Updated to new property naming convention.

**lib/build-assets.xml**
> Properties and filenames updated to new naming convention.

**tools/build-common-imports.xml**
> Added facility to enable backwards compatibility mode. It is off
> by default.

**tools/build-common-properties.xml**
> Updated to new property naming convention. List of changes below.

**tools/build-common-targets.xml**
> Updated to new target naming convention and use new property
> naming convention. List of changes below.

**tools/build-common-tasks.xml**
> Updated to new task naming convention and use new property naming
> convention. List of changes below.

**tutorial/`**` and templates/`**`**
> All files have been updated to use the new naming convention.  Any
> notable changes are listed below.

**templates/SampleAIRApplication/src/SampleAIRApplication-app.xml**
> Updated to AIR 1.0 descriptor format.

**src/`**`**
> Updated directories to new naming convention.

# Properties Renamed #

In file lib/build-assets.xml:

|Old Name|New Name|
|:-------|:-------|
|flexunit2.swc|flexunit.swc|
|arc-flexunit2.jar | arc-flexunit.jar|
|arc-flexunit2.swc | arc-flexunit.swc|
|arc-flexunit2.mxml | arc-flexunit.mxml|


In file tools/build-common-properties.xml:

|Old Name|New Name|
|:-------|:-------|
|project.flex2.application | project.flex.application|
|flex2.dir | flex.dir|
|flex2.frameworks.dir | flex.frameworks.dir|
|flex2.config | flex.config|
|flex2.dist.lib | flex.dist.lib|
|flex2.compc.jar | flex.compc.jar|
|flex2.mxmlc.jar | flex.mxmlc.jar|
|flex2.mxmlc.options | flex.mxmlc.options|
|flex2.compc.options | flex.compc.options|
|src.flex2.dir | src.flex.dir|
|flex2.standalone.player | flex.standalone.player|
|as3doc.template.dir | asdoc.template.dir|
|as3doc.jar | asdoc.jar|
|as3doc.xalan.jar | asdoc.xalan.jar|
|build.as3doc.dir | build.asdoc.dir|
|arc-flexunit2.loglevel | arc-flexunit.loglevel|
|arc-flexunit2.class | arc-flexunit.class|
|arc-flexunit2.alltests.suite | arc-flexunit.alltests.suite|
|arc-flexunit2.reportserver.port | arc-flexunit.reportserver.port|
|arc-flexunit2.reportserver.host | arc-flexunit.reportserver.host|
|arc-flexunit2.timeout | arc-flexunit.timeout|
|arc-flexunit2.filters | arc-flexunit.filters|



# Targets Renamed #

In file tools/build-common-targets.xml:

|Old Name|New Name|
|:-------|:-------|
|flex2-application | flex-application|
|flex2-application-copy | flex-application-copy|
|flex2-application-check | flex-application-check|
|flex2-library | flex-library|
|flex2-library-check | flex-library-check|
|as3doc  | asdoc  |
|as3doc-check | asdoc-check|
|flex2-test-application | flex-test-application|
|test-flexunit2 | test-flexunit|
|test-flexunit2-os | test-flexunit-os|
|test-flexunit2-mac | test-flexunit-mac|
|test-flexunit2-notmac | test-flexunit-notmac|
|test-flexunit2-failure | test-flexunit-failure|



# Tasks Renamed #

In file tools/build-common-tasks.xml:

|Old Name|New Name|
|:-------|:-------|
|as3doc  | asdoc  |



# Files Renamed #

|Old Name|New Name|
|:-------|:-------|
|lib/arc-flexunit2.jar | lib/arc-flexunit.jar|
|lib/arc-flexunit2.swc | lib/arc-flexunit.swc|
|lib/flexunit2.swc | lib/flexunit.swc|


# Directories Renamed #

|Old Name|New Name|
|:-------|:-------|
|src/arc-flexunit2 | src/arc-flexunit|
|src/arc-flexunit2/flex2 | src/arc-flexunit/flex|
|src/arc-flexunit2/flex2/com/allurent/flexunit2 | src/arc-flexunit/flex/com/allurent/flexunit|
|src/arc-flexunit2/java/com/allurent/flexunit2 | src/arc-flexunit/java/com/allurent/flexunit|
|templates/`**`/flex2 | templates/`**`/src|
|tutorial/`**`/flex2 | tutorial/`**`/src|