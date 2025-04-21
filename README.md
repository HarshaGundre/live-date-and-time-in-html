<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Live Date and Time</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding-top: 50px;
      background-color: #f0f0f0;
    }
    #clock {
      font-size: 2em;
      color: #333;
      background: #fff;
      padding: 20px;
      border-radius: 10px;
      display: inline-block;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }
  </style>
</head>
<body>

  <div id="clock">Loading time...</div>

  <script>
    function updateTime() {
      const now = new Date();
      const formatted = now.toLocaleString();
      document.getElementById('clock').textContent = formatted;
    }

    // Update immediately and then every second
    updateTime();
    setInterval(updateTime, 1000);
  </script>

</body>
</html>
