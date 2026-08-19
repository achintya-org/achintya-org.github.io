<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <meta name="theme-color" content="#000000">
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black">
  <meta name="apple-mobile-web-app-title" content="Achintya">
  <title>Achintya</title>

  <style>
    * {
      box-sizing: border-box;
    }

    html,
    body {
      margin: 0;
      width: 100%;
      min-height: 100%;
      background: #000;
      color: #fff;
      font-family: Arial, Helvetica, sans-serif;
    }

    body {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .app {
      width: 100%;
      max-width: 520px;
      min-height: 100vh;
      padding: 70px 28px 40px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
    }

    .logo {
      width: 86px;
      height: 86px;
      margin-bottom: 28px;
      object-fit: contain;
    }

    .title {
      margin: 0;
      font-family: Georgia, "Times New Roman", serif;
      font-size: 48px;
      font-weight: 400;
      letter-spacing: -1px;
    }

    .subtitle {
      margin: 12px 0 52px;
      max-width: 430px;
      color: #aaa;
      font-size: 16px;
      line-height: 1.55;
    }

    .login {
      width: 100%;
      max-width: 420px;
    }

    .input {
      width: 100%;
      height: 58px;
      padding: 0 18px;
      border: 1px solid #444;
      border-radius: 8px;
      outline: none;
      background: #080808;
      color: #fff;
      font-size: 17px;
      text-align: center;
    }

    .input:focus {
      border-color: #888;
    }

    .input::placeholder {
      color: #666;
    }

    .button {
      width: 100%;
      height: 58px;
      margin-top: 14px;
      border: 0;
      border-radius: 8px;
      background: #fff;
      color: #000;
      font-size: 17px;
      cursor: pointer;
    }

    .error {
      display: none;
      margin-top: 18px;
      color: #fff;
      font-size: 15px;
    }

    .error.show {
      display: block;
    }

    @media (max-width: 480px) {
      .app {
        padding: 50px 24px 30px;
      }

      .logo {
        width: 72px;
        height: 72px;
      }

      .title {
        font-size: 42px;
      }

      .subtitle {
        font-size: 15px;
        margin-bottom: 44px;
      }
    }
  </style>
</head>

<body>
  <main class="app">

    <img class="logo" src="uprightA.png" alt="Achintya">

    <h1 class="title">Achintya</h1>

    <div class="subtitle">
      The silent revolution to take the world from Internet to Innernet
    </div>

    <form class="login" id="login">
      <input
        id="username"
        class="input"
        type="text"
        autocomplete="username"
        placeholder="Username"
        autofocus
      >

      <button class="button" type="submit">
        Continue
      </button>

      <div class="error" id="error">
        Invalid user
      </div>
    </form>

  </main>

  <script>
    document.getElementById("login").addEventListener("submit", function (event) {
      event.preventDefault();

      const username = document.getElementById("username").value.trim();
      const error = document.getElementById("error");

      if (username) {
        error.classList.add("show");
      }
    });
  </script>
</body>
</html>
