# X-editable

In-place editing with Twitter Bootstrap, jQuery UI or pure jQuery.  
It is a new life of [bootstrap-editable plugin](http://github.com/vitalets/bootstrap-editable) that was strongly refactored and improved. 

## Demo + Docs + Download
See **http://vitalets.github.com/x-editable**

## Reporting issues
When creating issues please provide jsFiddle example. You can just fork [this fiddle](http://jsfiddle.net/xBB5x/5/) as starting point.  
Your feedback is very appreciated!

## Contribution
A few steps how to start contributing:  

1.[Fork X-editable](https://github.com/vitalets/x-editable/fork) and pull the latest changes from <code>dev</code> branch

2.Arrange local directory structure. It should be:  
**x-editable**  
 | -- **lib** (repo related to <code>dev</code> and <code>master</code> branches)  
 | -- **gh-pages** (repo related to <code>gh-pages</code> branch for docs & demo)  
 | -- **playground** (simple node-server and html page for testing, [playground.zip](https://github.com/downloads/vitalets/x-editable/playground.zip))      

To make it easy follow this script ( _assuming you have [nodejs](http://nodejs.org) installed_ ).
Please replace <code>&lt;your-github-name&gt;</code> with your name:
````
mkdir x-editable
cd x-editable

#lib
git clone https://github.com/<your-github-name>/x-editable.git -b dev lib
cd lib
#install gruntjs globally - building tool
npm install -g grunt 
#install other dependencies - grunt-contrib
npm install 
cd ..

#gh-pages
git clone https://github.com/<your-github-name>/x-editable.git -b gh-pages gh-pages
cd gh-pages
npm install 
cd ..

#playground 
#download playground.zip from https://github.com/downloads/vitalets/x-editable/playground.zip
unzip playground.zip
cd playground
npm install 
````  
3.That's it! You can start editing files in **lib/src** directory or create new editable input/container/whatever.  
To test the result go to **playground**, start server <code>node server.js</code> and open in your browser [http://localhost:3000/playground](http://localhost:3000/playground).

4.To run unit tests you can open it directly in browser **lib/test/index.html**.   
Or use grunt's _qunit_ task <code>grunt test</code>. For that you also need to [install PhantomJS](https://github.com/gruntjs/grunt/blob/master/docs/faq.md#why-does-grunt-complain-that-phantomjs-isnt-installed)

5.To build lib + docs:
* run <code>grunt build</code> in **lib** directory
* run <code>build data-docs-dist</code> in **gh-pages** directory  
You will get distributive in **lib/dist** and updated docs in **gh-pages/*.html**.  
Do not edit **index.html** and **docs.html** directly! Instead look at [Handlebars](https://github.com/wycats/handlebars.js) templates in **generator/templates**.

6.Commit changes on <code>dev</code> / <code>gh-pages-dev</code> branch and make pull request as usual.  

Thanks for your support!

## License
Copyright (c) 2012 Vitaliy Potapov  
Licensed under the MIT licenses.