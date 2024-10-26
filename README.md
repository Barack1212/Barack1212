<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CALCULATOR</title>
    <link rel="stylesheet" href="style.CSS" />
    <style>
      

body{
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: hsl(0, 0%, 95%);
}

#calculator{
    font-family: Arial,sans-serif;
    background-color: hsl(0, 0%, 15%);
    border-radius: 15px;
    max-width: 500px;
    overflow: hidden;
}
#display{
    width: 100%;
    padding: 20px;
    font-size: 5rem;
    text-align: left;
    border: none;
    background-color: hsl(0, 0%, 20%);
    color: white;
}
#keys{
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
    padding: 25px;
}

button{
    width: 100px;
    height: 100px;
    border-radius: 50px;
    border: none;
    background-color: hsl(0, 0%, 30%);
    color: white;
    font-size: 3rem;
    font-weight: bold;
    cursor: pointer;
}
button:hover{
    background-color: hsl(0, 1%, 40%);
}
button:active{
    background-color: hsl(0, 0%, 50%);
}
.operator-btn{
    background-color: hsl(53, 69%, 49%);
}
.operator-btn:hover{
    background-color: hsl(69, 92%, 64%);
}
.operator-btn:active{
    background-color: hsl(35, 82%, 68%);
}
    </style>
  </head>
  <body>
    <div id="calculator">
      <input id="display" readonly />
      <div id="keys">
        <button onclick="appendToDisplay('+')" class="operator-btn">+</button>
        <button onclick="appendToDisplay('7')">7</button>
        <button onclick="appendToDisplay('8')">8</button>
        <button onclick="appendToDisplay('9')">9</button>
        <button onclick="appendToDisplay('-')" class="operator-btn">-</button>
        <button onclick="appendToDisplay('4')">4</button>
        <button onclick="appendToDisplay('5')">5</button>
        <button onclick="appendToDisplay('6')">6</button>
        <button onclick="appendToDisplay('*')" class="operator-btn">*</button>
        <button onclick="appendToDisplay('1')">1</button>
        <button onclick="appendToDisplay('2')">2</button>
        <button onclick="appendToDisplay('3')">3</button>
        <button onclick="appendToDisplay('/')" class="operator-btn">/</button>
        <button onclick="appendToDisplay('0')">0</button>
        <button onclick="appendToDisplay('.')">.</button>
        <button onclick="calculate()">=</button>
        <button onclick="clearDisplay()" class="operator-btn">C</button>
      </div>
    </div>
    <script src="hello.js"></script>
    <script>// CALCULATOR PROGRAM

const display = document.getElementById("display");

function appendToDisplay(input) {
  display.value += input;
}

function clearDisplay() {
  display.value = "";
}

function calculate() {
  try {
    display.value = eval(display.value);
  } catch (error) {
    display.value = "error";
  }
}
</script>
  </body>
</html>
