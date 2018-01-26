# Krupskiy35.yokngalam.github.io


Author: Krupskiy Andrey

Cross-browser compatibility: IE9+.

The template uses a Less with Less syntax and project was built with the help of the webpack assembler, that contains ready project with optimized HTML, CSS, JS and images.


1. npm install <br>
2. npm start-command that will start the dev server, it is necessary to compile less / ES6 files<br>
3. Go to the browser at http: // localhost: 8080<br>
4. To stop the server in the console (terminal), press CTRL + C twice. If there are compilation errors, there will be red error messages in the terminal, at the very beginning of the message it is described quite precisely what went wrong, pay attention to it. Also, in case of problems with the assembly, please apply a screenshot with the text of the console error

File structure
assets - directory for storage of asets - image fonts usage example look in common / styles / header.less<br><br><br>


src<br>
.<br>
|<br>
├──index - page index.html and all that apply to it<br>
|   |<br>
|   +-- scripts - scripts must be imported into index.js<br>
|   +-- styles - styles must be imported into index.less<br>
|   +-- index.html - main document html, home page of your site<br>
|   +-- index.js - the main file js, the entire script that refers to this page is imported into this file (from the scripts directory)<br>
|   +-- index.less - main style file<br>
+- common - the directory where you store the common files for all pages of your site, for example, styles and scripts to use, you need to put in the main file of the pages to look at index / index.less<br>
    |<br>
    +- scripts<br>
    |<br>
    +- styles <br>    
    
    
    
 If there is a need to add a new page, you need to create a directory with the name of your page, html, js and less. The file should be named the same as the name of the directory, see the example src / about. After creating the directory, you need to connect this page to the webpack assembly. Open config / base.js in entry - add the following line to the name of your folder, for example test, then the line will look like test: ['babel-polyfill', './src/test/test.js'], as a result entry should look like as :  <br><br>
 
 сonst entry = {<br>
        index: ['babel-polyfill', './src/index/index.js'],<br>
        about: ['babel-polyfill', './src/about/about.js'],<br>
        test: ['babel-polyfill', './src/test/test.js']<br>
    };
