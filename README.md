FIDATA Eclipse
==============

1.	Сustom Eclipse configuration

	Using Yoxos, I've made FIDATA Eclipse, custom Eclipse
configuration for development of FIDATA. You can freely (registration
is required) download it for your platform from
https://yoxos.eclipsesource.com/userdata/profile/ce4122db97d0e3997ad7040db041d755

	Otherwise, if you have Yoxos Launcher >= 5.4.3 installed, you can
open file `FIDATA.yoxos` from this repository.

	After unpacking make the first run, it takes some time.

	Links to download Yoxos Launcher:
	*	[Yoxos](https://yoxos.eclipsesource.com/downloadlauncher.html)
	*	[Chocolatey](https://chocolatey.org/packages/yoxos-launcher/)

2.	Additional plugins for Eclipse

	Unfortunately, some required plugins aren't provided by Yoxos, and
you have to install them manually using the following steps:

	1.	Import `bookmarks.xml` from this repository into Available
Software Sites (Preferences -> Install/Update -> Available Software
Files).

	2.	Using Help -> Install New Software, install the following
plugins:
		1.	CMake Editor
		2.	StatET for R
		3.	StatET for R - R tasks Add-on for Graphics ('ggplot')
		4.	ReST Editor
		5.	Doxia Editors Feature
		6.	WFE Wordfile Editor
		7.	TeXLipse
		8.	Pdf4Eclipse

	3.	Using Help -> Install Papyrus Additional Components, install the
following plugins:
		1.	MARTE
		2.	RealTime
		3.	Diagram generation
		4.	Papyrus Layers
		5.	Qompass
		6.	Moka

	I also recommend to check for updates (Help -> Check for Updates).


------------------------------------------------------------------------
Copyright © 2013, 2014, 2017  Basil Peace

This is part of FIDATA.

Copying and distribution of this file, with or without modification,
are permitted in any medium without royalty provided the copyright
notice and this notice are preserved.  This file is offered as-is,
without any warranty.
