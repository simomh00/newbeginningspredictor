# newbeginningspredictor<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>توقع رقم التعبئة</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            text-align: center;
            padding: 20px;
        }
        h1 {
            color: #333;
        }
        select, button {
            padding: 10px;
            margin: 10px;
            font-size: 16px;
            transition: background-color 0.3s, transform 0.3s;
        }
        button {
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
        }
        button:hover {
            background-color: #0056b3;
            transform: scale(1.05);
        }
        #result {
            margin-top: 20px;
            font-size: 24px;
            color: #007bff;
            opacity: 0; /* لجعل النص غير مرئي في البداية */
            transition: opacity 0.5s ease; /* تأثير الانتقال */
        }
    </style>
</head>
<body>
    <h1>توقع رقم التعبئة</h1>
    <p>اختر الشبكة أدناه:</p>
    <select id="network">
        <option value="orange">Orange</option>
        <option value="inwi">Inwi</option>
        <option value="teleMaroc">Télé Maroc</option>
    </select>
    <button onclick="generateCode()">توقع الرقم</button>

    <div id="result"></div>

    <script>
        function generateCode() {
            const network = document.getElementById("network").value;
            let predictedCode;

            // توليد رقم التعبئة المكون من 16 رقمًا بناءً على الشبكة المختارة
            if (network === "orange") {
                predictedCode = "orange-" + Math.floor(Math.random() * 10000000000000000); // 16 رقم لـ Orange
            } else if (network === "inwi") {
                predictedCode = "inwi-" + Math.floor(Math.random() * 10000000000000000); // 16 رقم لـ Inwi
            } else if (network === "teleMaroc") {
                predictedCode = "teleMaroc-" + Math.floor(Math.random() * 10000000000000000); // 16 رقم لـ Télé Maroc
            }

            // عرض الرقم المتوقع مع تأثير
            const resultDiv = document.getElementById("result");
            resultDiv.innerText = "رقم التعبئة المتوقع: " + predictedCode;
            resultDiv.style.opacity = 1; // جعل النص مرئي
        }
    </script>
</body>
</html>

رمز الأنترنيت
