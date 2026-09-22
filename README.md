# HTMLCSS
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>BMI 계산기</title>
</head>

<body>

    <h2>BMI 계산기</h2>

    <p>신장을 입력하세요(cm)</p>
    <input type="number" id="height">

    <p>체중을 입력하세요(kg)</p>
    <input type="number" id="weight">

    <button onclick="calculateBMI()">BMI 계산</button>

    <hr>

    <p>
        신장: <span id="resultHeight"></span>cm
    </p>

    <p>
        체중: <span id="resultWeight"></span>kg
    </p>

    <p>
        BMI: <span id="resultBMI"></span>
    </p>


    <script>
        function calculateBMI() {
            let height = document.getElementById("height").value;
            let weight = document.getElementById("weight").value;

            let heightMeter = height / 100;

            let bmi = weight / (heightMeter * heightMeter);

            document.getElementById("resultHeight").innerText = height;
            document.getElementById("resultWeight").innerText = weight;
            document.getElementById("resultBMI").innerText = bmi.toFixed(2);
        }
    </script>

</body>
</html>
