Cross-Platform JSLint Support for Sublime Text Editor 2 (using NodeJS)
========================

JSLint is an indispensable tool if you're serious about your JavaScript code quality. This project provides a cross-platform script which helps Sublime Text 2 to check JSLint when you’re working within a JavaScript file.

Features
-------------

- Validate JSLint on Save

- JSLint: Quick Check (Super+Shift+L)

- JSLint: View Full Report (Super+Shift+Alt+L)

- Using NodeJS

- Notification Support
	- Using Growl (http://growl.info/) on OSX and notify-send on Ubuntu/Linux.
	- Those settings are configurable on "Sublime-JSLint (Linux).sublime-settings", "Sublime-JSLint (OSX).sublime-settings", and "Sublime-JSLint (Windows).sublime-settings".

Requirements
-------------

- You need to have NodeJS installed (http://nodejs.org/)

- For Linux Users: Install "libnotify-bin" lib to enbale "notify-send" command:

	- # apt-get install libnotify-bin

- For OSX Users: Install "growlnotify":

	- Download the latest Growl version from http://growl.info/downloads, inside the .dmg file, go to "Extras" folder and install "growlnotify.pkg".

- DO NOT DO THIS STEP IF YOU ARE USING THE DEFAULT INSTALLATION FOR THE REQUIREMENTS SPECIFIED IN THIS SECTION!
	
	- Those settings are configurable overriding the properties from your user settings. To create a user settings create the following setting filenames inside "User" folder on packages folder: "Packages/User/Sublime-JSLint (Linux).sublime-settings", "Packages/User/Sublime-JSLint (OSX).sublime-settings", and "Packages/User/Sublime-JSLint (Windows).sublime-settings".

	- Update the "node_path" and "notification_command" on your system to the right paths:

	{
		"node_path": "/usr/local/bin/node",
		"notification_command": "/usr/bin/notify-send \"%(title)s\" \"%(msg)s\" --icon=\"%(image)s\""
	}

How to use?
-------------

- When Sublime saves a JavaScript file it runs the Quick Check displaying the notification alert.

- Yoi can also access using the Command Palette (Super+Shift+P) then search for:

	- JSLint: Quick Check (Super+Shift+L)
	- JSLint: View Full Report (Super+Shift+Alt+L)

Open up a .js file and hit Super+Shift+L for Quick Report and Super+Shift+Alt+L. An inline prompt will appear giving you the JSLint results:

Screenshots
-------------

![](https://github.com/eduardolundgren/Sublime-JSLint/raw/master/images/screenshot.png)
![](https://github.com/eduardolundgren/Sublime-JSLint/raw/master/images/preview.png)

Changeset
-------------

Rhino is no longer being used as default engine due to performance issues, NodeJS (http://nodejs.org/) is now being used instead.