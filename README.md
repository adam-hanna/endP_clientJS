# EndPoint.io client js library
Use this library to simplify the process of submitting forms to the endpoint form submission api.

## Instructions
In order to use, please include the minified js file which can be found at `/source/min/endP.min.js`.

```html
	<!DOCTYPE html>
	<html>
		<body>
			<form id="myForm" onSubmit="endP_formSubmit(event, success, error, complete)">
				<input name="ajax" value="true" hidden />
				<input name="form-id" value="3" hidden />
				<input type="radio" name="gender" value="male" checked /> Male<br>
				<input type="radio" name="gender" value="female" /> Female<br>
				<input type="radio" name="gender" value="other" /> Other<br>
				<input type="text" name="name" placeholder="Your Name" /><br>
				<select name="food">
					<option value="meat" selected>Meat</option>
					<option value="chicken">Chicken</option>
				</select><br>
				<textarea name="comment" placeholder="Your Comment"></textarea><br>
				<input type="submit" value="Submit">
			</form>
			<!-- note: you need to place this minified js file on your server and point to it -->
			<script type="text/javascript" src="/js/lib/endP.min.js"></script>
			<script type="text/javascript">
				var success = function(data, event) {
					alert("success");
					console.log(data, event);
				};
				var error = function(jqXHR, textStatus, errorThrown, event) {
					alert("error");
					console.log(jqXHR, textStatus, errorThrown, event);
				};
				var complete = function(jqXHR, textStatus, event) {
					alert("complete");
					console.log(jqXHR, textStatus, event);
				};
			</script>
		</body>
	</html>
```

## Example
See the example folder for a very simple example. Note: in order for this to work on your site, please change the source of the js file to wherever you've placed it on your server.


## LICENSE
MIT