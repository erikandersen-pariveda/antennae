# Changes in Antennae 1.0001 #

**Flex based AIR application support**
> New targets and tasks have been added to support the building,
> running, and packaging of Flex based AIR applications.

> A sample project has been put together that demonstrates the use
> of these new targets.

> A key concept used in AIR application support is the concept of an
> "assets" directory. Since the AIR ADT application packager
> requires you to specify each file that should be bundled into the
> application, Antennae has instead chosen to specify a single
> directory. The goal being that by default all files under "assets"
> will be packaged with the application and there is no need to
> include these files in the source tree.

**Simplified importing**
> All template applications have been updated to use the new single
> build-common-imports.xml file to pull in all standard Antennae
> build files.

**Source code included**
> The source code for the ARC-FlexUnit pieces are now bundled with
> Antennae. This is for reference purposes. To rebuild the platform
> please grab the latest source code from the SVN repository for
> Antennae. http://antennae.googlecode.com/svn/

**Linux fixes**
> Fixed bug about not being able to run automated unit tests on Linux.

# Updated Files #

**build-user.properties.mac**
> Updated to include new required and optional AIR properties.

**build-user.properties.win**
> Updated to include new required and optional AIR properties.

**templates/Sample?/build.xml**
> Updated to reference new build-common-imports.xml file.

# New Files #

**tools/build-common-imports.xml**
> This provides a single file that projects can import that will
> pickup all the other standard build-common-?.xml files.

**templates/SampleAIRApplication**
> Sample project that demonstrates using the new AIR targets
> (described below) to build and run a Flex based AIR application.

# New Targets (tools/build-common-targets.xml) #

**air-application**
> Compiles an AIR application based on a project.mxml and
> project-app.xml file existing the in source directory.

**air-library**
> Compiles source that use AIR APIs into a .swc for use by other
> AIR applications.

**air-application-stage**
> Copies the compiled application, descriptor, and assets
> directory into a stage directory for running or packaging.

**air-package**
> Creates a .air file using ADT based on the content of the stage
> directory. Includes certificate support.

**air-launch**
> Launch your AIR application from the stage directory using ADL.

# New Tasks (tools/build-common-tasks.xml) #

**adl**
> Handles calling ADL with the needed arguments to run an AIR
> application.

**adt**
> Handles calling ADT with to package an AIR application.

# New Properties (tools/build-common-properties.xml) #

**project.air**
> Name of the .air file to produce when packaging an AIR
> application.

> Default: ${project.name}.air

**project.air.desc**
> Name of the AIR descriptor file that should be used for running
> and packaging the application.

> Default: ${project.name}-app.xml

**air.config**
> Location of the AIR specific configuration file used by the Flex
> compiler to build an AIR application.

> Default: ${flex2.frameworks.dir}/air-config.xml

**air.adt.jar**
> Location of the ADT jar that is used to package an AIR application.

> Default: ${flex2.dist.lib}/adt.jar

**src.assets.dir**
> Location of a directory that includes files that should be bundled
> with the AIR application.

> Default: assets

**build.assets.dir**
> Location that the contents of the assets directory are copied to
> when staging the AIR application.

> Default: ${build.stage.dir}/assets

**air.adl**
> Location of the ADL executable.

> Default: ${flex2.dir}/bin/adl.exe (windows) or ${flex2.dir}/bin/adl (mac)

# New unspecified properties #

**air.certificate**
> Required by air-package target

> Location of the certificate file to sign the AIR application with.

> No default, specify in build-user.properties

**air.certificate.password**
> Optional, will prompt if not specified

> Password associated with the certificate file

> No default, optionally specify in build-user.properties