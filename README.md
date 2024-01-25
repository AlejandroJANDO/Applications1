
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Staff Application Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
    }
    form {
      max-width: 600px;
      margin: 0 auto;
    }
    label {
      display: block;
      margin-bottom: 8px;
    }
    input, textarea {
      width: 100%;
      padding: 8px;
      margin-bottom: 16px;
      box-sizing: border-box;
    }
    button {
      background-color: #4CAF50;
      color: white;
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    button:hover {
      background-color: #45a049;
    }
    #results {
      margin-top: 20px;
    }
  </style>
</head>
<body>

  <form id="myForm">
    <label for="discord">Discord Username and Tag:</label>
    <input type="text" id="discord" name="discord" required>

    <label for="roblox">Roblox Username:</label>
    <input type="text" id="roblox" name="roblox" required>

    <label for="age">How old are you:</label>
    <input type="number" id="age" name="age" required>

    <label for="activity">How active are you (scale 1-10):</label>
    <input type="number" id="activity" name="activity" min="1" max="10" required>

    <label for="grammar">Grammar and spelling skills (scale 1-10):</label>
    <input type="number" id="grammar" name="grammar" min="1" max="10" required>

    <label for="experience">Do you have staff experience? If so, what rank did you achieve:</label>
    <input type="text" id="experience" name="experience" required>

    <label for="qualification">What makes you qualify for staff:</label>
    <textarea id="qualification" name="qualification" rows="4" required></textarea>

    <label for="why">Why should we accept you over others:</label>
    <textarea id="why" name="why" rows="4" required></textarea>

    <label for="rdm">What does RDM mean:</label>
    <input type="text" id="rdm" name="rdm" required>

    <label for="vdm">What does VDM mean:</label>
    <input type="text" id="vdm" name="vdm" required>

    <label for="ltap">What does LTAP mean? Explain if needed:</label>
    <textarea id="ltap" name="ltap" rows="4" required></textarea>

    <label for="action">What would you do if someone was shooting at civ spawn and killed you:</label>
    <textarea id="action" name="action" rows="4" required></textarea>

    <label for="other">Any other things you want to say (optional):</label>
    <textarea id="other" name="other" rows="4"></textarea>

    <button type="button" onclick="submitForm()">Submit</button>
  </form>

  <div id="results"></div>

  <script>
    function submitForm() {
      var formData = {
        discord: document.getElementById('discord').value,
        roblox: document.getElementById('roblox').value,
        age: document.getElementById('age').value,
        activity: document.getElementById('activity').value,
        grammar: document.getElementById('grammar').value,
        experience: document.getElementById('experience').value,
        qualification: document.getElementById('qualification').value,
        why: document.getElementById('why').value,
        rdm: document.getElementById('rdm').value,
        vdm: document.getElementById('vdm').value,
        ltap: document.getElementById('ltap').value,
        action: document.getElementById('action').value,
        other: document.getElementById('other').value
      };

      // Simple client-side validation
      for (var key in formData) {
        if (!formData[key]) {
          alert('Please fill in all fields.');
          return;
        }
      }

      // Display results
      var resultsDiv = document.getElementById('results');
      resultsDiv.innerHTML = '<h2>Application Results</h2>';
      for (var key in formData) {
        resultsDiv.innerHTML += '<p><strong>' + key.charAt(0).toUpperCase() + key.slice(1) + ':</strong> ' + formData[key] + '</p>';
      }

      // You can also reset the form after submission
      document.getElementById('myForm').reset();
    }
  </script>

</body>
</html>
