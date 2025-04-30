<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>CarFixHelper</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #1a1a1a;
      color: #f4f4f4;
      text-align: center;
      padding: 40px;
    }

    h1 {
      color: #ff3c00;
      font-size: 3em;
    }

    .car-image {
      width: 90%;
      max-width: 600px;
      border-radius: 10px;
      margin-top: 20px;
    }

    .form-section {
      margin-top: 40px;
    }

    select, button {
      padding: 12px;
      font-size: 1em;
      margin: 10px;
      border: none;
      border-radius: 5px;
    }

    select {
      width: 250px;
    }

    button {
      background-color: #ff3c00;
      color: white;
      cursor: pointer;
    }

    footer {
      margin-top: 60px;
      font-size: 0.9em;
      color: #999;
    }
  </style>
</head>
<body>

  <h1>CarFixHelper 🚘</h1>
  <p>Diagnose common car problems and get quick help to fix them.</p>
  
  <img src="https://images.unsplash.com/photo-1570129477492-45c003edd2be" alt="Car Repair" class="car-image" />

  <div class="form-section">
    <h2>Select a Car Problem</h2>
    <form id="problemForm">
      <select id="problemSelect" required>
        <option value="">-- Choose a problem --</option>
        <option value="engine.html">Engine won’t start</option>
        <option value="brakes.html">Brake problems</option>
        <option value="overheating.html">Car is overheating</option>
        <option value="battery.html">Battery issues</option>
        <option value="tires.html">Flat or low tire</option>
      </select>
      <br />
      <button type="submit">Fix It 🔧</button>
    </form>
  </div>

  <footer>
    &copy; 2025 CarFixHelper. Built to help you fix it fast.
  </footer>

  <script>
    document.getElementById('problemForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const page = document.getElementById('problemSelect').value;
      if (page) {
        window.location.href = page;
      } else {
        alert("Please select a problem to continue.");
      }
    });
  </script>

</body>
</html>
