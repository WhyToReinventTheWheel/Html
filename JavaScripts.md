https://www.w3schools.com/js/js_json_intro.asp
Notes 

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
	
# Objects
	A JavaScript object is a collection of named values
	* var car = {type:"Fiat", model:"500", color:"white"};
		objectName.propertyName or 	objectName["propertyName"]
		car.type  or car["Fiat"]
	* Object Method
		objectName.methodName()
		var person = {
			firstName: "John",
			lastName : "Doe",
			id       : 5566,
			fullName : function() {
			   return this.firstName + " " + this.lastName;
			}
		};
		document.getElementById("demo").innerHTML = person.fullName();
	* var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"}
		var x = person;  // This will not create a copy of person.
		x.age = 10;      // This will change both x.age and person.age
		delete person.age;   // or delete person["age"]; 
# Function
	function myFunction(p1, p2) {
		return p1 * p2;              // The function returns the product of p1 and p2
	}
	
# Events
	onchange:	An HTML element has been changed
	onclick: 	The user clicks an HTML element
	onmouseover:	The user moves the mouse over an HTML element
	onmouseout:	The user moves the mouse away from an HTML element
	onkeydown:	The user pushes a keyboard key
	onload:		The browser has finished loading the page
	
# Switch 
	It is a common mistake to forget that switch statements use strict comparison:
	
	var x = 10;
	switch(x) {
		case 10: alert("Hello");    // This will execute 
	} 
	
	var x = 10;
	switch(x) {
		case "10": alert("Hello"); // This will not execute 
	}
	
# For
	var cars = ["BMW", "Volvo", "Saab", "Ford", "Fiat", "Audi"];
	var text = "";
	var i;
	for (i = 0; i < cars.length; i++) {
		text += cars[i] + "<br>";
	}
	
# JSON Text to a JavaScript Object
	<script>
		var text = '{"employees":[' +
		'{"firstName":"John","lastName":"Doe" },' +
		'{"firstName":"Anna","lastName":"Smith" },' +
		'{"firstName":"Peter","lastName":"Jones" }]}';

		Since the JSON format is text only, it can easily be sent to and from a server, 
		and used as a data format by any programming language.
		var obj = JSON.parse(text);
		document.getElementById("demo").innerHTML =
		obj.employees[1].firstName + " " + obj.employees[1].lastName;
		
		var myJSON = JSON.stringify(obj);
	</script>

# JSON is Like XML Because
	Both JSON and XML are "self describing" (human readable)
	Both JSON and XML are hierarchical (values within values)
	Both JSON and XML can be parsed and used by lots of programming languages
	Both JSON and XML can be fetched with an XMLHttpRequest

# JSON is Unlike XML Because
	JSON doesn't use end tag
	JSON is shorter
	JSON is quicker to read and write
	JSON can use arrays
	The biggest difference is:

	XML has to be parsed with an XML parser. JSON can be parsed by a standard JavaScript function.

# Why JSON is Better Than XML
	XML is much more difficult to parse than JSON.
	JSON is parsed into a ready-to-use JavaScript object.
	For AJAX applications, JSON is faster and easier than XML:
	Using XML
		Fetch an XML document
		Use the XML DOM to loop through the document
		Extract values and store in variables
	Using JSON
		Fetch a JSON string
		JSON.Parse the JSON string
		
