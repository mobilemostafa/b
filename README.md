
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
    .header, .bill-list, .note, footer {
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
      margin-bottom: 5px;
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
    .note {
      font-size: 14px;
      color: #555;
      background-color: #fff3cd;
      border: 1px solid #ffeeba;
      border-radius: 5px;
      margin: 0 auto 10px auto;
      max-width: 95%;
    }
    iframe {
      width: 100vw;
      height: calc(100vh - 250px);
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
        height: calc(100vh - 290px);
      }
    }
  </style>
</head>
<body>

  <div class="header">
    <div class="signature">ساخته شده توسط <strong>مصطفی ماندگاری</strong> 🌟</div>
  </div>

  <div class="bill-list">
    <button onclick="copyAndRefresh('6554770104324')">شناسه منزل (6554770104324)</button>
    <button onclick="copyAndRefresh('6538373804322')">شناسه مغازه (6538373804322)</button>
  </div>

  <div class="note">
    با زدن دکمه، شناسه به‌صورت خودکار در حافظه کپی می‌شود. آن را در کادر جستجوی سایت جای‌گذاری کرده و روی دکمه بررسی کلیک کنید.
  </div>

  <iframe id="outageFrame" src="https://outage.aepdc.ir"></iframe>

  <footer>
    © طراحی و توسعه توسط مصطفی ماندگاری
  </footer>

  <script>
    function copyAndRefresh(text) {
      navigator.clipboard.writeText(text).then(() => {
        document.getElementById('outageFrame').src = 'https://outage.aepdc.ir';
      });
    }
  </script>

</body>
</html>
