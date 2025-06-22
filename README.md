<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Login Page</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f0f2f5;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .login-container {
      background: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
      width: 300px;
    }

    .login-container h2 {
      margin-bottom: 20px;
      text-align: center;
    }

    .form-group {
      margin-bottom: 15px;
    }

    .form-group label {
      display: block;
      margin-bottom: 5px;
    }

    .form-group input {
      width: 100%;
      padding: 8px;
      box-sizing: border-box;
    }

    button {
      width: 100%;
      padding: 10px;
      background: #4CAF50;
      border: none;
      color: white;
      font-size: 16px;
      border-radius: 5px;
      cursor: pointer;
    }

    .error {
      color: red;
      text-align: center;
      margin-top: 10px;
    }
  </style>
</head>
<body>

  <div class="login-container">
    <h2>Login</h2>
    <div class="form-group">
      <label>Username</label>
      <input type="text" id="username" placeholder="Enter username" />
    </div>
    <div class="form-group">
      <label>Password</label>
      <input type="password" id="password" placeholder="Enter password" />
    </div>
    <button onclick="login()">Login</button>
    <div class="error" id="error-msg"></div>
  </div>

  <script>
    function login() {
      const username = document.getElementById("username").value;
      const password = document.getElementById("password").value;
      const errorMsg = document.getElementById("error-msg");

      if (username === "admin" && password === "1234") {
        alert("Login successful!");
        // redirect or continue
      } else {
        errorMsg.textContent = "Invalid username or password";
      }
    }
  </script>

</body>
</html>
