# saferoute-AI
SafeRoute AI is an accident prevention and route safety awareness platform designed to analyze travel conditions and predict potential accident risk levels.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>SafeRoute AI</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background: #f4f6f8;
    }

    header {
      background: #1a73e8;
      color: white;
      padding: 20px;
      text-align: center;
    }

    .card {
      background: white;
      margin: 20px auto;
      padding: 20px;
      border-radius: 8px;
      max-width: 900px;
    }

    iframe {
      width: 100%;
      height: 400px;
      border: none;
      border-radius: 8px;
    }

    .risk {
      font-size: 22px;
      font-weight: bold;
    }

    .high { color: red; }
    .medium { color: orange; }
    .low { color: green; }

    button {
      padding: 10px 16px;
      font-size: 16px;
      background: #1a73e8;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>

<body>

<header>
  <h1>SafeRoute AI</h1>
  <p>AI-Powered Accident Prevention Platform</p>
</header>

<div class="card">
  <h2>Accident Hotspot Map</h2>

  <iframe
    src="https://maps.google.com/maps?q=ccsu%20meerut&z=14&output=embed">
  </iframe>
</div>

<div class="card">
  <h2>AI Risk Prediction</h2>

  <p class="risk">
    Risk Level:
    <span id="riskText">NOT CALCULATED</span>
  </p>

  <p id="riskDesc"></p>

  <button id="predictBtn">Run AI Prediction</button>
</div>

<script>
  document.getElementById("predictBtn").addEventListener("click", function () {

    var riskScore = Math.random(); // Simulated AI output

    var riskText = document.getElementById("riskText");
    var riskDesc = document.getElementById("riskDesc");

    if (riskScore > 0.7) {
      riskText.textContent = "HIGH";
      riskText.className = "high";
      riskDesc.textContent =
        "High accident probability. Avoid this route or drive carefully.";
    }
    else if (riskScore > 0.4) {
      riskText.textContent = "MEDIUM";
      riskText.className = "medium";
      riskDesc.textContent =
        "Moderate risk detected. Maintain safe driving practices.";
    }
    else {
      riskText.textContent = "LOW";
      riskText.className = "low";
      riskDesc.textContent =
        "Low risk area. Route is relatively safe.";
    }

  });
</script>

</body>
</html>
