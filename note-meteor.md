__author__ Tom coleman and Sacha Greif


[Github repository](https://github.com/DiscoverMeteor/Microscope)

- Code in the /server directory only runs on the server.
- Code in the /client directory only runs on the client.Everything else runs on both the client and server.
- Your static assets (fonts, images, etc.) go in the /public directory.
- And it’s also useful to know how Meteor decides in which order to load your files:
- Files in /lib are loaded before anything else.
- Any main.* file is loaded after everything else.
- Everything else loads in alphabetical order based on the file name.


- Spacebars is simply HTML, with the addition of three things: inclusions (also sometimes known as “partials”), expressions and block
helpers.
- Inclusions use the {{> templateName}} syntax, and simply tell Meteor to replace the inclusion with the template of the same name (in our case postItem ).
- Expressions such as {{title}} either call a property of the current object, or the return value of a
template helper as defined in the current template’s manager (more on this later).
- Finally, block helpers are special tags that control the flow of the template, such as
```
{{#each}}
{{/each}}
or
{{#if}}...{{/if}}
```

- The browser’s memory: things like JavaScript variables are stored in the browser’s
memory, which means they’re not permanent: they’re local to the current browser tab, and
will disappear as soon as you close it.
- The browser’s storage: browsers can also store data more permanently using cookies or
Local Storage. Although this data will persist from session to session, it’s local to the current
user (but available across tabs) and can’t be easily shared with other users.
- The server-side database: the best place for permanent data that you also want to make
available to more than one user is in a good old database (MongoDB being the default
solution for Meteor apps).
