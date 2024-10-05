<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Phép tính cơ bản</title>
</head>
<body>
    <h1>Thực hiện 4 phép tính: Cộng, Trừ, Nhân, Chia</h1>
    <form name="calculator">
        <input type="number" id="num1">
        <select id="operator">
            <option value="+">+</option>
            <option value="-">-</option>
            <option value="*">*</option>
            <option value="/">/</option>
        </select>
        <input type="number" id="num2">
        <button type="button" onclick="calculate()">=</button>
        <input type="text" id="result" readonly>
    </form>

    <script>
        function calculate() {
            var num1 = parseFloat(document.getElementById('num1').value);
            var operator = document.getElementById('operator').value;
            var num2 = parseFloat(document.getElementById('num2').value);
            var result = 0;

            if (operator == '+') {
                result = num1 + num2;
            } else if (operator == '-') {
                result = num1 - num2;
            } else if (operator == '*') {
                result = num1 * num2;
            } else if (operator == '/') {
                result = num1 / num2;
            }
            document.getElementById('result').value = result;
        }
    </script>
</body>
</html>
