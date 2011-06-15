HTML5 Boilerplate Publish Up The Tree
=====================================

Sorry it's not a more creative name...

The problem I had was I wanted the wonderful HTML5 Boilerplate build script to publish up the tree, rather than into a /publish folder. This was because I wanted to be able to use Git with the project, deploy using Git, then build on the server. This is fine for JS apps, and Paul Irish shows a way to do it in the video, but if one is building a webapp, the security is not good enough. You shouldn't have any code in your public folder, it should always be above.

Anyway, this is designed for use with Fuel and CodeIgniter, as well as other apps. I'll more details soon.
