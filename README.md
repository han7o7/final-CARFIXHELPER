<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Compatibility Checker</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      text-align: center;
      padding: 50px;
    }

    input {
      margin: 10px;
      padding: 8px;
      font-size: 1em;
    }

    button {
      padding: 10px 20px;
      font-size: 1em;
      background: crimson;
      color: white;
      border: none;
      cursor: pointer;
    }

    #result {
      margin-top: 20px;
      font-size: 1.2em;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <h1>Compatibility Checker</h1>

  <form id="compatibilityForm">
    <input type="text" id="name1" placeholder="Your Name" required />
    <input type="text" id="name2" placeholder="Their Name" required />
    <button type="submit">Check Compatibility</button>
  </form>

  <div id="result"></div>

  <script>
    // Feature 1: Input form handling
    document.getElementById('compatibilityForm').addEventListener('submit', function (e) {
      e.preventDefault();
      const name1 = document.getElementById('name1').value.trim();
      const name2 = document.getElementById('name2').value.trim();

      if (!name1 || !name2) return alert('Please enter both names.');

      // Feature 2: Basic compatibility algorithm (random)
      const score = Math.floor(Math.random() * 101);
      const message = generateMessage(score);

      // Feature 3: Display result dynamically
      document.getElementById('result').innerText = `${name1} ❤️ ${name2}: ${score}% Compatible\n${message}`;

      // Feature 4: Save to localStorage (advanced feature)
      saveHistory(name1, name2, score);
    });

    // Feature 5 (greater complexity): Generate custom message
    function generateMessage(score) {
      if (score > 80) return "A perfect match!";
      if (score > 60) return "Looking pretty good!";
      if (score > 40) return "There's potential.";
      return "Might want to reconsider...";
    }

    // Advanced Feature 2: Save compatibility data to localStorage
    function saveHistory(name1, name2, score) {
      const history = JSON.parse(localStorage.getItem('compatibilityHistory')) || [];
      history.push({ name1, name2, score, time: new Date().toLocaleString() });
      localStorage.setItem('compatibilityHistory', JSON.stringify(history));
    }
  </script>

</body>
</html>
