<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Application Portal</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }

        .container {
            max-width: 800px;
            margin: auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .applications {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }

        .application {
            flex: 1 1 calc(33.33% - 20px);
            background-color: #3498db;
            color: #fff;
            padding: 20px;
            border-radius: 8px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .application:hover {
            background-color: #2980b9;
        }

        .editor {
            display: none;
        }

        .access-code-input {
            margin-bottom: 10px;
        }

        .access-code-button {
            background-color: #2ecc71;
            color: #fff;
            padding: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="applications" id="applications">
            <!-- Applications will be dynamically added here -->
        </div>

        <div class="editor" id="editor">
            <h2>Editor</h2>
            <input type="text" class="access-code-input" id="accessCode" placeholder="Enter Access Code">
            <button class="access-code-button" onclick="verifyAccessCode()">Access</button>
        </div>
    </div>

    <script>
        function verifyAccessCode() {
            var accessCode = document.getElementById('accessCode').value;

            // Replace this with actual access code verification logic
            if (accessCode === 'your_access_code') {
                showEditor();
            } else {
                alert('Invalid access code');
            }
        }

        function showEditor() {
            document.getElementById('editor').style.display = 'block';
        }
    </script>
</body>
</html>
