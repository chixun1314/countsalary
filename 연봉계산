<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>실지급 연봉 및 월급 계산기</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin: 20px; }
        .container { max-width: 400px; margin: auto; padding: 20px; border: 1px solid #ddd; border-radius: 10px; }
        input, button { width: 100%; padding: 10px; margin: 5px 0; }
        .result { font-weight: bold; margin-top: 10px; }
    </style>
</head>
<body>
    <div class="container">
        <h2>연봉 실지급액 계산기</h2>
        <label for="salary">연봉 입력 (만원):</label>
        <input type="number" id="salary" placeholder="예: 5000" oninput="calculateSalary()">
        <div class="result" id="result"></div>
    </div>

    <script>
        function calculateSalary() {
            let annualSalary = parseInt(document.getElementById('salary').value) * 10000;
            if (isNaN(annualSalary) || annualSalary <= 0) {
                document.getElementById('result').innerHTML = "올바른 연봉을 입력하세요.";
                return;
            }
            
            // 대략적인 공제 비율 (예: 4대보험 약 9%, 소득세+지방세 약 6%)
            let insurance = annualSalary * 0.09;
            let tax = annualSalary * 0.06;
            let totalDeductions = insurance + tax;
            let netAnnualSalary = annualSalary - totalDeductions;
            let netMonthlySalary = netAnnualSalary / 12;
            
            document.getElementById('result').innerHTML = `
                <p>실지급 연봉: <span style="color:blue;">${netAnnualSalary.toLocaleString()} 원</span></p>
                <p>실지급 월급: <span style="color:blue;">${Math.floor(netMonthlySalary).toLocaleString()} 원</span></p>
            `;
        }
    </script>
</body>
</html>
