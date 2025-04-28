<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8">
  <title>بررسی خاموشی برق</title>
  <style>
    body {
      text-align: center;
      font-family: sans-serif;
      direction: rtl;
      margin: 20px;
      background: #f9f9f9;
    }
    iframe {
      width: 90%;
      height: 600px;
      border: 1px solid #ccc;
      border-radius: 8px;
      margin-top: 20px;
      background: white;
    }
    .bill-list {
      margin-top: 20px;
    }
    .bill-list button, .back-button {
      margin: 5px;
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
      border: none;
      background-color: #4CAF50;
      color: white;
      border-radius: 5px;
      transition: background-color 0.3s;
    }
    .bill-list button:hover, .back-button:hover {
      background-color: #45a049;
    }
    footer {
      margin-top: 30px;
      font-size: 14px;
      color: #555;
    }
  </style>
</head>
<body>

  <h1>بررسی خاموشی برق (منزل و مغازه)</h1>

  <div class="bill-list">
    <p>روی شناسه کلیک کن تا کپی بشه:</p>
    <button onclick="copyToClipboard('6554770104324')">شناسه منزل: 6554770104324</button>
    <button onclick="copyToClipboard('6538373804322')">شناسه مغازه: 6538373804322</button>
    <br><br>
    <button class="back-button" onclick="goHome()">بازگشت به صفحه اصلی</button>
  </div>

  <iframe id="outageFrame" src="https://outage.aepdc.ir"></iframe>

  <footer>
    طراحی شده توسط <strong>مصطفی ماندگاری</strong> 🌟
  </footer>

  <script>
    function copyToClipboard(text) {
      navigator.clipboard.writeText(text)
        .then(() => alert('✅ شناسه کپی شد! حالا تو فرم سایت paste کن.'))
        .catch(err => alert('❌ خطا در کپی کردن.'));
    }

    function goHome() {
      document.getElementById('outageFrame').src = 'https://outage.aepdc.ir';
    }
  </script>

</body>
</html>
