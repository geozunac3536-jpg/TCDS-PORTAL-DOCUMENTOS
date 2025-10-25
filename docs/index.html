<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>TCDS — PORTAL DOCUMENTOS</title>
  <link rel="icon" href="data:,">
  <style>
    :root {
      --bg: #0b0d12;
      --card: #121621;
      --muted: #9aa4b2;
      --accent: #ff3c3c;
      --accent2: #ff6f6f;
      --ring: #ff9c9c;
    }
    * { box-sizing: border-box }
    html, body {
      margin: 0;
      background: var(--bg);
      color: #e6edf3;
      font: 16px/1.55 Inter, system-ui;
    }
    a { color: inherit; text-decoration: none }
    .container { max-width: 1200px; margin: 0 auto; padding: 24px }
    .nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 16px 0;
    }
    .nav a {
      padding: 8px 14px;
      border-radius: 12px;
      background: var(--card);
      border: 1px solid var(--accent);
    }
    .nav a:hover { background: var(--accent); color: #fff }
    .h1 {
      font-size: clamp(28px, 4vw, 44px);
      font-weight: 800;
      line-height: 1.1;
      background: linear-gradient(92deg, var(--accent), var(--accent2));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .p { color: var(--muted) }
    .btn {
      display: inline-flex;
      gap: 10px;
      align-items: center;
      padding: 12px 16px;
      border-radius: 14px;
      border: 1px solid var(--accent);
      background: var(--card);
      color: var(--accent);
      cursor: pointer;
      transition: 0.2s ease;
    }
    .btn:hover {
      background: var(--accent);
      color: #fff;
      border-color: var(--ring);
    }
    .footer {
      margin: 40px 0 16px;
      color: #7f8a99;
      font-size: 14px;
      text-align: center;
    }
  </style>
</head>
<body>
  <div class="container">
    <nav class="nav">
      <div class="h1">TCDS — PORTAL DOCUMENTOS</div>
      <div>
        <a href="index.html">Inicio</a>
        <a href="https://github.com/geozunac3536-jpg/TCDS-PORTAL-DOCUMENTOS">Repositorio</a>
      </div>
    </nav>

    <section>
      <h1 class="h1">Documentos Fundamentales del Canon TCDS</h1>
      <p class="p">Selecciona un documento para visualizarlo directamente. El visor se adapta a tu pantalla.</p>

      <!-- Botones -->
      <div style="display:flex;flex-wrap:wrap;gap:12px;margin-bottom:20px">
        <button class="btn" onclick="loadPDF('pdf/simbiosis.pdf')">🤝 Simbiosis</button>
        <button class="btn" onclick="loadPDF('pdf/anexo_isomorfico.pdf')">🔁 Anexo Isomórfico</button>
        <button class="btn" onclick="loadPDF('pdf/propuesta_reestructurada_tcds.pdf')">📐 Reestructura TCDS</button>
        <button class="btn" onclick="loadPDF('pdf/coherencia.pdf')">🧠 Coherencia</button>
        <button class="btn" onclick="loadPDF('pdf/modelo_palindromo_tcds.pdf')">🪞 Palíndromo TCDS</button>
        <button class="btn" onclick="loadPDF('pdf/reestructura_de_sigma_y_su_campo.pdf')">📡 Campo Sigma</button>
        <button class="btn" onclick="loadPDF('pdf/proyecto_vacio.pdf')">🌀 Proyecto Vacío</button>
      </div>

      <!-- Visor embebido -->
      <div style="width:100%;height:calc(100vh - 300px);overflow:hidden;border-radius:12px;border:1px solid var(--accent)">
        <iframe id="pdf-viewer" src="pdf/simbiosis.pdf" width="100%" height="100%" style="border:none;"></iframe>
      </div>
    </section>

    <footer class="footer">
      © Genaro Carrasco Ozuna — TCDS. ORCID: <a href="https://orcid.org/0009-0005-6358-9910" target="_blank">0009-0005-6358-9910</a>
    </footer>
  </div>

  <!-- Script de carga dinámica -->
  <script>
    function loadPDF(path) {
      const viewer = document.getElementById('pdf-viewer');
      viewer.style.opacity = 0;
      setTimeout(() => {
        viewer.src = path;
        viewer.style.opacity = 1;
      }, 200);
    }
  </script>

  <!-- Script de validación automática -->
  <script>
    const pdfFiles = [
      "simbiosis.pdf",
      "anexo_isomorfico.pdf",
      "propuesta_reestructurada_tcds.pdf",
      "coherencia.pdf",
      "modelo_palindromo_tcds.pdf",
      "reestructura_de_sigma_y_su_campo.pdf",
      "proyecto_vacio.pdf"
    ];

    const missing = [];

    async function validatePDFs() {
      for (const file of pdfFiles) {
        const url = `pdf/${file}`;
        try {
          const res = await fetch(url, { method: "HEAD" });
          if (!res.ok) missing.push(file);
        } catch (err) {
          missing.push(file);
        }
      }

      if (missing.length > 0) {
        alert("⚠️ Archivos faltantes en /docs/pdf:\n\n" + missing.join("\n"));
      }
    }

    window.addEventListener("DOMContentLoaded", validatePDFs);
  </script>
</body>
</html>
