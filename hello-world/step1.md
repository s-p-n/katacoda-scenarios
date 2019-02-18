How to create an Arini Project on Ubuntu with npm.

### First, make a directory for your project.

`mkdir project`{{execute}}

### Now, enter that directory

`cd project`{{execute}}

### Once you're in there, run npm init and install arini

`npm init && npm i --save -g arini`{{execute}}

Follow the directions from npm to initialize your Node.JS prackage.

#### Once that's done, create an arini program:
`touch program.ari`{{execute}}


<pre class="file" data-filename="project/program.ari" data-target="replace">
  console.log("Sup?");
</pre>
