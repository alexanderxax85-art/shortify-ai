# shortify-ai
DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Shortify AI – Dashboard</title>

  <style>
    * { box-sizing: border-box; }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #0f1220;
      color: #fff;
    }

    .sidebar {
      width: 220px;
      background: #151933;
      height: 100vh;
      position: fixed;
      padding: 20px;
    }

    .sidebar h2 {
      color: #4da3ff;
      margin-bottom: 30px;
    }

    .sidebar a {
      display: block;
      color: #cfd3ff;
      text-decoration: none;
      margin: 15px 0;
      transition: 0.2s;
    }

    .sidebar a:hover {
      color: #4da3ff;
    }

    .main {
      margin-left: 240px;
      padding: 30px;
    }

    .card {
      background: #1c2147;
      padding: 20px;
      border-radius: 12px;
      margin-bottom: 20px;
    }

    button {
      background: #4da3ff;
      border: none;
      padding: 12px 20px;
      border-radius: 8px;
      color: #000;
      font-weight: bold;
      cursor: pointer;
    }

    button:hover {
      opacity: 0.9;
    }

    .clips li {
      background: #2a2f63;
      margin: 10px 0;
      padding: 10px;
      border-radius: 8px;
      list-style: none;
    }

    footer {
      margin-top: 40px;
      color: #888;
      font-size: 14px;
    }
  </style>
</head>

<body>

  <div class="sidebar">
    <h2>Shortify AI</h2>
    <a href="#">🏠 Dashboard</a>
    <a href="#">🎬 Crear Video</a>
    <a href="#">📁 Mis Clips</a>
    <a href="#">⚙️ Configuración</a>
  </div>

  <div class="main">
    <h1>Dashboard</h1>

    <div class="card">
      <h3>Crear video corto</h3>
      <p>Genera Shorts, Reels o TikToks automáticamente con IA.</p>
      <button onclick="crearVideo()">Crear ahora</button>
    </div>

    <div class="card">
      <h3>Mis Clips</h3>
      <ul class="clips" id="listaClips">
        <li>No hay videos aún.</li>
      </ul>
    </div>

    <footer>
      © 2026 Shortify AI — Proyecto demo
    </footer>
  </div>

  <script>
    let contador = 1;

    function crearVideo() {
      const lista = document.getElementById("listaClips");

      if (contador === 1) {
        lista.innerHTML = "";
      }

      const clip = document.createElement("li");
      clip.textContent = "🎥 Video generado #" + contador;
      lista.appendChild(clip);

      contador++;
    }
  </script>

</body>
</html>
