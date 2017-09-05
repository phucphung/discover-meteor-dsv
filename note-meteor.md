__author__ Tom coleman and Sacha Greif


[Github repository](https://github.com/DiscoverMeteor/Microscope)

- Code in the /server directory only runs on the server.
- Code in the /client directory only runs on the client.Everything else runs on both the client and server.
- Your static assets (fonts, images, etc.) go in the /public directory.
- And it’s also useful to know how Meteor decides in which order to load your files:
- Files in /lib are loaded before anything else.
- Any main.* file is loaded after everything else.
- Everything else loads in alphabetical order based on the file name.
