# Javascript

JavaScript (JS) is a dynamic computer programming language.[5] It is most commonly used as part of web browsers, whose implementations allow client-side scripts to interact with the user, control the browser, communicate asynchronously, and alter the document content that is displayed. It has also become common in server-side programming, game development and the creation of desktop applications.

JavaScript is a prototype-based scripting language with dynamic typing and has first-class functions. Its syntax was influenced by C. JavaScript copies many names and naming conventions from Java, but the two languages are otherwise unrelated and have very different semantics. The key design principles within JavaScript are taken from the Self and Scheme programming languages. It is a multi-paradigm language, supporting object-oriented, imperative, and functional programming styles.

The application of JavaScript to use outside of web pages—for example, in PDF documents, site-specific browsers, and desktop widgets—is also significant. Newer and faster JavaScript VMs and platforms built upon them (notably Node.js) have also increased the popularity of JavaScript for server-side web applications. On the client side, JavaScript was traditionally implemented as an interpreted language but just-in-time compilation is now performed by recent (post-2012) browsers.

## How does it work?

* **Prototypical** Javascript does not have classes, so instead it uses functions that can be reproduced with the 'new' keyword (Ex. var x = new Person()) and can be extended with new properties with the '.prototype' function (Ex. Person.prototype.hairColor = 'black')

* **Linear** One process happens one after another, line by line

* **Storage** JavaScript programs run in memory and can access different types of local storage that exists within the user's browser

## Adding JavaScript to a webpage

* It is best to never include JavaScript directly into your HTML page within <script></script> tags. You should instead have a seperate .js file with your JavaScript code and include them into you web page like this:

```html
<script src="path/to/js/file"></script>
```

* It is recommended to include your JavaScript files at the bottom of the <body> section of your HTML document, as it allows the user to view the page while the JS files are being loaded. It also may be necessary if parts of your JS needs an element on the page to be present in order to attach an event listener to it.

## Data Types:

* **String**

	```javascript
	'hello'
	```

	* can be declared using either single or double quotes
	* If you are writing a string that has quotes within it, you can use escaping by using a backslash( \ ).

	```javascript
	'She\'ll be here soon'
	```

* **Number**
```javascript
1
```

* **Float**
	```javascript
	42.99
	```

	* **NOTE** even if they do not have a decimal point, are considered floats which can make working with prices, for example, a bit tricky


* **Boolean**
```javascript
	true && false
```

* **Null vs Undefined**
	* `undefined` means a variable has been declared but has not yet been assigned a value. On the other hand, `null` is an assignment value. It can be assigned to a variable as a representation of no value.
	* Also, `undefined` and `null` are two distinct types: `undefined` is a type itself (`undefined`) while `null` is an object.
	* Unassigned variables are initialized by JavaScript with a default value of `undefined`. JavaScript never sets a value to `null`. That must be done programmatically.

* **Array**
	```javascript
	var x = [1,2,3,'hello', true];
	```
	* used to store lists of values

* **Object**
	```javascript
	var x = { cat: 'feline', dog: 'canine' }
	```

* **Functions**
```javascript
var functionName = function(arguments) {
	/** code to execute */
};
```

	* Variables declared inside of a function is only accessible within that funciton, while variables declared outside of functions in the global scope are accessible within any function

## Variables
```javascript
var x = 'Meowcakes!';
```
* used to store values, which can be strings, arrays, objects, functions, or boolean values
* You can also declare a variable without an initial value for later use
```javascript
var x;
```

* used to organize data into key-value pairs
* the keys in an object can be assigned to any data type, including another object
* Values inside of an object are accessed through their keys. You can do this in two ways:
* x["cat"] /** returns feline */
* x.cat /** returns feline */


## Logging
```javascript
console.log("Hello World");
```

## Alert
```javascript
alert("Foo Bar");
```

## Prompt
```javascript
var userAge = prompt('What is your age?')
```

* Will present a alert window with a text field. The value that user inputs into the textfield will be attributed to the variable. In the above example, after the user enters a value and pressing 'Ok', userAge will be equal to whatever the user inputs.

## Converting values
* **String -> Number**
```javascript
parseInt('42') /** returns 42 */
```
* Strings that only have integers in them, such as '42', can be converted to a number using parseInt()


* **Number -> String**
```javascript
42.toString(); /** returns '42' */
```
* Numbers can be converted into strings using .toString()

## jQuery

```javascript
$(function() {
	/* When the page has finished loading, execute the code in this function */
})
```

* calls to jQuery functions can begin with either $ or jQuery

* works "cross-browser", though newer versions of jQuery will be dropping support for Internet Explorer 6 & 7

* Allows:
	* DOM traversal
	* CSS manipulation
	* Event handling
	* XHR requests
	* Animation
	* and more!

* **Selecting a DOM element**
	* By selector:
		```javascript
		$('p') /** will select all <p> elements on a page */
		```

	* By class:
		```javascript
		$('.foo') /** will select all elements with class set to 'foo' */
		```

	* By id:
		```javascript
		$('#foo') /** will select all elements with id set to foo */
		```


* **Change text**
	```javascript
	$('p').text('new text to display in all <p> elements')
	```

* **Update html**
	```javascript
	$('body').html('<div>this line replaces the body content with this div<div>')
	```

* **Change CSS**
	```javascript
	$('h1').css({
		color: 'red'
	});
	/* this will set the color of all h1s to red */
	```

* **Attach events to elements**
	```javascript
	$('h3').click(function(event) {
		$(this).hide();
	});
	/* When a h3 is click, it will get hidden */
	```
	* You can attach an event to one element and manipulate anything on the page within the callback function
	* If an element has a default event that gets executed on a specific event, such as how `<a>` tags will open a webpage when they are clicked, you can include event.preventDefault() within the callback function to disable that default behaviour.


## Tools & Tips
* **CDN** stands for Content Delivery Network, and is used to host and serve documents, most commonly JavaScript and CSS libraries

## Best Practices
* If you're working for company that does not want to use a CDN or you want the ability to develop offline, you can download and serve a JavaScript library from your web application, though it is best practice to use a CDN as the user will probably already have a cached copy of the files that are being served with your web application.