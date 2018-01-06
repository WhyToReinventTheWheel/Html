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
	
	