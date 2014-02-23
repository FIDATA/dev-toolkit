FIDATA.dev-toolkit
==================

Environment for building and development of FIDATA.

Build environment:
------------------

1.	Java SE Development Kit

	Maven requires JDK 5 or later. For development (see below) you need
more fresh version. The latest update is highly recommended
([security]).

	There are two most popular implementations:
	*	Oracle JDK
		*	It is known as more stable and having fewer bugs.
		Download page:
http://www.oracle.com/technetwork/java/javase/downloads/index.html.
	*	OpenJDK
		*	New versions of Oracle JDK are based on OpenJDK.
			See [Henrik Stahl. Moving to OpenJDK as the official Java SE
7 Reference Implementation]
(https://blogs.oracle.com/henrik/entry/moving_to_openjdk_as_the).

			However, it is claimed to be less stable.
		*	It is licensed under GPLv2 with the Classpath Exception.

		Download page for Linux: http://openjdk.java.net/install/.

		Unofficial builds for Windows from Alex Kasko (updated with some
lag): https://bitbucket.org/alexkasko/openjdk-unofficial-builds/.

	In development I use OpenJDK for it is FOSS. If you have some
troubles, try Oracle's distribution.

	Environment variables: `JAVA_HOME` should be set to JDK installation
directory, and Java `bin` directory should be included in `PATH`.

2.	Apache Maven

	Download page: http://maven.apache.org/download.cgi.

	Environment variables: `M2_HOME` should be set to Maven installation
directory, and Maven `bin` directory should be included in `PATH`.

3.	SFTP client

	Under Windows I use PuTTy.

	Download page: http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html.

	Most Linux users use OpenSSH: http://www.openssh.org/.

	Environment variables: sftp client should be accessible from command
line.

4.	CMake

	Download page: http://www.cmake.org/cmake/resources/software.html.

5.	Qt Installer Framework

	Download page: http://download.qt-project.org/official_releases/qt-installer-framework/.

	Environment variables: Qt Installer Framework `bin` directory
should be included in `PATH`.

6.	Git client

	Under Windows I prefer Git for Windows + TortoiseGit.

	Download pages:
	*	http://code.google.com/p/msysgit/downloads/list?q=full+installer+official+git;
	*	http://code.google.com/p/tortoisegit/wiki/Download.

	Environment variables: `git` should be accessible from command
line.


Development environment:
------------------------

1.	Java SE Development Kit 7
	*	Eclipse Kepler (4.3), including Java Development Tools, requires
JRE 4 or later, and 5 is recommended.
	*	PyDev requires JDK 7 (see e.g.
http://stackoverflow.com/a/20604456/2576070).
	*	yEd requires JRE 6 or later.

	So, development environment in total requires JDK 7. Custom
Eclipse configuration (see below) is made with

		-Dosgi.requiredJavaVersion=1.7

	The latest update in highly recommended ([security]).

2.	Everything else for build (see above)

3.	Mercurial client

	Under Windows I use TortoiseHg.

	Download page: http://tortoisehg.bitbucket.org/download/index.html.

	Environment variables: `hg` should be accessible from command
line.

4.	Python 3

	I use Python 3.3 and I'm not sure about ability to work with other
versions.

	Download page: http://python.org/download/.

	Environment variables: Python installation directory should be
included in `PATH`.

5.	Eclipse (custom configuration)

	Using Yoxos, I've made FIDATA Eclipse, custom Eclipse
configuration for development of FIDATA. You can freely (registration
is required) download it for your platform from
https://yoxos.eclipsesource.com/userdata/profile/ce4122db97d0e3997ad7040db041d755

	Otherwise, if you have Yoxos Launcher >= 5.4.3 installed, you can
open file `FIDATA.yoxos` from this repository.

	After unpacking make the first run, it takes some time.

6.	Additional plugins for Eclipse

	Unfortunately, some required plugins aren't provided by Yoxos, and
you have to install them manually using the following steps:

	1.	Import `bookmarks.xml` from this repository into Available
Software Sites (Preferences -> Install/Update -> Available Software
Files).

	2.	Using Help -> Install New Software, install the following
plugins:
		*	Mylyn Tasks Connector: Mantis (it's needed if you want to
work with my private bug tracker, located at http://grv87.ftp.sh/bugs/)
		*	CMake Editor
		*	StatET for R
		*	ShellEd
		*	JSON Editor Plugin
		*	ReST Editor
		*	GFM Viewer Feature
		*	WFE Wordfile Editor

	3.	Using Help -> Install Papyrus Additional Components, install the
following plugins:
		*	MARTE 1.1
		*	UML-RT
		*	Diagram generation

	Environment variables: I recommend to include Eclipse's directory in
`PATH`, however, at present it is not required.

	I also recommend to check for updates (Help -> Check for Updates).

7.	yEd Graph Editor >= 3.11

	It's suited for creation of nice graphs, and it stores them in
GraphML format. It isn't open source, but free of charge.

	Download page: http://www.yworks.com/en/downloads.html#yEd. Get
version without JRE included.

### Optional features

1.	Subversion client

	Under Windows I use TortoiseSVN with switched-on 'command line
client tools' feature.

	Download page: http://tortoisesvn.net/downloads.html.

	Environment variables: `svn` should be accessible from command
line.

2.	CVS client

	Under Windows I use TortoiseCVS.

	Download page: http://www.tortoisecvs.org/download.shtml.

	Environment variables: `cvs` should be accessible from command
line.

3.	Bazaar client
	*	Bazaar

		Download page: https://launchpad.net/bzr/+download.

		Since Bazaar is based on Python 2, Standalone Installer is
required.

		Environment variables: `bzr` should be accessible from command
line.
	*	Eclipse plugin: Bazaar Team Provider

4.	Console text editor

	For editing commit messages I prefer Nano, which is available under
both Windows and Linux.

	Download page: http://www.nano-editor.org/download.php.

	Environment variables: set `EDITOR` to be pointed to Nano (or other
editor), so it can be used by git (and maybe other VCSs) for editing
commit messages.


------------------------------------------------------------------------
Copyright © 2013, 2014  Basil Peace

This is part of FIDATA.

Copying and distribution of this file, with or without modification,
are permitted in any medium without royalty provided the copyright
notice and this notice are preserved.  This file is offered as-is,
without any warranty.
