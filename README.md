# &lt;num-stepper&gt;

HTML custom element for numeric range entry.

## Demo
[See demo](http://bbrewer97202.github.io/num-stepper/demo.html)

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install num-stepper --save
```

## Usage

Embed element on page with initial, mimimum, maximum and step values. 

```HTML
<num-stepper min="5" max="18" step="1" value="9"></num-stepper>
```

Get the current value from the element value attribute:

```JavaScript
document.querySelector('num-stepper').getAttribute('value')
```

Listen for _ready_ and _change_ events to get the selected value:

```JavaScript
var exampleStepper = document.querySelector('num-stepper');

exampleStepper.addEventListener('ready', function(e) {
    console.log("initialized with value: " + e.detail.value);
});

exampleStepper.addEventListener('change', function(e) {
    console.log("changed with value: " + e.detail.value);
});
```

## Notes    
No extra requirements if run in a browser that supports custom elements, shadow DOM and HTML imports.  Otherwise, use the webcomponents.js polyfill from bower.io.

May require polyfills for older IEs (for CustomEvent, classlist).

## License

[MIT License](http://opensource.org/licenses/MIT)
