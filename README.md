<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>TuNoSaBeNa</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #e8f0ff 0%, #ffffff 100%);
      color: #222;
      padding: 2em;
      min-height: 100vh;
    }
    header {
      text-align: center;
      padding: 1.5em;
      background: rgba(255, 255, 255, 0.6);
      border-radius: 16px;
      backdrop-filter: blur(20px) saturate(180%);
      -webkit-backdrop-filter: blur(20px) saturate(180%);
      border: 1px solid rgba(255, 255, 255, 0.4);
      box-shadow: 0 4px 30px rgba(0,0,0,0.08);
    }
    section {
      padding: 2em;
      margin: 1.5em auto;
      border-radius: 16px;
      max-width: 900px;
      background: rgba(255, 255, 255, 0.55);
      backdrop-filter: blur(18px) saturate(160%);
      -webkit-backdrop-filter: blur(18px) saturate(160%);
      border: 1px solid rgba(255, 255, 255, 0.4);
      box-shadow: 0 4px 25px rgba(0,0,0,0.1);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    section:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 30px rgba(0,0,0,0.15);
    }
    h1, h2, h3 {
      color: #111;
    }
    .video-grid {
  display: grid;
  gap: 1em;
}

/* 🧱 Dos columnas en todos los móviles, incluso los más pequeños */
@media screen and (max-width: 768px) {
  .video-grid {
    grid-template-columns: repeat(2, 1fr) !important;
  }
}

/* 💻 Tres columnas o más en pantallas grandes */
@media screen and (min-width: 769px) {
  .video-grid {
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)) !important;
  }
}

/* 🎨 Fondo bicolor azul-rojo difuminado */
body {
  margin: 0;
  font-family: 'Segoe UI', sans-serif;
  background: linear-gradient(135deg, #0044ff 0%, #ff0033 100%);
  background-attachment: fixed;
  background-size: cover;
  color: #fff;
  padding: 2em;
  min-height: 100vh;
}
    .video {
      position: relative;
      cursor: pointer;
      background: rgba(255,255,255,0.35);
      border-radius: 12px;
      overflow: hidden;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    .video:hover {
      transform: scale(1.03);
      box-shadow: 0 4px 20px rgba(0,0,0,0.1);
    }
    .video img {
      width: 100%;
      display: block;
    }
    .play-button {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 3em;
      color: white;
      text-shadow: 0 0 20px rgba(255,255,255,0.7);
      opacity: 0.85;
      transition: transform 0.2s, opacity 0.2s;
    }
    .video:hover .play-button {
      transform: translate(-50%, -50%) scale(1.1);
      opacity: 1;
    }
    audio {
      width: 100%;
      border-radius: 8px;
      background-color: rgba(255,255,255,0.3);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
      border: 1px solid rgba(255,255,255,0.4);
    }
    .catalogo-card {
      text-align: center;
      padding: 2em;
      border-radius: 16px;
      background: rgba(255,255,255,0.7);
      backdrop-filter: blur(20px);
      border: 1px solid rgba(255,255,255,0.4);
      box-shadow: 0 4px 25px rgba(0,0,0,0.1);
    }
    .catalogo-card button {
      margin-top: 1em;
      padding: 0.8em 1.8em;
      font-size: 1.1em;
      border: none;
      border-radius: 30px;
      background: linear-gradient(90deg, #0072ff, #00c6ff);
      color: white;
      cursor: pointer;
      transition: background 0.3s ease, transform 0.2s ease;
    }
    .catalogo-card button:hover {
      background: linear-gradient(90deg, #0055cc, #00aaff);
      transform: scale(1.05);
    }
    footer {
      text-align: center;
      padding: 1em;
      background: rgba(255,255,255,0.55);
      border-radius: 12px;
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255,255,255,0.4);
      margin-top: 2em;
      font-size: 1em;
    }
  </style>
</head>
<body>
  <header>
    <h1 class="titulo-principal">TuNoSaBeNa</h1>
  </header>

  <section id="galeria-videos">
    <h2>🎵 FONTANERO MUSIC</h2>
    <p>Canciones que animan. ¿Quieres más? Ya sabes dónde encontrarme.</p>
    <div class="playlist">
      <div>
        <h3>LATINO MIX 2023</h3>
        <audio controls>
          <source src="https://dl.dropboxusercontent.com/scl/fi/tzka46nhcclxieizxnn0i/LATINO-MIX-2023.mp3?rlkey=kpa8xwmaso8kdcm0j1zt6squd&st=f54ztlwt" type="audio/mpeg">
        </audio>
      </div>
      <div>
        <h3>Salsa Vieja</h3>
        <audio controls>
          <source src="https://dl.dropboxusercontent.com/scl/fi/mxxv0bwdrz93cgqqlfrpt/Salsa-Vieja-MP3.mp3?rlkey=c5nrbj8j22ybjxxnxw98fm66d&st=rsec3mr0" type="audio/mpeg">
        </audio>
      </div>
    </div>
  </section>

  <section id="videos">
    <h2>🎬 VideosRodri recomendados</h2>
    <div class="video-grid" id="videoGrid"></div>
  </section>

  <section id="catalogo">
    <h2>📘 Catálogo SIMON 270</h2>
    <div class="catalogo-card">
      <p>Descubre el catálogo completo de productos SIMON 270 para 2025.</p>
      <a href="Simon270_Catalogo_2025.pdf" target="_blank">
        <button>Ver Catálogo</button>
      </a>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 LUMINARTE. Todos los derechos reservados.</p>
  </footer>

  <script>
    const videos = [
      "hCW2NHbWNwA",
      "VaVC3PAWqLk",
      "YflRLhAY-_k",
      "yfEQRqFo2bI",
      "oIiv_335yus",
      "UNGpoO3NHC8",
      "JV0VKAw3kPs"
    ];

    const videoGrid = document.getElementById("videoGrid");
    let currentVideo = null;

    videos.forEach(id => {
      const div = document.createElement("div");
      div.className = "video";
      div.innerHTML = `
        <img src="https://img.youtube.com/vi/${id}/hqdefault.jpg" alt="Video preview">
        <div class="play-button">▶️</div>
      `;
      div.addEventListener("click", () => {
        if (currentVideo && currentVideo !== div) {
          currentVideo.innerHTML = `
            <img src="https://img.youtube.com/vi/${currentVideo.dataset.id}/hqdefault.jpg" alt="Video preview">
            <div class="play-button">▶️</div>
          `;
        }
        div.dataset.id = id;
        div.innerHTML = `
          <iframe width="100%" height="200" src="https://www.youtube.com/embed/${id}?autoplay=1"
            frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
        `;
        currentVideo = div;
      });
      div.dataset.id = id;
      videoGrid.appendChild(div);
    });
  </script>
</body>
</html>
