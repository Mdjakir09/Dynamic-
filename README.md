# Dynamic-
It's A Dynamic game
<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8">
  <title>Spin & Win - ভাগ্য চাকা ঘোরাও</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      text-align: center;
      font-family: Arial, sans-serif;
      background: linear-gradient(to right, #fdfbfb, #ebedee);
      padding: 40px;
    }
    h1 {
      color: #333;
      margin-bottom: 20px;
    }
    #wheel {
      width: 300px;
      height: 300px;
      border-radius: 50%;
      border: 10px solid #ff9800;
      margin: 30px auto;
      background: conic-gradient(
        #f44336 0deg 60deg,
        #2196f3 60deg 120deg,
        #4caf50 120deg 180deg,
        #ffeb3b 180deg 240deg,
        #9c27b0 240deg 300deg,
        #00bcd4 300deg 360deg
      );
      transition: transform 4s ease-out;
    }
    button {
      padding: 15px 30px;
      font-size: 18px;
      background: #4caf50;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
    #result {
      margin-top: 20px;
      font-size: 20px;
      color: #222;
    }
  </style>
</head>
<body>

  <h1>🎯 Spin & Win 🎁</h1>
  <div id="wheel"></div>
  <button onclick="spin()">চাকা ঘোরাও</button>
  <p id="result"></p>

  <script>
    function spin() {
      const wheel = document.getElementById('wheel');
      const result = document.getElementById('result');
      const degree = 3600 + Math.floor(Math.random() * 360);
      wheel.style.transform = `rotate(${degree}deg)`;

      const segments = [
        "৫০ টাকা ক্যাশব্যাক", "১ GB ফ্রি ইন্টারনেট", 
        "ধন্যবাদ!", "১০০ টাকা ক্যাশ ইন", 
        "১ দিনের ফ্রি মুভি সাবস্ক্রিপশন", "পুনরায় চেষ্টা করুন"
      ];

      setTimeout(() => {
        const index = Math.floor((degree % 360) / 60);
        result.innerText = "🎉 আপনি জিতেছেন: " + segments[index];
      }, 4000);
    }
  </script>

</body>
</html>
