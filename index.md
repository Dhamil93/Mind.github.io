<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Number Guessing Game</title>

	<style>
		html {
	font-family: sans-serif;
	}
    p   {
        font-weight: bolder;
    }
    .about-section {
            padding: 70px;
            text-align: center;
            background-color: rgb(181, 202, 61);
            color: rgb(185, 203, 226);
        }
        .about-section h1 {
            font-weight: bolder;
            color: azure;
            }
            .about-section p {
                font-weight: bolder;
                color: azure;
            }

        .about-section a:link {
            text-decoration: none;
            cursor: grab;
        }

        .about-section a:any-link {
            color: red;
            font-size: larger;
        }

		body {
	width: 50%;
	max-width: 800px;
	min-width: 480px;
	margin: 0 auto;
	background-color: rgb(25, 54, 54);
	}
	h1	{
		text-align: center;
		color: Yellow;
	}
	.form {
		color: Yellow;
	}
	</style>
</head>

<body>
    <div class="about-section">
        <h1>WELCOME</h1>
        <p>Atilola Damilare Ezekiel welcome you to a challenge</p>
        <a href="contact.html">Home Page</a>
        </div>


<h1>Guess The Number</h1>

<p>We have selected a random number between 1 - 10.
See if you can guess it. Cheers!!!</p>

<div class="form">
	<label for="guessField">Enter a guess: </label>
	<input type = "text" id = "guessField" class = "guessField">
	<input type = "submit" value = "Submit guess"
		class = "guessSubmit" id = "submitguess">
</div>

<script type = "text/javascript">

	// random value generated
	var y = Math.floor(Math.random() * 10 + 1);

	// counting the number of guesses
	// made for correct Guess
	var guess = 1;

	document.getElementById("submitguess").onclick = function(){

// number guessed by user
var x = document.getElementById("guessField").value;

if(x == y)
{
	alert("CONGRATULATIONS!!! YOU GUESSED IT RIGHT IN "
			+ guess + " GUESS ");
}
else if(x > y) /* if guessed number is greater
				than actual number*/
{
	guess++;
	alert("OOPS SORRY!! TRY A SMALLER NUMBER");
}
else
{
	guess++;
	alert("OOPS SORRY!! TRY A GREATER NUMBER")
}
}
</script>
</body>
</html>
