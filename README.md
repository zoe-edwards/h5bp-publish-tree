HTML5 Boilerplate Publish Up The Tree
=====================================

Sorry it’s not a more creative name...

The problem I had was I wanted the wonderful HTML5 Boilerplate build script to publish up the tree, rather than into a /publish folder. This was because I wanted to be able to use Git with the project, deploy using Git, then build on the server. This is fine for JS apps, and Paul Irish shows a way to do it in the video, but if one is building a web app, the security is not good enough. You shouldn't have any code in your public folder, it should always be above.

Anyway, this is designed for use with Fuel and CodeIgniter, as well as other apps.

At the moment it’s only good for using public_html, no renaming options available, will build those back in soon.

__On build, it will remove the /dev/intermediate and /public_html.__

How to use
----------

1. Create a new folder for your web app. You’re looking at the home folder.

2. Create a folder called ‘dev’ or something similar.

3. Inside ‘dev’, create a folder called ‘public_html’.

4. Get a copy of HTML5 Boilerplate (H5BP), however you please.

5. Put /build from H5BP and put it in ‘dev’

6. Put everything else from H5BP in ‘public_html’

7. Download ‘Publish Up The Tree’ (above)

8. Replace the three files provided:
	* /dev/build/build.xml
	* /dev/build/config/*

9. Download Fuel or CodeIgniter and place in ‘dev’

10. Add views to /dev/build/config/project.properties as normal

11. Run build as normal

Structure
---------

This is what I’m talking about:

	/home/user
	|-- dev
	|   |-- build
	|   |   `-- build.xml etc
	|   |-- fuel
	|   |   |-- app
	|   |   |   |-- views
	|   |   |   |   |-- welcome
	|   |   |   |   |   |-- index.php
	|   |   |-- core
	|   |   `-- packages
	|   `-- public_html
	|       |-- apple-touch etc...
	|       |-- css
	|       |-- js
	|       |-- img
	|       `-- index.php
	|-- fuel
	|   |-- app
	|   |   |-- views
	|   |   |   |-- welcome
	|   |   |   |   |-- index.php
	|   |-- core
	|   `-- packages
	`-- public_html
	    |-- apple-touch etc...
	    |-- css
	    |-- js
	    |-- img
	    `-- index.php

In this situation, one would add ‘fuel/app/views/welcome/index.php’ to ‘file.pages’ in ‘project.properties’.

Limitations
-----------

* Cannot use different names or structure for /js /css etc
* Cannot use JSLint or JSHint
* Will remove everything in /dev/intermediate and /public_html