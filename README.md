<!DOCTYPE html>
<html>
<head>
  <title>Bootstrap Calculator</title>
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css">
  <style>
    .calculator {
      max-width: 300px;
      margin: 0 auto;
      margin-top: 100px;
    }
    .container1{
        background-color: black;
        border: red;
        border-radius: 5px;
    }
  </style>
</head>
<body>
   
  <div class="container calculator container1 p-2">
    <input type="text" id="display" class="form-control mb-3" readonly>

    <div class="row p-2">
      <div class="col">
        <button class="btn btn-primary btn-block" onclick="appendToDisplay(1)">1</button>
      </div>
      <div class="col">
        <button class="btn btn-primary btn-block" onclick="appendToDisplay(2)">2</button>
      </div>
      <div class="col">
        <button class="btn btn-primary btn-block" onclick="appendToDisplay(3)">3</button>
      </div>
    </div>

    <div class="row p-2 ">
      <div class="col">
        <button class="btn btn-primary btn-block" onclick="appendToDisplay(4)">4</button>
      </div>
      <div class="col">
        <button class="btn btn-primary btn-block" onclick="appendToDisplay(5)">5</button>
      </div>
      <div class="col">
        <button class="btn btn-primary btn-block" onclick="appendToDisplay(6)">6</button>
      </div>
    </div>

    <div class="row p-2">
      <div class="col">
        <button class="btn btn-primary btn-block" onclick="appendToDisplay(7)">7</button>
      </div>
      <div class="col">
        <button class="btn btn-primary btn-block" onclick="appendToDisplay(8)">8</button>
      </div>
      <div class="col">
        <button class="btn btn-primary btn-block" onclick="appendToDisplay(9)">9</button>
      </div>
    </div>

    <div class="row p-2">
      <div class="col">
        <button class="btn btn-primary btn-block" onclick="appendToDisplay(0)">0</button>
      </div>
      <div class="col">
        <button class="btn btn-danger btn-block" onclick="clearDisplay()">C</button>
      </div>
      <div class="col">
        <button class="btn btn-success btn-block" onclick="calculate()">=</button>
      </div>
    </div>

    <div class="row mt-3 p-2">
      <div class="col">
        <button class="btn btn-primary btn-block" onclick="appendToDisplay('+')">+</button>
      </div>
      <div class="col">
        <button class="btn btn-primary btn-block" onclick="appendToDisplay('-')">-</button>
      </div>
      <div class="col">
        <button class="btn btn-primary btn-block" onclick="appendToDisplay('*')">*</button>
      </div>
      <div class="col">
        <button class="btn btn-primary btn-block" onclick="appendToDisplay('/')">/</button>
      </div>
    </div>
  </div>
    </div>

  <script>
    function appendToDisplay(value) {
      document.getElementById('display').value += value;
    }

    function clearDisplay() {
      document.getElementById('display').value = '';
    }

    function calculate() {
      var displayValue = document.getElementById('display').value;
      var result = eval(displayValue);
      document.getElementById('display').value = result;
    }
  </script>
</body>
</html>
