protrader.dev-toolkit
=====================

Toolkit for building or development of ProTrader.

Build environment:
------------------

1.	Java SE Development Kit

	Maven requires JDK 1.5 or later. For development (see below) you
need more fresh version. The latest update is highly recommended
([security]).

	Download page: http://www.oracle.com/technetwork/java/javase/downloads/index.html.

	Environment variables: `JAVA_HOME` should be set to JDK installation
path, and Java `bin` directory should be included in `PATH`.

2.	Apache Maven

	Download page: http://maven.apache.org/download.cgi.

	Environment variables: Maven `bin` directory should be included in `PATH`.

3.	SSH client

	Under Windows I use PuTTy.

	Download page: http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html.

	Mose Linux users use OpenSSH: http://www.openssh.org/.

	Environment variables: ssh client should be accessible from command
line.

4.	CMake

	Download page: http://www.cmake.org/cmake/resources/software.html.

5.	Qt Installer Framework

	Download page: http://download.qt-project.org/official_releases/qt-installer-framework/.

Development environment:
------------------------

1.	Java SE Development Kit 1.7
	*	Eclipse Kepler (4.3) requires JRE 1.4 or later, and 1.5 is
recommended.
	*	PyDev requires 1.7.
	*	yEd requires JRE 1.6 or later.

	So, development environment in total requires JDK 1.7. Custom
Eclipse configuration (see below) is made with

		-Dosgi.requiredJavaVersion=1.7

	The latest update in highly recommended ([security]).

2.	Everything else for build (see above)

3.	Python 3

	I use Python 3.3 and I'm not sure about workability with other versions.

	Download page: http://python.org/download/.

	Environment variables: `PYTHONHOME` should be set to Python
installation path, and this path should also be included in `PATH`.

4.	Eclipse (custom configuration)

	Using Yoxos, I've made custom Eclipse configuration for development
of ProTrader. You can freely (registration is required) download it for
your platform from
https://yoxos.eclipsesource.com/userdata/profile/0ff9e65119e71c770a9200891ba741ed

	Otherwise, if you have Yoxos Launcher >= 5.4.3 installed, you can
open file `ProTrader.yoxos` from this repository.

	After unpacking make the first run, it takes some time.

5.	Additional plugins for Eclipse

	Unfortunately, some required plugins aren't provided by Yoxos, and
you have to install them manually using the following steps:

	1.	Import `bookmarks.xml` from this repository into Available
Software Sites (Preferences -> Install/Update -> Available Software
Files).

	2.	Using Help -> Install New Sofware, install the following plugins:
		*	Mylyn Tasks Connector: Mantis
		*	Google Code Mylyn Connector Feature
		*	Bazaar Team Provider
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

6.	yEd Graph Editor >= 3.11

	It isn't open source, but free of charge.

	Download page: http://www.yworks.com/en/products_yed_download.html.
