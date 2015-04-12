# javascript-editor

[codemirror](http://codemirror.net/) + [esprima](http://esprima.org/) powered html5 javascript editor component

based originally on [htmleditor](http://mrdoob.com/projects/htmleditor/) by mrdoob

## features

- JS syntax highlighting
- JS errors are detected and highlighted as you code
- by default if you drop a .js file on the editor it will load the contents
- modular and installable with NPM

## usage

Install Node and [browserify](http://browserify.org).

 1. `git clone https://github.com/liamzebedee/javascript-editor`
 2. `cd javascript-editor && npm install`
 3. `browserify demo.js -o bundle.js`

Then include `bundle.js` and all the CSS files included in the directory, and access the global.jsEditor function to do things further.

```javascript
var editor = jsEditor({ container: document.querySelector('#editor') })

editor.on('change', function() {
  var value = editor.getValue()
})

editor.on('valid', function(noErrors) {
  // noErrors is a boolean
})
```

### default options

```javascript
var defaults = {
	value: "// hello world\n",
	container: document.body,
	mode: "javascript",
	lineNumbers: true,
	matchBrackets: true,
	indentWithTabs: false,
	tabSize: 2,
	indentUnit: 2,
	updateInterval: 500,
	dragAndDrop: true
}
```

## license

BSD
