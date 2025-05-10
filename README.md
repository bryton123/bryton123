<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>MJ Motors Login</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #e3eaf0;
      margin: 0;
      padding: 0;
    }

    .navbar {
      background-color: #121820;
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      padding: 10px 20px;
    }

    .logo-box {
      display: flex;
      align-items: center;
    }

    .m-logo {
      font-family: Georgia, serif;
      font-size: 60px;
      font-weight: bold;
      color: transparent;
      background: linear-gradient(135deg, red 45%, transparent 45%, transparent 55%, red 55%);
      -webkit-background-clip: text;
      background-clip: text;
      transform: skewX(-5deg);
      letter-spacing: 2px;
      margin-right: 10px;
    }

    .logo-text {
      color: red;
      font-weight: bold;
      font-size: 20px;
      letter-spacing: 1px;
    }

    .navbar-right {
      display: flex;
      flex-direction: column;
      align-items: flex-end;
    }

    .menu-lines {
      display: flex;
      flex-direction: column;
      gap: 4px;
      margin-bottom: 5px;
    }

    .menu-lines div {
      height: 3px;
      background-color: red;
      border-radius: 2px;
    }

    .menu-lines div:nth-child(1) {
      width: 25px;
    }

    .menu-lines div:nth-child(2) {
      width: 18px;
    }

    .menu-lines div:nth-child(3) {
      width: 12px;
    }

    .sell-btn {
      background-color: red;
      color: white;
      padding: 8px 15px;
      border-radius: 5px;
      border: none;
      font-weight: bold;
      cursor: pointer;
    }

    .container {
      text-align: center;
      margin-top: 30px;
    }

    .tabs {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-bottom: 30px;
    }

    .tabs button {
      background-color: #dbe0e7;
      padding: 10px 30px;
      border: none;
      border-radius: 10px;
      font-size: 16px;
      cursor: pointer;
      color: #121820;
      font-weight: bold;
    }

    h2 {
      font-weight: bold;
      color: #121820;
    }

    p {
      color: #121820;
    }

    .form-box {
      max-width: 400px;
      margin: 0 auto;
      background-color: transparent;
      padding: 20px;
      text-align: left;
    }

    .form-box input[type="text"],
    .form-box input[type="password"] {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border-radius: 8px;
      border: none;
      background-color: #f2f4f6;
    }

    .form-options {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 14px;
      color: #121820;
    }

    .form-options label {
      display: flex;
      align-items: center;
      color: #121820;
    }

    .form-options a {
      color: #121820;
      text-decoration: underline;
    }

    .login-btn {
      width: 100%;
      padding: 12px;
      margin-top: 20px;
      background-color: red;
      color: white;
      font-size: 16px;
      font-weight: bold;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="navbar">
    <div class="logo-box">
      <div class="m-logo">M</div>
      <div class="logo-text">J MOTORS</div>
    </div>
    <div class="navbar-right">
      <div class="menu-lines">
        <div></div>
        <div></div>
        <div></div>
      </div>
      <button class="sell-btn">Sell My Car</button>
    </div>
  </div>

  <div class="container">
    <div class="tabs">
      <button>Login</button>
      <button>Register</button>
    </div>

    <h2>Log in to your account</h2>
    <p>Welcome back! Sign in to your account</p>

    <div class="form-box">
      <input type="text" placeholder="Email or Username" />
      <input type="password" placeholder="Password" />
      <div class="form-options">
        <label><input type="checkbox" /> Remember</label>
        <a href="#">Forgotten password?</a>
      </div>
      <button class="login-btn">Login</button>
    </div>
  </div>
</body>
</html>
