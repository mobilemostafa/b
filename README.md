
<html lang="fa">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- این خط برای ریسپانسیو بودن صفحه ضروریه -->
  <title>بررسی خاموشی برق</title>
  <style>
    body {
      text-align: center;
      font-family: sans-serif;
      direction: rtl;
      margin: 20px;
      background: #f0f2f5;
    }
    iframe {
      width: 100%; /* عرض iframe 100% از صفحه نمایش */
      height: 600px;
      border: 1px solid #ccc;
      border-radius: 8px;
      margin-top: 20px;
      background: white;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      overflow: hidden;
    }
    .header {
      margin-bottom: 10px;
    }
    .signature {
      font-size: 14px;
      color: #666;
      margin-bottom: 20px;
    }
    .bill-list {
      margin-top: 10px;
      display: flex;
      justify-content: center;
      gap: 10px;
      flex-wrap: wrap;
      align-items: center;
      flex-direction: column; /* در موبایل دکمه‌ها زیر هم قرار می‌گیرند */
    }
    .bill-list button {
      padding: 10px 18px;
      font-size: 16px;
      cursor: pointer;
      border: none;
      background-color: #4CAF50;
      color: white;
      border-radius: 5px;
      transition: background-color 0.3s, transform 0.2s;
    }
    .bill-list button:hover {
      background-color: #45a049;
      transform: scale(1.05);
    }
    .back-button {
      padding: 8px 14px;
      font-size: 14px;
      background-color: #2196F3;
    }
    .back-button:hover {
      background-color: #1976D2;
    }
    .instructions {
      font-size: 15px;
      color: #333;
      margin-top: 15px;
      background: #fff3cd;
      padding: 10px 15px;
      border: 1px solid #ffeeba;
      border-radius: 5px;
      display: inline-block;
      max-width: 80%;
      box-shadow: 0 1px 4px rgba(0,0,0,0.1);
    }
    footer {
      margin-top: 30px;
      font-size: 12px;
      color: #999;
    }

    /* Media query برای صفحات کوچک (مثل موبایل) */
    @media only screen and (max-width: 768px) {
      iframe {
        height: 400px; /* اندازه iframe در موبایل کمتر میشه */
      }
      .bill-list button {
        width: 100%; /* دکمه‌ها در موبایل تمام عرض صفحه رو می‌گیرن */
      }
    }
  </style>
</head>
<body>

  <div class="header">
    <h1>بررسی خاموشی برق (منزل و مغازه)</h1>
    <div class="signature">طراحی شده توسط <strong>مصطفی ماندگاری</strong> 🌟</div>
  </div>

  <div class="bill-list">
    <button onclick="copyToClipboard('6554770104324')">شناسه منزل</button>
    <button onclick="copyToClipboard('6538373804322')">شناسه مغازه</button>
    <button class="back-button" onclick="goHome()">بازگشت</button>
  </div>

  <div class="instructions">
    🔹 روی یکی از دکمه‌های شناسه کلیک کنید تا شناسه برق کپی شود.<br>
    🔹 سپس در سایت، جلوی دکمه "بررسی"، شناسه را Paste کنید.
  </div>

  <iframe id="outageFrame" src="https://outage.aepdc.ir"></iframe>

  <footer>
    © تمام حقوق محفوظ است.
  </footer>

  <script>
    function copyToClipboard(text) {
      navigator.clipboard.writeText(text)
        .then(() => alert('✅ شناسه کپی شد! حالا در فرم سایت Paste کن.'))
        .catch(err => alert('❌ خطا در کپی کردن.'));
    }

    function goHome() {
      document.getElementById('outageFrame').src = 'https://outage.aepdc.ir';
    }
  </script>

</body>
</html>
