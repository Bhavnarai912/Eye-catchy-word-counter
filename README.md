# Eye-catchy-word-counter
<!DOCTYPE html>
<html>

<body style="text-align: center;">

	<h1 style="color: green">
		GeeksforGeeks
	</h1>

	
<p>
		Type in the textbox and click on
		the button to count the words
	</p>



	<textarea id="inputField" rows=10 cols="60">
	</textarea>
	<br><br>

	<button onclick="countWords()">
		Count Words
	</button>
	<br><br>

	
<p> Word Count:
		<span id="show">0</span>
	</p>



	<script>
		function countWords() {

			// Get the input text value
			var text = document
				.getElementById("inputField").value;

			// Initialize the word counter
			var numWords = 0;

			// Loop through the text
			// and count spaces in it
			for (var i = 0; i < text.length; i++) {
				var currentCharacter = text[i];

				// Check if the character is a space
				if (currentCharacter == " ") {
					numWords += 1;
				}
			}

			// Add 1 to make the count equal to
			// the number of words
			// (count of words = count of spaces + 1)
			numWords += 1;

			// Display it as output
			document.getElementById("show")
				.innerHTML = numWords;
		}
	</script>
</body>

</html>
