<!DOCTYPE html>
<html>
<head>
  <title>Password Gate</title>
  <style>
    body {
      background-color: black;
      color: white;
      font-family: Arial, sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }
    #inputSection, #message {
      margin-top: 20px;
    }
    input {
      padding: 10px;
      font-size: 16px;
    }
    button {
      padding: 10px 15px;
      font-size: 16px;
      margin-left: 10px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h2>Enter the password</h2>
  <div id="inputSection">
    <input type="password" id="passwordInput" placeholder="Type password here">
    <button onclick="checkPassword()">Submit</button>
  </div>
  <div id="message"></div>

  <script>
    function checkPassword() {
      const input = document.getElementById('passwordInput').value;
      const message = document.getElementById('message');
      if (input === 'Rms4009') {
        message.innerHTML = "<h2>Hi you guess it</h2>";
        document.getElementById('inputSection').style.display = 'none';
      } else {
        message.textContent = "Password is incorrect";
      }
    }
  </script>
</body>
</html>
