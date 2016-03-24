nutjar
=
-----

A multi-version squirrel/nuts#5 server built for node.js

> **!** This is stackdesk-nutjar but evolved and preped for use in non-electron apps (even though it works in electron)

Originaly created to supply a simple squirrel update server.
Recommened that you learn to use squirrel at their git repos here

Usage (non-npm)
=

For use on a personal computer
------------------------------

> **!** This only works if you have a static IP adress! Users will not be able to connect if you have a dynamic IP adress! Even if you use DNS!

You must have *Node.js*/*NPM* installed for this tool to work properly

 1.  Git-Clone the repository to your computer with `$ git clone http://www.github.com/vogasoftware/nutjar.git`
 2. Change-Directory (`cd`) into the directory you git-cloned to.
 2. Update required packages automagically with `$ npm install`
 3. To start the server run `npm start`
 4. You will see something allong the lines of:

        $ npm start

        > stackdesk-nutjar@0.2.5 start C:\ladel\stackdesk\nutjar
        > squirrel-server --port 8080 --releases ./releases.json

 5. YOU WILL NOT GET ANY OUTPUT AFTER THAT! But, congradulations your server is now online! *claping for you excitedly*.

For use on Docker/Heroku
-
 1.  Git-Clone the repository to your computer with `$ git clone http://www.github.com/vogasoftware/nutjar.git`
 2. Change-Directory (`cd`) into the directory you git-cloned to.
 3. Execute:
 For heroku (*REQUIRES [HEROKU TOOLBELT*](https://toolbelt.heroku.com/)):

        heroku create my-nutjar
        git push heroku master

 For docker (*REQUIRES [DOCKER ENGINE](https://docs.docker.com/engine/installation/)*)

        docker build -t my-nutjar .
        docker run -p 3000 my-nutjar
 4. And it should run elegantly at this point!

Usage (npm)
=
This method is for using a dedicated home computer.
We do not recommend using this method for heroku/docker servers

 1. CD into your node.js application directory.
 2. Run the command `npm install nutjar`
 3. Run the command `cd node_modules` and then run `cd nutjar`
 4. To start your squirrel server run `npm start`.
 5. YOU WILL NOT RECIEVE ANY OUTPUT.

Configuration
=
Most of the configuration magic goes on in package.json's definitive line of:

    "start": "squirrel-server --port 8080 --releases ./releases.json"

Editing this must be tailored to how it should be formatted if you wish to change your releases file.

Credit
=
This application mainly uses the `squirrel-server` npm module. In fact it is simply a simplified version of this application.
