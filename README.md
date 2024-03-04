!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
   <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        .calculator {
            width: 350px;
            margin: 0 auto;
            padding: 27px;
            border: 5px solid #808080;
            border-radius:25px;
        }
        .calculator input[type="text"] {
            width: 100%;
            margin-bottom: 10px;
            padding:8px;
            font-size:35px;
            border-radius:20px;
        }
        .calculator input[type="button"] {
            width: 32%;
            padding: 15px;
            font-size: 20px;
            margin-bottom: 6px;
            border: 3px solid #0000FF;
            border-radius: 5px;
            cursor: pointer;
        }
        .calculator input[type="button"]:hover {
            background-color: #00FFFF;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" readonly>
        <input type="button" value="1" onclick="addToDisplay('1')">
        <input type="button" value="2" onclick="addToDisplay('2')">
        <input type="button" value="+" onclick="addToDisplay('+')">
        <input type="button" value="3" onclick="addToDisplay('3')">
        <input type="button" value="4" onclick="addToDisplay('4')">
        <input type="button" value="-" onclick="addToDisplay('-')">
        <input type="button" value="5" onclick="addToDisplay('5')">
        <input type="button" value="6" onclick="addToDisplay('6')">
        <input type="button" value="*" onclick="addToDisplay('*')">
        <input type="button" value="7" onclick="addToDisplay('7')">
        <input type="button" value="8" onclick="addToDisplay('8')">
        <input type="button" value="/" onclick="addToDisplay('/')">
        <input type="button" value="9" onclick="addToDisplay('9')">
		<input type="button" value="0" onclick="addToDisplay('0')">
        <input type="button" value="=" onclick="calculate()">
		<input type="button" value="." onclick="addToDisplay('.')">
		<input type="button" value="C" onclick="clearDisplay()">
		
	
    </div>

    <script>
        function addToDisplay(value) {
            document.getElementById('display').value += value;
        }

        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function calculate() {
            var expression = document.getElementById('display').value;
            try {
                var result = eval(expression);
                document.getElementById('display').value = result;
            } catch (error) {
                document.getElementById('display').value = 'Error';
            }
        }
    </script>
</body>
</html>
