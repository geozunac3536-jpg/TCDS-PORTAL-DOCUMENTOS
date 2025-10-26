<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>TCDS — Portal de Documentos</title>
  <style>
    :root{--bg:#0a0a0a;--fg:#e5e5e5;--accent:#e63946;--card:#151515;--border:#333}
    *{box-sizing:border-box;margin:0;padding:0}
    body{background:var(--bg);color:var(--fg);font-family:system-ui,Segoe UI,Roboto,sans-serif}
    header{padding:1.5rem;border-bottom:1px solid var(--border);text-align:center}
    h1{color:var(--accent);font-size:1.4rem}
    .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:1rem;padding:1rem}
    .card{background:var(--card);border:1px solid var(--border);border-radius:12px;padding:1rem}
    .card h2{font-size:1rem;color:var(--accent);margin-bottom:.25rem}
    .card p{font-size:.9rem;margin-bottom:.75rem}
    .btn{display:inline-block;background:var(--accent);color:var(--fg);padding:.5rem .8rem;border-radius:8px;text-decoration:none;font-weight:600}
    .viewer-wrap{padding:0 1rem 1rem}
    .toolbar{display:flex;gap:.5rem;align-items:center;margin:.5rem 0}
    .toolbar a{font-size:.85rem}
    object{width:100%;height:80vh;border:1px solid var(--border);border-radius:10px;background:#0f0f0f}
    .hint{font-size:.85rem;color:#aaa}
    footer{padding:1rem;border-top:1px solid var(--border);text-align:center;color:#888}
  </style>
</head>
<body>
  <header>
    <h1>TCDS — Portal de Documentos</h1>
    <p>Repositorio maestro del Canon TCDS</p>
  </header>

  <main>
    <section class="grid" id="cards">
      <div class="card"><h2>🤝 Simbiosis</h2><p>Ingeniería paradigmática Humano–IA.</p>
        <a class="btn" data-pdf="pdf/simbiosis.pdf" href="#">Ver PDF</a></div>

      <div class="card"><h2>🔁 Anexo Isomórfico</h2><p>Parámetros cruzados.</p>
        <a class="btn" data-pdf="pdf/anexo_isomorfico.pdf" href="#">Ver PDF</a></div>

      <div class="card"><h2>📐 Reestructura TCDS</h2><p>Elevación de E a coherencia.</p>
        <a class="btn" data-pdf="pdf/propuestareestructuradatcds.pdf" href="#">Ver PDF</a></div>

      <div class="card"><h2>🧠 Coherencia</h2><p>LBCU como ecuación de estado.</p>
        <a class="btn" data-pdf="pdf/coherencia.pdf" href="#">Ver PDF</a></div>

      <div class="card"><h2>🪞 Palíndromo TCDS</h2><p>Modo espejo causal.</p>
        <a class="btn" data-pdf="pdf/modelopalindromotcds.pdf" href="#">Ver PDF</a></div>

      <div class="card"><h2>📡 Campo Σ</h2><p>Cotas y decisión.</p>
        <a class="btn" data-pdf="pdf/reestructuradesigmaysu_campo.pdf" href="#">Ver PDF</a></div>

      <div class="card"><h2>🌀 Proyecto Vacío</h2><p>Validación mínima y Sincronón.</p>
        <a class="btn" data-pdf="pdf/proyecto_vacio.pdf" href="#">Ver PDF</a></div>
    </section>

    <section class="viewer-wrap" id="viewerWrap" style="display:none">
      <div class="toolbar">
        <a id="openNative" class="btn" href="#" target="_blank" rel="noopener">Abrir en pestaña nueva</a>
        <span class="hint" id="statusHint">Cargando…</span>
      </div>
      <object id="viewer" type="application/pdf" data="">
        <p>No se pudo embeber el PDF. <a id="fallbackLink" href="#" target="_blank" rel="noopener">Abrir externo</a></p>
      </object>
    </section>
  </main>

  <footer>© 2025 Genaro Carrasco Ozuna · <a href="https://orcid.org/0009-0005-6358-9910" style="color:#888">ORCID</a></footer>

  <script>
    const wrap = document.getElementById('viewerWrap');
    const obj = document.getElementById('viewer');
    const openNative = document.getElementById('openNative');
    const fallbackLink = document.getElementById('fallbackLink');
    const hint = document.getElementById('statusHint');

    async function show(pdfPath){
      hint.textContent = 'Verificando recurso…';
      wrap.style.display = 'block';
      openNative.href = pdfPath;
      fallbackLink.href = pdfPath;

      try {
        const res = await fetch(pdfPath, { method: 'HEAD', cache: 'no-store' });
        if (!res.ok) throw new Error('HTTP ' + res.status);
        obj.data = pdfPath;
        hint.textContent = 'Listo. Si no ves el visor, usa “Abrir en pestaña nueva”.';
      } catch (e) {
        obj.data = ''; // forzar fallback
        hint.textContent = 'No embebible o no encontrado. Usa “Abrir en pestaña nueva”.';
      }
      window.scrollTo({ top: wrap.offsetTop, behavior: 'smooth' });
    }

    document.querySelectorAll('.btn[data-pdf]').forEach(b=>{
      b.addEventListener('click', ev=>{
        ev.preventDefault();
        const path = b.getAttribute('data-pdf');
        show(path);
      });
    });
  </script>
</body>
</html>
