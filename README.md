# <!DOCTYPE html>
<html>

<body>

<h2>BMI 계산기</h2>

신장(cm):
<input id="height">

<br><br>

체중(kg):
<input id="weight">

<br><br>

<button onclick="calc()">계산</button>

<p>BMI: <span id="result"></span></p>

<script>
function calc() {
    let h = document.getElementById("height").value / 100;
    let w = document.getElementById("weight").value;

    let bmi = w / (h * h);

    document.getElementById("result").innerText = bmi.toFixed(2);
}
</script>

</body>

</html>
