# Changes in 1.2.1 #

## Bug fixes ##

The following issues logged against Antennae have been fixed:

**Issue [7](http://code.google.com/p/antennae/issues/detail?id=7): Test AIR Apps**

**Issue [8](http://code.google.com/p/antennae/issues/detail?id=8): Building Antennae error**

## New Files ##

**lib/RunAirTests**
> Application shell and descriptor used to create an AIR based
> FlexUnit application.

**templates/SampleAIRTestApplication/`**`**
> Template project for running AIR based FlexUnit tests.

## Updated Files ##

**lib/arc-flexunit.swc and src/arc-flexunit/`**`**
> Facility added to call a function at the conclusion of all unit
> tests. Added to support exiting from an AIR based FlexUnit
> application.

**lib/build-assets.xml**
> Includes references to template files for creating AIR based
> FlexUnit applications.

**tools/build-common-targets.xml**
> Added new targets to support AIR based FlexUnit applications.

**tools/build-common-tasks.xml**
> Updated to allow library paths to include spaces.

## New Targets (tools/build-common-targets.xml) ##

**air-test-application-stage**
> Stages an AIR based FlexUnit application for running. This is the
> test version of the air-application-stage target.

**air-test-application**
> Compiles an AIR based FlexUnit application. This automatically
> creates the TestSuite that the application will use. This is the
> AIR version of the flex-test-application target.

**flex-test-app**
> Creates the application MXML for a Flex based FlexUnit
> application. Tasks in this target were removed from
> create-test-suite in order to support AIR based FlexUnit
> applications. Called by the existing flex-test-application target.

**air-test-app**
> Creates the application MXML and application descriptor for an AIR
> based FlexUnit application.  Called by the new
> air-test-application target.

**test-air-flexunit**
> Runs an AIR based FlexUnit application, assumes application has
> already been built.

## New Properties (lib/build-assets.xml) ##

**arc-air-flexunit.mxml**
> Template file used to create an AIR based FlexUnit application.

> Default: ${lib.assets.dir}/RunAirTests.mxml

**arc-air-flexunit-app.xml**
> Template file used to create the AIR descriptor for a FlexUnit
> application.

> Default: ${lib.assets.dir}/RunAirTests-app.xml