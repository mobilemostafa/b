
<html lang="fa">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>بررسی خاموشی برق</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: sans-serif;
      direction: rtl;
      background: #f0f2f5;
    }
    .header, .bill-list, .instructions, footer {
      padding: 10px;
      text-align: center;
    }
    .signature {
      font-size: 14px;
      color: #666;
      margin-bottom: 10px;
    }
    .bill-list {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      justify-content: center;
      align-items: center;
      margin-bottom: 10px;
    }
    .bill-list button {
      padding: 10px 18px;
      font-size: 16px;
      cursor: pointer;
      border: none;
      background-color: #4CAF50;
      color: white;
      border-radius: 5px;
      transition: 0.3s;
    }
    .bill-list button:hover {
      background-color: #45a049;
      transform: scale(1.05);
    }
    .back-button {
      background-color: #2196F3;
    }
    .back-button:hover {
      background-color: #1976D2;
    }
    .instructions {
      background: #fff3cd;
      padding: 8px 12px;
      border: 1px solid #ffeeba;
      border-radius: 5px;
      font-size: 15px;
      margin-bottom: 10px;
      box-shadow: 0 1px 4px rgba(0,0,0,0.1);
      max-width: 95%;
      margin: auto;
    }
    iframe {
      width: 100vw; /* تمام عرض صفحه */
      height: calc(100vh - 300px); /* ارتفاع با کم کردن ارتفاع بالایی */
      border: none;
      margin-top: 10px;
    }
    footer {
      font-size: 12px;
      color: #999;
      margin-top: 10px;
    }
    @media (max-width: 768px) {
      .bill-list button {
        width: 100%;
      }
      iframe {
        height: calc(100vh - 400px);
      }
    }
  </style>
</head>
<body>

  <div class="header">
    <h1>بررسی خاموشی برق (منزل و مغازه)</h1>
    <div class="signature">ساخته شده توسط <strong>مصطفی ماندگاری</strong> 🌟</div>
  </div>

  <div class="bill-list">
    <button onclick="copyToClipboard('6554770104324')">شناسه منزل</button>
    <button onclick="copyToClipboard('6538373804322')">شناسه مغازه</button>
    <button class="back-button" onclick="goHome()">بازگشت</button>
  </div>

  <div class="instructions">
    🔹 روی یکی از دکمه‌های شناسه کلیک کنید تا کپی شود.<br>
    🔹 سپس داخل سایت، جلوی دکمه "بررسی"، Paste کنید و دکمه بررسی را بزنید.
  </div>

  <iframe id="outageFrame" src="https://outage.aepdc.ir"></iframe>

  <footer>
    © طراحی و توسعه توسط مصطفی ماندگاری
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
