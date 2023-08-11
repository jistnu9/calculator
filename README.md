<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Basic Calculator</title>
<style>
  body {
    font-family: Arial, sans-serif;
  }
  #calculator {
    width: 300px;
    margin: 0 auto;
    border: 1px solid #ccc;
    padding: 10px;
    text-align: center;
  }
  .button {
    width: 60px;
    height: 60px;
    font-size: 20px;
    margin: 5px;
    cursor: pointer;
  }
</style>
</head>
<body>
<div id="calculator">
  <input type="text" id="display" readonly>
  <br>
  <button class="button" onclick="appendToDisplay('1')">1</button>
  <button class="button" onclick="appendToDisplay('2')">2</button>
  <button class="button" onclick="appendToDisplay('3')">3</button>
  <button class="button" onclick="appendToDisplay('+')">+</button>
  <br>
  <button class="button" onclick="appendToDisplay('4')">4</button>
  <button class="button" onclick="appendToDisplay('5')">5</button>
  <button class="button" onclick="appendToDisplay('6')">6</button>
  <button class="button" onclick="appendToDisplay('-')">-</button>
  <br>
  <button class="button" onclick="appendToDisplay('7')">7</button>
  <button class="button" onclick="appendToDisplay('8')">8</button>
  <button class="button" onclick="appendToDisplay('9')">9</button>
  <button class="button" onclick="appendToDisplay('*')">*</button>
  <br>
  <button class="button" onclick="appendToDisplay('0')">0</button>
  <button class="button" onclick="clearDisplay()">C</button>
  <button class="button" onclick="calculate()">=</button>
  <button class="button" onclick="appendToDisplay('/')">/</button>
</div>

<script>
  const display = document.getElementById('display');

  function appendToDisplay(value) {
    display.value += value;
  }

  function clearDisplay() {
    display.value = '';
  }

  function calculate() {
    try {
      display.value = eval(display.value);
    } catch (error) {
      display.value = 'Error';
    }
  }
</script>
</body>
</html>
