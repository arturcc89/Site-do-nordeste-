<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Nordeste — Tela Principal</title>
  <style>
    :root{--accent:#ff6b35;--bg:#0f1720}
    *{box-sizing:border-box}
    body{
      margin:0;
      font-family:Inter,system-ui,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
      background:linear-gradient(180deg,#071028 0%,#092033 100%);
      color:#e6eef8;
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:24px
    }
    .container{
      width:100%;
      max-width:960px;
      text-align:center
    }
    h1{
      font-size:28px;
      margin-bottom:20px
    }
    .grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
      gap:20px
    }
    .card{
      background:rgba(255,255,255,0.03);
      border-radius:16px;
      padding:20px;
      border:1px solid rgba(255,255,255,0.06);
      box-shadow:0 6px 18px rgba(0,0,0,0.5)
    }
    h2{margin:0 0 8px;color:var(--accent)}
    p{margin:0 0 14px;color:rgba(230,238,248,0.85)}
    a.btn{
      display:inline-block;
      padding:10px 16px;
      border-radius:10px;
      background:var(--accent);
      color:#071022;
      text-decoration:none;
      font-weight:600
    }
    footer{
      margin-top:24px;
      font-size:13px;
      opacity:0.7
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Conheça o Nordeste</h1>

    <div class="grid">
      <div class="card">
        <h2>História</h2>
        <p>Eventos coloniais, revoltas e símbolos culturais.</p>
        <!-- Link para a página de história -->
        <a class="btn" href="historia.html">Ver História</a>
      </div>

      <div class="card">
        <h2>Principais Artistas</h2>
        <p>Músicos, escritores e atores famosos do Nordeste.</p>
        <a class="btn" href="#">Em breve</a>
      </div>

      <div class="card">
        <h2>Curiosidades</h2>
        <p>Biomas, comidas típicas e festas populares.</p>
        <a class="btn" href="#">Em breve</a>
      </div>
    </div>

    <footer>
      Feito com ♥ — salve este arquivo como <strong>index.html</strong> no mesmo lugar que <strong>historia.html</strong>.
    </footer>
  </div>
</body>
</html>
