<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>บันทึกการออกกำลังกาย 1 สัปดาห์</title>
    <style>
        body {
            background-color: pink;
            font-family: Arial, sans-serif;
            padding: 20px;
        }
        h1 {
            text-align: center;
            color: white;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .exercise-log {
            margin-bottom: 20px;
        }
        label {
            display: block;
            margin: 10px 0 5px;
        }
        input {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .result {
            font-size: 18px;
            color: green;
            font-weight: bold;
        }
        .btn {
            background-color: #ff66b2;
            color: white;
            padding: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            width: 100%;
        }
        .btn:hover {
            background-color: #ff3385;
        }
    </style>
</head>
<body>

    <h1>บันทึกการออกกำลังกาย 1 สัปดาห์</h1>

    <div class="container">
        <div class="exercise-log">
            <label for="exercise-time">กรุณากรอกระยะเวลาการออกกำลังกายในแต่ละวัน (เป็นนาที):</label>
            <input type="number" id="exercise-time" placeholder="กรุณากรอกจำนวนระยะเวลา (นาที)" required>
        </div>

        <button class="btn" onclick="checkExercise()">แสดงผล</button>

        <div id="result" class="result"></div>
    </div>

    <script>
        function checkExercise() {
            const time = parseInt(document.getElementById('exercise-time').value);
            let result = '';

            if (isNaN(time) || time <= 0) {
                result = 'กรุณากรอกระยะเวลาออกกำลังกายที่ถูกต้อง!';
            } else if (time >= 10 && time <= 30) {
                result = 'การออกกำลังกายของคุณ: ดี';
            } else if (time >= 30 && time <= 60) {
                result = 'การออกกำลังกายของคุณ: ดีเยี่ยม';
            } else {
                result = 'ระยะเวลาออกกำลังกายเกินกำหนด! กรุณากรอกเวลา 1-60 นาที';
            }

            document.getElementById('result').innerText = result;
        }
    </script>

</body>
</html>