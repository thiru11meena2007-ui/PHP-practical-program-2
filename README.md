# PHP-practical-program-2

<!DOCTYPE html>
<html>
<head>
    <title>Simple Calculator</title>
</head>
<body>

<h2>Simple Calculator</h2>

<form method="post">
    Number 1:
    <input type="number" name="num1" required><br><br>

    Number 2:
    <input type="number" name="num2" required><br><br>

    <input type="submit" name="calculate" value="Calculate">
</form>

<?php
if (isset($_POST['calculate'])) {

    $num1 = $_POST['num1'];
    $num2 = $_POST['num2'];

    echo "<h3>Output</h3>";

    echo "Sum = " . ($num1 + $num2) . "<br>";
    echo "Difference = " . ($num1 - $num2) . "<br>";
    echo "Product = " . ($num1 * $num2) . "<br>";

    if ($num2 != 0) {
        echo "Quotient = " . ($num1 / $num2);
    } else {
        echo "Quotient = Cannot divide by zero";
    }
}
?>

</body>
</html>


Input
Number 1: 20
Number 2: 5

Output
Sum = 25
Difference = 15
Product = 100
Quotient = 4
