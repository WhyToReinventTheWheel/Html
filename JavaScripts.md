# JavaScripts 
	document.getElementById("demo").innerHTML = "Hello JavaScript";
	document.getElementById('demo').innerHTML = 'Hello JavaScript';
	document.getElementById("demo").style.fontSize = "35px";
	
	//Hide HTML Tag
		<p id="demo">JavaScript can hide HTML elements.</p>
		<button type="button" onclick="document.getElementById('demo').style.display='none'">Click Me!</button>
	//Show HTML Tag
		<p id="demo" style="display:none">Hello JavaScript!</p>
		<button type="button" onclick="document.getElementById('demo').style.display='block'">Click Me!</button>
	//
# <script> Tag
	JavaScript in <head> or <body>
	<head>
		<script>
			function myFunction() {
				document.getElementById("demo").innerHTML = "Paragraph changed.";
			}
		</script>
	</head>
	
# External JavaScript
		<script src="myScript.js"></script>
		<script src="/js/myScript1.js"></script>
# Alert
	<script> window.alert(5 + 6);	</script>
# Console
	<script> console.log(5 + 6); </script>
	
# Variable
	var x, y;
	x = 5 + 6;
	y = x * 10;
	
	The identity (===) operator behaves identically to the equality (==) operator except 
	no type conversion is done, and the types must be the same to be considered equal.
	
	var x = 2 + 3 + "5";
	console.log(typeof(x));  //string
	isNaN(x);				// false
	
	var x = 2 + "A" + "5" ;
	console.log(typeof(x));  //string
	isNaN(x); 				// true

# Undefined
	A variable without a value, has the value undefined. The typeof is also undefined.
	var car;                // Value is undefined, type is undefined
# Null
	var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
	person = null;        // Now value is null, but type is still an object

# Difference Between Undefined and Null
	typeof undefined           // undefined
	typeof null                // object

	null === undefined         // false
	null == undefined          // true
	
# Primitive Data
	string
	number
	boolean
	undefined

	var length = 16;                               // Number
	var lastName = "Johnson";                      // String
	var x = {firstName:"John", lastName:"Doe"};    // Object
	* JavaScript evaluates expressions from left to right. Different sequences can produce different results:
		var x = 16 + 4 + "Volvo";    ==> 20Volvo   //JavaScript treats 16 and 4 as numbers, until it reaches "Volvo".
		var x = "Volvo" + 16 + 4;    ==> Volvo164  //first operand is a string, all operands are treated as strings.
		
	* JavaScript Types are Dynamic.
		var x;               // Now x is undefined
		var x = 5;           // Now x is a Number
		var x = "John";      // Now x is a String
		
# Complex Data
	function
	object
	
	typeof {name:'John', age:34} // Returns "object"
	typeof [1,2,3,4]             // Returns "object" //The typeof operator returns "object" for arrays because in JavaScript arrays are objects.
	typeof null                  // Returns "object"
	typeof function myFunc(){}   // Returns "function"