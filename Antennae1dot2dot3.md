# Changes in 1.2.3 #

## Bug fixes ##

The following issues logged against Antennae have been fixed:

**Issue [10](http://code.google.com/p/antennae/issues/detail?id=10): Sometimes ARC Report Server exits with error before reporting Test Results**

## Behavior changes ##

A new command line property has been added to AllTestsFileGenerator to control if the AlwaysFail test should be included if a filters file is in use. This behavior can be controlled through the use of a new property described below.

## New Files ##

**src/build-imports.xml**
> Import file to allow building projects under src/

**src/arc-flexunit/build`**`**
> Build files for arc-flexunit.

**templates/SampleAS3/`**`**
> Template project for building an AS3 only application.

## Updated Files ##

**lib/RunAirTests-app.xml**
> Updated the descriptor version to 1.5.

**src/arc-flexunit/`**`**
> Facility added to disable the AlwaysFail test.

**tools/build-common-targets.xml**
> Fix test SWF launch path issue for non Mac platforms.
> Support for the new AlwaysFail test disabling.

**tools/build-common-properties.xml**
> Support for the new AlwaysFail test disabling.

## New Properties (tools/build-common-properties.xml) ##

**arc-flexunit.filters-fail**
> Flag to control the inclusion of the AlwaysFail test when using a
> filters file.  This property can be overridden in
> build-user.properties or in a project's build.xml with a value of
> -skipAlwaysFail to change the default behavior.

> Default: -alwaysFail