## Using [Grunt](http://gruntjs.com/) to Build
<i>“Not every person has the same kind of talents, so you discover what yours are and work with them.” — Frank Gehry.</i>

<p align="justify"><a href="http://gruntjs.com/">Grunt</a> — is the JavaScript Task Runner, that automates script minification, CoffeeScript or JavaScript compilation, code quality “lint” tools, CSS pre-processors, and just about any repetitive chore that needs doing to support client side development. Grunt is fully supported to build anything that is required for everyday programming task.</p>
<h3>Why to use Grunt?</h3>
<p align="justify">The Grunt ecosystem is huge and it's growing every day. With literally hundreds of <a href="http://gruntjs.com/plugins/">plugins</a> to choose from, you can use Grunt to automate just about anything with a minimum of effort. If someone hasn't already built what you need, authoring and publishing your own Grunt plugin to <a href="https://www.npmjs.com/">npm</a> is a breeze.</p>
<ol>
  <li>
    <h4>I don’t need the things Grunt does</h4>
    <p align="justify">You probably do, actually. Check out that list up top. Those things aren’t nice-to-haves. They are pretty vital parts of web application development these days. If you already do all of them, that’s awesome. Perhaps you use a variety of different tools to accomplish them. Grunt can help bring them under one roof, so to speak. If you don’t already do all of them, you probably should and Grunt can help. Then, once you are doing those, you can keep using Grunt to do more for you, which will basically make you better at doing your programming job.</p>
  </li>
  <li>
    <h4>Grunt runs on Node.js — I don’t know Node</h4>
    <p align="justify">You don’t have to know Node. Just like you don’t have to know Ruby to use Sass. Or PHP to use WordPress. Or C++ to use Microsoft Word.</p>
  </li>
  <li>
    <h4>I have other ways to do the things Grunt could do for me</h4>
    <p align="justify">Are they all organized in one place, configured to run automatically when needed, and shared among every single person working on that project? Unlikely, I’d venture.</p>
  </li>
  <li>
    <h4>Grunt is a command line tool — I’m just a designer</h4>
    <p align="justify">I’m a designer too. I prefer native apps with graphical interfaces when I can get them. But I don’t think that’s going to happen with Grunt<sup>1.</sup></p>
  </li>
</ol>
<p align="justify">The extent to which you need to use the command line is:</p>
<p align="justify">1. Navigate to your project’s directory.<br/>2. Type <code>$ grunt</code> and press <b>Return</b>.</p>
<p align="justify">After set-up, that is, which again isn’t particularly difficult.</p>
<h3>Okay. Let's get Grunt Installed</h3>
<p align="justify"><a href="https://nodejs.org/en/">Node</a> is indeed a prerequisite for Grunt. If you don’t have Node installed, don’t worry, it’s very easy. You literally <a href="https://nodejs.org/en/download/">download</a> an installer and run it. Click the big Install button on the Node website.</p>
<p align="justify">Now, you have to install Grunt. To do this, just use Terminal of your OS and type:</p>
<p align="justify">1. <code>$ npm install grunt -g</code><br/>2. <code>$ npm install grunt-cli -g</code></p>
<p align="justify">I’m using an <a href="https://gist.github.com/iamprabhat/ab14676bb8f432460efcf5e31af24f11">example code</a> to work with grunt to build everyday task(s).</p>
<p align="justify">The finished example cleans the target deployment directory, combines JavaScript files, checks code quality, condenses JavaScript file content and deploys to the root of the web application.</p>
<p align="justify"><b>I will use the following</b> <i>packages</i>:</p>
<ol>
  <li>
    <p align="justify"><a href="https://github.com/gruntjs/grunt">grunt</a>: The Grunt task runner package.</p>
  </li>
  <li>
    <p align="justify"><a href="https://github.com/gruntjs/grunt-cli">grunt-cli</a>: The Grunt command line interface.</p>
  </li>
  <li>
    <p align="justify"><a href="https://github.com/gruntjs/grunt-contrib-clean">grunt-contrib-clean</a>: A plugin that removes files or directories.</p>
  </li>
  <li>
    <p align="justify"><a href="https://github.com/gruntjs/grunt-contrib-less">grunt-contrib-less</a>: A plugin to Compile LESS files to CSS.</p>
  </li>
  <li>
    <p align="justify"><a href="https://github.com/gruntjs/grunt-contrib-jshint">grunt-contrib-jshint</a>: A plugin that reviews JavaScript code quality.</p>
  </li>
  <li>
    <p align="justify"><a href="https://github.com/gruntjs/grunt-contrib-concat">grunt-contrib-concat</a>: A plugin that joins files into a single file.</p>
  </li>
  <li>
    <p align="justify"><a href="https://github.com/gruntjs/grunt-contrib-uglify">grunt-contrib-uglify</a>: A plugin that minifies JavaScript to reduce size.</p>
  </li>
  <li>
    <p align="justify"><a href="https://github.com/gruntjs/grunt-contrib-watch">grunt-contrib-watch</a>: A plugin that watches file activity.</p>
  </li>
</ol>
<h3>Working for 'example-build'</h3>
<p align="justify">After that, you have to install Grunt on a per-project basis. Go to your project’s folder. It needs a file there named <code>package.json</code> at the root level. You can just create one and put it there.</p>
<p align="justify">1. <code>$ cd example-build</code><br/>2. <code>$ npm init</code></p>
<h3>Configuring NPM:</h3>
<p align="justify">In the <code>package.json</code> file, inside the devDependencies object braces, enter “grunt”, then put colon and version of it.</p>
<p align="justify">There is a simple way also to to do it. On Terminal of Mac OS, just type npm init and it will let you through all the processing.</p>
<p align="justify"><b>Note</b>: NPM uses <a href="http://semver.org/">semantic versioning</a> to organize dependencies. Semantic versioning, also known as SemVer, identifies packages with the numbering scheme. Always consider the latest stable version of the package. The caret (^) symbol matches the most recent major version and the tilde (~) matches the most recent minor version. See the <a href="https://www.npmjs.com/package/semver">NPM semver version parser reference</a> as a guide to the full expressivity that SemVer provides.</p>
<p align="justify">Add more dependencies to load grunt-contrib* packages for clean, less, jshint, concat, uglify and watch as shown in the example below. The versions do not need to match the example.</p>
