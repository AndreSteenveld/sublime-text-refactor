Javascript Refactor plugin for Sublime Text 2 and 3 
===============================
<img src="https://travis-ci.org/s-a/sublime-text-refactor.png" />

Overview
========

- Extract selected source to a new method.
- Goto definition of a variable or function.
- Rename variable or function respecting its current scope.


Preview
========
http://www.youtube.com/watch?v=P9K7mxWItPw  
<img src="http://saquery.com/blg/wp-content/uploads/sublime-text-javascript-refactor.png" width="400" />

Installation
============

Use the Sublime Package Control and search for: "JavaScript Refactor"  
or  
Clone or download the git repository into your packages folder. 
In Sublime Text use "Preferences/Browse Packages" menu item to open this folder. 
The shorter way of doing this is: 
#### Linux
`git clone https://github.com/s-a/sublime-text-refactor ~/.config/sublime-text-2/Packages/sublime-text-refactor`

#### Mac
`git clone https://github.com/s-a/sublime-text-refactor ~/Library/Application\ Support/Sublime\ Text\ 2/Packages/sublime-text-refactor`

#### Windows
`git clone https://github.com/s-a/sublime-text-refactor %APPDATA%/Sublime\ Text\ 2/Packages/sublime-text-refactor`


Dependencies
============
- This Plugin makes heavy usage of Node.js. So it needs a local installation of http://nodejs.org 
- mocha (only for testing)

Usage
=====

***Extract Method:***  
Select the source code you want to extract into a new method and choose "Refactor / Extract methode" from context menu. 
This will extract the source code instantly to a new methode aka function. The plugin will manage undeclared variable usages and pass them within a single bundled JSON parameter to the new function.
It als generates a sample function call at the bottom of the new methode.
The plugin marks all variables occurring in the source code so you can rename them on the fly. 

***Goto Definition:***  
Select a keyword via double click or point the cursor to the keyword and choose "Goto Definition" from context menu.

***Rename:***  
Select a keyword via double click or point the cursor to the keyword and choose "Rename" from context menu. The plugin will select all variables or function calls occurring in the source code including its declaration. After that you rename them all on the fly. The logic respects the variables or functions scope. So it should be save to rename them all without thinking ;) .

Run the tests
=============
Goto Pluginfolder and type 
    npm test

You can find an examples of current test cases here...  
https://github.com/s-a/sublime-text-refactor/blob/master/js/test/


Todo
========================
- ***Extract method***  
- Define exceptions of global scoped variable names like jQuery or $.
- Do not pass variables available in current Scope (optional).
- Let the user choose a function name before or after extraction.
- Let the user choose a custom position to insert extracted methode code and indent it correctly.


License
=======


MIT and GPL license.

Copyright (c) 2013 Stephan Ahlf <stephan@ahlf-it.de>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.