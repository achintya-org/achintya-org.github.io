<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, viewport-fit=cover" />
<title>Achintya</title>
<meta name="description" content="The silent revolution to take the world from Internet to Innernet" />

<!-- Theme / status bar -->
<meta name="theme-color" content="#000000" />

<!-- Android / Chrome: Web App Manifest (drives the Add to Home Screen name + icon) -->
<link rel="manifest" href="data:application/manifest+json;base64,eyJuYW1lIjogIkFjaGludHlhIiwgInNob3J0X25hbWUiOiAiQWNoaW50eWEiLCAic3RhcnRfdXJsIjogImh0dHBzOi8vYWNoaW50eWEub3JnIiwgInNjb3BlIjogImh0dHBzOi8vYWNoaW50eWEub3JnIiwgImRpc3BsYXkiOiAic3RhbmRhbG9uZSIsICJvcmllbnRhdGlvbiI6ICJwb3J0cmFpdCIsICJ0aGVtZV9jb2xvciI6ICIjMDAwMDAwIiwgImJhY2tncm91bmRfY29sb3IiOiAiI2ZmZmZmZiIsICJpY29ucyI6IFt7InNyYyI6ICIvbG9nbzE5Mi5wbmciLCAic2l6ZXMiOiAiMTkyeDE5MiIsICJ0eXBlIjogImltYWdlL3BuZyJ9LCB7InNyYyI6ICIvbG9nbzUxMi5wbmciLCAic2l6ZXMiOiAiNTEyeDUxMiIsICJ0eXBlIjogImltYWdlL3BuZyJ9XX0=" />
<meta name="mobile-web-app-capable" content="yes" />

<!-- iOS Safari: Add to Home Screen doesn't read the manifest, needs these directly -->
<meta name="apple-mobile-web-app-capable" content="yes" />
<meta name="apple-mobile-web-app-status-bar-style" content="black" />
<meta name="apple-mobile-web-app-title" content="Achintya" />
<link rel="apple-touch-icon" href="/logo512.png" />

<!-- Favicon -->
<link rel="icon" href="/uprightA.png" />

<style>
  * { box-sizing: border-box; }
  html, body {
    margin: 0; padding: 0; height: 100%;
    background: #fff; color: #000;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  }
  body {
    display: flex; align-items: center; justify-content: center;
    min-height: 100vh; min-height: 100dvh;
    padding: 24px;
  }
  a { text-decoration: none; color: inherit; }
  .card {
    display: flex; flex-direction: column; align-items: center;
    text-align: center; max-width: 420px; width: 100%;
  }
  .logo {
    width: 130px; height: auto; margin-bottom: 8px;
  }
  .title {
    font-weight: 500; font-size: 36px; margin: 4px 0;
  }
  .tagline {
    font-weight: 200; font-size: 15px; margin: 0 0 32px; color: #333;
  }
  .enter-btn, .submit-btn {
    background: #000; color: #fff; border: none;
    font-size: 16px; cursor: pointer; padding: 16px 40px;
    letter-spacing: 0.02em;
  }
  .enter-btn:active, .submit-btn:active { opacity: 0.8; }
  .login-form {
    display: none; flex-direction: column; gap: 10px; align-items: center; width: 100%;
  }
  .login-form.visible { display: flex; }
  .enter-wrap.hidden { display: none; }
  .username-input {
    padding: 11px; border-radius: 8px; border: 1.5px solid #111;
    font-size: 15px; width: 100%; max-width: 260px;
    background: #fff; color: #111; font-weight: 700;
    font-family: inherit; text-align: center;
  }
  .username-input:focus { outline: none; }
  .error-msg {
    min-height: 18px; font-size: 13px; color: #d00; margin: 2px 0 0;
  }
</style>
</head>
<body>
  <div class="card">
    <img class="logo" src="/uprightA.png" alt="Achintya" />
    <p class="title">Achintya</p>
    <p class="tagline">The silent revolution to take the world from Internet to Innernet!</p>

    <div class="enter-wrap" id="enterWrap">
      <button class="enter-btn" id="enterBtn" type="button">Enter</button>
    </div>

    <form class="login-form" id="loginForm">
      <input class="username-input" id="usernameInput" type="text" placeholder="Username" autocomplete="off" autocapitalize="off" />
      <button class="submit-btn" type="submit">Continue</button>
      <p class="error-msg" id="errorMsg">&nbsp;</p>
    </form>
  </div>

  <script>
    var enterBtn = document.getElementById('enterBtn');
    var enterWrap = document.getElementById('enterWrap');
    var loginForm = document.getElementById('loginForm');
    var usernameInput = document.getElementById('usernameInput');
    var errorMsg = document.getElementById('errorMsg');

    enterBtn.addEventListener('click', function () {
      enterWrap.classList.add('hidden');
      loginForm.classList.add('visible');
      usernameInput.focus();
    });

    loginForm.addEventListener('submit', function (e) {
      e.preventDefault();
      errorMsg.textContent = 'Unregistered User';
    });
  </script>
</body>
</html>
