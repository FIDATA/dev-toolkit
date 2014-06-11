FIDATA dev-toolkit
==================

Environment for building and development of FIDATA.


Build environment:
------------------

1.	Java SE Development Kit

	Both Maven and Gradle require JDK 5 or later. For development (see
below) you need more fresh version. The latest update is highly
recommended ([security]).

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

3.	Gradle >= 1.7

	Download page: http://www.gradle.org/downloads.

	Environment variables: `gradle` should be accessible from command
line.

4.	CMake

	Download page: http://www.cmake.org/cmake/resources/software.html.

5.	Qt Installer Framework

	Download page:
http://download.qt-project.org/official_releases/qt-installer-framework/.

	Environment variables: Qt Installer Framework `bin` directory
should be included in `PATH`.

6.	Git client

	Under Windows I prefer Git for Windows + TortoiseGit.

	Download pages:
	*	http://code.google.com/p/msysgit/downloads/list?q=full+installer+official+git;
	*	http://code.google.com/p/tortoisegit/wiki/Download.

	Environment variables: `git` should be accessible from command
line.


### Build environment for documentation:

7.	LuaLaTeX and required packages

	For Windows I recommend TeX Live.

	Download page: http://tug.org/texlive/acquire-netinstall.html.

	Environment variables: `lualatex`, `latexmk`, `makeindex` and other
LaTeX executables should be accessible from command line.

	If you use custom distribution, at least the following packages are
required:
	*	latexmk
	*	docstrip
	*	ltxdoc
	*	geometry
	*	graphicx
	*	caption
	*	color
	*	array
	*	ragged2e
	*	longtable
	*	dcolumn
	*	fancyhdr
	*	natbib
	*	fontspec
	*	amsfonts
	*	amsmath
	*	unicode-math
	*	url
	*	hyperref
	*	lipsum

	This list is not thorough. Rely on errors from LuaLaTeX/Latexmk
for resolving other requirements.

	TeX Live full installation contains all requirements.

8.	Haskell

	Haskell is required by pandoc.

	Download page: http://www.haskell.org/platform/.

9.	Pandoc

	Download page: http://johnmacfarlane.net/pandoc/installing.html.

	Environment variables: `pandoc` should be accessible from command
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

4.	Python 3

	I use Python 3.3 and I'm not sure about ability to work with other
versions.

	Download page: http://python.org/download/.

	Environment variables: Python installation directory should be
included in `PATH`.

5.	Eclipse (custom configuration FIDATA Eclipse)

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
		1.	Mylyn Tasks Connector: Mantis (it's needed if you want to
work with my private bug tracker (see below))
		2.	Gradle IDE
		3.	CMake Editor
		4.	StatET for R
		5.	ShellEd
		6.	JSON Editor Plugin
		7.	ReST Editor
		8.	GFM Viewer Feature
		9.	Doxia Editors Feature
		10.	WFE Wordfile Editor

	3.	Using Help -> Install Papyrus Additional Components, install the
following plugins:
		1.	MARTE 1.1
		2.	UML-RT
		3.	Diagram generation

	Environment variables: I recommend to include Eclipse's directory in
`PATH`, however, at present it is not required.

	I also recommend to check for updates (Help -> Check for Updates).

7.	yEd Graph Editor >= 3.11

	It's suited for creation of nice graphs, and it stores them in
GraphML format. It isn't open source, but free of charge.

	Download page: http://www.yworks.com/en/downloads.html#yEd. Get
version without JRE included.


### Optional features

1.	Console text editor

	For editing commit messages I prefer Nano, which is available under
both Windows and Linux.

	Download page: http://www.nano-editor.org/download.php.

	Environment variables: set `EDITOR` to be pointed to Nano (or other
editor), so it can be used by git (and maybe other VCSs) for editing
commit messages.


Links for Development Team
--------------------------
*	FIDATA organization on GitHub, including all source repositories

	https://github.com/FIDATA/

*	Private bug tracker

	[Mantis](http://grv87.ftp.sh/bugs/)

*	Yoxos FIDATA Eclipse Profile

	https://yoxos.eclipsesource.com/userdata/profile/ce4122db97d0e3997ad7040db041d755

*	Continuous Integration System

	[Jenkins](http://grv87.ftp.sh:8082/)

*	Continuous Inspection of Code Quality Tool

	[SonarQube](http://grv87.ftp.sh:9000/)

*	Artifact Repository Manager

	[Artifactory](http://grv87.ftp.sh:8081/)

Please note, that grv87.ftp.sh is the DDNS address of my home
computer (hosted by [FreeDNS](https://freedns.afraid.org/)). Please,
don't abuse that. Also, although my PC is usually switched-on 24/7,
it is not [highly available]
(http://en.wikipedia.org/wiki/High_availability). I can have maintenance
hours and power and network outages.


------------------------------------------------------------------------
Copyright © 2013, 2014  Basil Peace

This is part of FIDATA.

Copying and distribution of this file, with or without modification,
are permitted in any medium without royalty provided the copyright
notice and this notice are preserved.  This file is offered as-is,
without any warranty.
