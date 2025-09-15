<!doctype html>

<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Nordeste — Escolha uma seção</title>
  <style>
    :root{--accent:#ff6b35;--bg:#0f1720;--card:#0b1220;--glass:rgba(255,255,255,0.04)}
    *{box-sizing:border-box}
    body{margin:0;font-family:Inter,system-ui,Segoe UI,Roboto,Helvetica,Arial,sans-serif;background:linear-gradient(180deg,#071028 0%,#092033 100%);color:#e6eef8;min-height:100vh;display:flex;align-items:center;justify-content:center;padding:24px}
    .container{width:100%;max-width:980px}
    header{display:flex;align-items:center;gap:16px;margin-bottom:28px}
    .logo{width:64px;height:64px;border-radius:12px;background:linear-gradient(135deg,var(--accent),#ff9a56);display:flex;align-items:center;justify-content:center;font-weight:700;color:#08212a}
    h1{font-size:20px;margin:0}
    p.lead{margin:6px 0 0;opacity:0.9}.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:18px}
.card{background:linear-gradient(180deg,rgba(255,255,255,0.02),rgba(0,0,0,0.06));border-radius:16px;padding:20px;backdrop-filter:blur(6px);box-shadow:0 6px 18px rgba(2,6,23,0.6);border:1px solid rgba(255,255,255,0.03)}
.card h2{margin:0 0 8px;font-size:18px}
.card p{margin:0 0 14px;color:rgba(230,238,248,0.85)}
.actions{display:flex;gap:10px;flex-wrap:wrap}
.btn{appearance:none;border:0;padding:10px 14px;border-radius:10px;font-weight:600;cursor:pointer}
.btn-primary{background:var(--accent);color:#071022}
.btn-outline{background:transparent;border:1px solid rgba(255,255,255,0.06);color:inherit}

footer{margin-top:18px;text-align:center;color:rgba(230,238,248,0.6);font-size:13px}

/* state selector line */
.state-row{display:flex;gap:10px;margin-top:18px;align-items:center}
select{padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit}

@media (max-width:420px){h1{font-size:18px}.logo{width:56px;height:56px}}

  </style>
</head>
<body>
  <div class="container" role="main">
    <header>
      <div class="logo">NE</div>
      <div>
        <h1>Conheça o Nordeste</h1>
        <p class="lead">Escolha o tipo de conteúdo que você quer ver — História, Artistas ou Curiosidades.</p>
      </div>
    </header><section class="grid">
  <article class="card" aria-labelledby="historia-title">
    <h2 id="historia-title">História</h2>
    <p>Linhas do tempo, eventos coloniais, revoltas e figuras históricas que moldaram a região.</p>
    <div class="actions">
      <a class="btn btn-primary" href="historia.html">Ir para História</a>
      <button class="btn btn-outline" onclick="preview('historia')">Visualizar resumo</button>
    </div>
  </article>

  <article class="card" aria-labelledby="artistas-title">
    <h2 id="artistas-title">Principais artistas</h2>
    <p>Listas de músicos, escritores, atores e personalidades. Ex.: Luiz Gonzaga, Ivete Sangalo, Wesley Safadão.</p>
    <div class="actions">
      <a class="btn btn-primary" href="artistas.html">Ir para Artistas</a>
      <button class="btn btn-outline" onclick="preview('artistas')">Visualizar resumo</button>
    </div>
  </article>

  <article class="card" aria-labelledby="curiosidades-title">
    <h2 id="curiosidades-title">Curiosidades</h2>
    <p>Biomas, culinária, festas populares e curiosidades culturais do Nordeste.</p>
    <div class="actions">
      <a class="btn btn-primary" href="curiosidades.html">Ir para Curiosidades</a>
      <button class="btn btn-outline" onclick="preview('curiosidades')">Visualizar resumo</button>
    </div>
  </article>
</section>

<div class="state-row">
  <label for="state">Escolha um estado (opcional):</label>
  <select id="state" onchange="goState(this.value)">
    <option value="">Todos os estados</option>
    <option value="al">Alagoas</option>
    <option value="ba">Bahia</option>
    <option value="ce">Ceará</option>
    <option value="ma">Maranhão</option>
    <option value="pb">Paraíba</option>
    <option value="pe">Pernambuco</option>
    <option value="pi">Piauí</option>
    <option value="rn">Rio Grande do Norte</option>
    <option value="se">Sergipe</option>
  </select>
  <button class="btn btn-outline" onclick="filterByState()">Filtrar</button>
</div>

<footer>Feito com ♥ — copie este arquivo para o seu repositório no GitHub como <strong>index.html</strong>.</footer>

  </div>  <script>
    function preview(section){
      const messages = {
        historia: 'Ex.: Invasões holandesas, Quilombo dos Palmares, Canudos — clique em "Ir para História" para ver a página completa.',
        artistas: 'Ex.: Luiz Gonzaga (PE), Ivete Sangalo (BA), Wesley Safadão (CE) — clique em "Ir para Artistas" para ver listas por estado.',
        curiosidades: 'Ex.: Caatinga (bioma), pratos como acarajé e baião de dois, festas como São João e Carnaval de Salvador.'
      };
      alert(messages[section] || 'Resumo indisponível');
    }

    function goState(code){
      // placeholder: em sites reais você poderia navegar para e.g. artistas.html?state=pe
      console.log('estado selecionado:', code);
    }

    function filterByState(){
      const v = document.getElementById('state').value;
      if(!v) return alert('Mostrando conteúdo para todos os estados.');
      alert('Vai filtrar pelo estado: ' + v.toUpperCase());
    }
  </script></body>
</html>
