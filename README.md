<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>CarFixHelper</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #1a1a1a;
      color: white;
      text-align: center;
      padding: 40px;
    }

    h1 {
      color: #ff4d4d;
      font-size: 2.5em;
    }

    img.banner {
      width: 100%;
      max-height: 250px;
      object-fit: cover;
      border-radius: 10px;
      box-shadow: 0 4px 12px rgba(255, 77, 77, 0.6);
    }

    select, button {
      padding: 10px;
      font-size: 1em;
      margin-top: 20px;
      border: none;
      border-radius: 5px;
    }

    select {
      background-color: #333;
      color: white;
    }

    button {
      background-color: #ff4d4d;
      color: white;
      margin-left: 10px;
      cursor: pointer;
    }

    .footer {
      margin-top: 50px;
      font-size: 0.9em;
      color: #aaa;
    }
  </style>
</head>
<body>

  <h1>🚗 CarFixHelper</h1>
  <img src="https://upload.wikimedia.org/wikipedia/commons/0/0d/Nissan_GT-R_black.jpg" alt="Car Banner" class="banner" />

  <p>Welcome to CarFixHelper! Select your car problem to find step-by-step fixes and guides.</p>

  <label for="issueSelector">Choose an issue:</label>
  <select id="issueSelector">
    <option value="">-- Select a car issue --</option>
    <option value="engine.html">Engine Problems</option>
    <option value="brakes.html">Brake Issues</option>
    <option value="battery.html">Battery Troubles</option>
    <option value="transmission.html">Transmission Problems</option>
    <option value="ac.html">AC Not Working</option>
  </select>
  <button onclick="goToFix()">Fix It!</button>

  <script>
    function goToFix() {
      const page = document.getElementById("issueSelector").value;
      if (page) {
        window.location.href = page;
      } else {
        alert("Please select a car issue to fix.");
      }
    }
  </script>

  <div class="footer">
    &copy; 2025 CarFixHelper | Made for auto lovers by Atahan Ors
  </div>

</body>
</html>
