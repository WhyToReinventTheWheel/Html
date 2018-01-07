https://www.w3schools.com/js/js_ajax_http.asp
Notes 

# AJAX is a developer's dream, because you can:
	* Read data from a web server - after the page has loaded
	* Update a web page without reloading the page
	* Send data to a web server - in the background

# XMLHttpRequest Object Methods
	Method						Description
	new XMLHttpRequest()		Creates a new XMLHttpRequest object
	abort()						Cancels the current request
	getAllResponseHeaders()		Returns header information
	getResponseHeader()			Returns specific header information
	open(method, url, async, user, psw)		Specifies the request
											method: the request type GET or POST
											url: the file location
											async: true (asynchronous) or false (synchronous)
											user: optional user name
											psw: optional password
	send()						Sends the request to the server,	Used for GET requests
	send(string)				Sends the request to the server.,	Used for POST requests
	setRequestHeader()			Adds a label/value pair to the header to be sent
	
# XMLHttpRequest Object Properties	
	Property				Description
	onreadystatechange		Defines a function to be called when the readyState property changes
	readyState				Holds the status of the XMLHttpRequest.
							0: request not initialized 
							1: server connection established
							2: request received 
							3: processing request 
							4: request finished and response is ready
	responseText			Returns the response data as a string
	responseXML				Returns the response data as XML data
	status					Returns the status-number of a request
							200: "OK"
							403: "Forbidden"
							404: "Not Found"
							For a complete list go to the Http Messages Reference
	statusText				Returns the status-text (e.g. "OK" or "Not Found")
	
# GetAjaxCall 
	 function getTest() {
		var xmlhttp = new XMLHttpRequest();
		xmlhttp.onreadystatechange = function() {
			if (this.readyState == 4 && this.status == 200) {
				var myObj = JSON.parse(this.responseText);
				document.getElementById("demo").innerHTML = myObj.content;
			}
		};
		xmlhttp.open("GET", "http://localhost:8080/greeting?name=User", true);
		xmlhttp.send();
	}
	
# Post Request 
	xhttp.open("POST", "ajax_test.asp", true);
	xhttp.setRequestHeader("Content-type", "application/x-www-form-urlencoded");
	xhttp.send("fname=Henry&lname=Ford");