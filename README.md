#Blank OpenWhisk Bot


##Instructions

Prerequisites: I assume you have node and npm installed. Need help installing either? [Here's a link for you.](http://blog.npmjs.org/post/85484771375/how-to-install-npm)

1. Clone this repo
2. Run `npm install`
3. Open in your favorite editor.

##Configuration

To run this bot yourself you will need Twitter and Bluemix credentials.

#####For Twitter, you will need:

* a Twitter account
* a Twitter application (not the same as a Twitter account; apply for one at apps.twitter.com)
* a Consumer Key, a Consumer Secret, an Access Token, and your Access Token Secret

Put this information in the `temp-config.js` file, and rename it to `config.js`. Then delete `temp-config.js`.

#####For OpenWhisk, you will need:

* Bluemix account
* Openwhisk installed
* You can also run your own OpenWhisk! This is beyond the scope of this workshop, but you can find more info [here](https://github.com/openwhisk/openwhisk).


#####Configuring for OpenWhisk

TK


##Source Data

To add text for your bot to tweet, add it in the `botfiles/sample-text.js` file.

IMPORTANT: you must install the botfiles folder as a local module before deploying: 

`npm install --save ./botfiles`

If you make changes, you must update the installation: 

`rm -rf node_module/botfiles && npm install --save ./botfiles`

##Tests
There are tests for the functions in `index.js` in the `tests/test.js` file. Run them with `npm test`.

##Running Your Bot with OpenWhisk


##Thank Yous
Thanks to [Darius Kazemi](https://github.com/dariusk) for the wordfilter module and for the .pick function. Thanks to [Thoughtworks](https://github.com/ThoughtWorksStudios) for the wonderful [node-aws-lambda](https://github.com/ThoughtWorksStudios/node-aws-lambda) module. Thanks also to [Allison Parrish](https://twitter.com/aparrish) and David Celis for reviewing; all errors remain the exclusive property & reponsibility of the author. :-)

wsk action create packageAction --kind nodejs:6 openwhisk.zip
wsk action update packageAction --kind nodejs:6 openwhisk.zip