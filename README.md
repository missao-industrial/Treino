# Treino
ficha de treino
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Treino Fê Linard</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:ital,wght@0,300;0,400;0,500;0,700;1,300&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0a0a0a;
    --surface: #141414;
    --card: #1c1c1c;
    --border: #2a2a2a;
    --accent: #d4f542;
    --accent2: #f5a342;
    --text: #f0f0f0;
    --muted: #888;
    --radius: 12px;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    font-size: 15px;
    line-height: 1.6;
  }

  /* HERO */
  .hero {
    background: var(--surface);
    border-bottom: 1px solid var(--border);
    padding: 60px 40px 50px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse 80% 60% at 50% 0%, rgba(212,245,66,0.07) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-label {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 14px;
  }
  .hero h1 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(52px, 8vw, 96px);
    letter-spacing: 3px;
    line-height: 0.95;
    color: var(--text);
  }
  .hero h1 span { color: var(--accent); }
  .hero-sub {
    margin-top: 18px;
    color: var(--muted);
    font-size: 14px;
    font-weight: 300;
    letter-spacing: 1px;
  }

  /* META STRIP */
  .meta-strip {
    display: flex;
    justify-content: center;
    gap: 0;
    border-bottom: 1px solid var(--border);
    background: var(--surface);
  }
  .meta-item {
    flex: 1;
    max-width: 220px;
    padding: 22px 20px;
    text-align: center;
    border-right: 1px solid var(--border);
  }
  .meta-item:last-child { border-right: none; }
  .meta-value {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 32px;
    color: var(--accent);
    line-height: 1;
  }
  .meta-label {
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-top: 4px;
  }

  /* HIIT BANNER */
  .hiit-banner {
    margin: 36px 40px;
    background: var(--card);
    border: 1px solid var(--accent);
    border-left: 4px solid var(--accent);
    border-radius: var(--radius);
    padding: 20px 28px;
    display: flex;
    align-items: center;
    gap: 18px;
  }
  .hiit-icon {
    font-size: 32px;
    flex-shrink: 0;
  }
  .hiit-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 20px;
    letter-spacing: 2px;
    color: var(--accent);
    margin-bottom: 3px;
  }
  .hiit-desc { font-size: 13px; color: var(--muted); }

  /* SECTION */
  .section {
    padding: 0 40px 60px;
  }
  .section-header {
    display: flex;
    align-items: flex-end;
    gap: 18px;
    padding: 40px 0 28px;
    border-bottom: 1px solid var(--border);
    margin-bottom: 32px;
  }
  .section-letter {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 80px;
    line-height: 1;
    color: var(--accent);
    opacity: 0.15;
    position: relative;
  }
  .section-info { flex: 1; }
  .section-tag {
    font-size: 10px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--accent);
    font-weight: 700;
    margin-bottom: 4px;
  }
  .section-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 36px;
    letter-spacing: 2px;
    color: var(--text);
    line-height: 1;
  }
  .section-muscles {
    font-size: 12px;
    color: var(--muted);
    margin-top: 6px;
    font-weight: 300;
  }
  .section-count {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 48px;
    color: var(--border);
    line-height: 1;
  }

  /* EXERCISE GRID */
  .exercise-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
    gap: 20px;
  }

  /* EXERCISE CARD */
  .ex-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    overflow: hidden;
    transition: border-color 0.2s, transform 0.2s;
  }
  .ex-card:hover {
    border-color: rgba(212,245,66,0.3);
    transform: translateY(-2px);
  }
  .ex-img-wrap {
    position: relative;
    height: 200px;
    overflow: hidden;
    background: #111;
  }
  .ex-img-wrap img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center top;
    display: block;
    transition: transform 0.4s ease;
  }
  .ex-card:hover .ex-img-wrap img {
    transform: scale(1.04);
  }
  .ex-num {
    position: absolute;
    top: 12px;
    left: 12px;
    background: var(--accent);
    color: #000;
    font-family: 'Bebas Neue', sans-serif;
    font-size: 15px;
    letter-spacing: 1px;
    padding: 3px 9px;
    border-radius: 4px;
    line-height: 1.4;
  }
  .ex-reps {
    position: absolute;
    bottom: 12px;
    right: 12px;
    background: rgba(0,0,0,0.75);
    backdrop-filter: blur(6px);
    color: var(--accent);
    font-family: 'Bebas Neue', sans-serif;
    font-size: 15px;
    letter-spacing: 1px;
    padding: 4px 10px;
    border-radius: 6px;
    border: 1px solid rgba(212,245,66,0.3);
  }
  .ex-body {
    padding: 18px 20px 20px;
  }
  .ex-name {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 19px;
    letter-spacing: 1px;
    color: var(--text);
    margin-bottom: 10px;
    line-height: 1.1;
  }
  .ex-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-bottom: 12px;
  }
  .ex-tag {
    font-size: 10px;
    font-weight: 600;
    letter-spacing: 1px;
    text-transform: uppercase;
    background: rgba(212,245,66,0.08);
    color: var(--accent);
    border: 1px solid rgba(212,245,66,0.2);
    padding: 3px 8px;
    border-radius: 4px;
  }
  .ex-tag.orange {
    background: rgba(245,163,66,0.08);
    color: var(--accent2);
    border-color: rgba(245,163,66,0.2);
  }
  .ex-instruction {
    font-size: 13px;
    color: #bbb;
    line-height: 1.65;
    font-weight: 300;
  }
  .ex-instruction strong {
    color: var(--text);
    font-weight: 500;
  }
  .ex-tips {
    margin-top: 12px;
    padding-top: 12px;
    border-top: 1px solid var(--border);
  }
  .tip-title {
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--accent2);
    margin-bottom: 6px;
  }
  .tip-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 4px;
  }
  .tip-list li {
    font-size: 12px;
    color: var(--muted);
    padding-left: 14px;
    position: relative;
    font-weight: 300;
  }
  .tip-list li::before {
    content: '→';
    position: absolute;
    left: 0;
    color: var(--accent2);
    font-size: 10px;
    top: 2px;
  }

  /* FOOTER */
  footer {
    text-align: center;
    padding: 40px 20px;
    border-top: 1px solid var(--border);
    color: var(--muted);
    font-size: 12px;
    letter-spacing: 1px;
  }

  @media (max-width: 600px) {
    .hero { padding: 40px 20px 36px; }
    .section { padding: 0 16px 48px; }
    .hiit-banner { margin: 24px 16px; }
    .exercise-grid { grid-template-columns: 1fr; }
    .meta-strip { flex-wrap: wrap; }
    .meta-item { min-width: 50%; }
  }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="hero-label">Ficha de Treino Personalizada</div>
  <h1>TREINO<br><span>FÊ LINARD</span></h1>
  <p class="hero-sub">4× por semana · Treino A + Treino B · HIIT na Escada</p>
</div>

<!-- META -->
<div class="meta-strip">
  <div class="meta-item">
    <div class="meta-value">4×</div>
    <div class="meta-label">Por Semana</div>
  </div>
  <div class="meta-item">
    <div class="meta-value">20'</div>
    <div class="meta-label">HIIT Escada</div>
  </div>
  <div class="meta-item">
    <div class="meta-value">21</div>
    <div class="meta-label">Exercícios</div>
  </div>
  <div class="meta-item">
    <div class="meta-value">A+B</div>
    <div class="meta-label">Divisão</div>
  </div>
</div>

<!-- HIIT BANNER -->
<div class="hiit-banner">
  <div class="hiit-icon">⚡</div>
  <div>
    <div class="hiit-title">HIIT NA ESCADA — 20 MINUTOS</div>
    <div class="hiit-desc">Alternar <strong style="color:#f0f0f0">1 minuto intenso</strong> com <strong style="color:#f0f0f0">1 minuto leve</strong>. Realizar antes ou após o treino de musculação. Foco em subir e descer escadas em ritmos alternados para máximo gasto calórico e condicionamento cardiovascular.</div>
  </div>
</div>

<!-- ===== TREINO A ===== -->
<div class="section">
  <div class="section-header">
    <div class="section-letter">A</div>
    <div class="section-info">
      <div class="section-tag">Treino A</div>
      <div class="section-title">QUADRÍCEPS · BÍCEPS<br>OMBRO (FRENTE) · PEITORAL</div>
      <div class="section-muscles">10 exercícios · Foco anterior</div>
    </div>
    <div class="section-count">10</div>
  </div>

  <div class="exercise-grid">

    <!-- 1 -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/3FGbkiSJHqM/maxresdefault.jpg" alt="Agachamento no Smith" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Agachamento+Smith'">
        <span class="ex-num">01</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">AGACHAMENTO NO SMITH<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Pés paralelos ao quadril</small></div>
        <div class="ex-tags">
          <span class="ex-tag">Quadríceps</span>
          <span class="ex-tag">Glúteos</span>
          <span class="ex-tag orange">Smith Machine</span>
        </div>
        <div class="ex-instruction">
          Posicione os pés na largura dos quadris, diretamente abaixo da barra. <strong>Desça controlando o movimento</strong> até as coxas ficarem paralelas ao chão (90°), mantendo o joelho alinhado com o segundo dedo do pé. Suba expirando e contraindo os glúteos no topo.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Mantenha o core contraído durante todo o movimento</li>
            <li>Não deixe os joelhos colapsarem para dentro</li>
            <li>Peso no meio do pé, não nas pontas</li>
            <li>Olhar levemente para cima ou à frente</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 2 -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/WpA_sJsJlYM/maxresdefault.jpg" alt="Rosca Corda Polia Alta" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Rosca+Corda+Polia'">
        <span class="ex-num">02</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">ROSCA T C/ CORDA<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Na polia alta</small></div>
        <div class="ex-tags">
          <span class="ex-tag">Bíceps</span>
          <span class="ex-tag orange">Polia Alta</span>
        </div>
        <div class="ex-instruction">
          De frente para a polia, segure a corda com ambas as mãos em posição supinada. <strong>Flexione os cotovelos trazendo os punhos em direção à testa</strong>, mantendo os cotovelos fixos na altura dos ombros. O movimento em "T" cria tensão constante no bíceps durante toda a amplitude.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Cotovelos estáticos — não balancem o tronco</li>
            <li>Desça a corda devagar (fase excêntrica = 2 seg)</li>
            <li>Puxe até os punhos chegarem perto da testa</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 3 -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/soxrZlIl35U/maxresdefault.jpg" alt="Rosca Alternada com Rotação" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Rosca+Alternada'">
        <span class="ex-num">03</span>
        <span class="ex-reps">4 × 8 (cada lado)</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">ROSCA ALTERNADA<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Com rotação do punho</small></div>
        <div class="ex-tags">
          <span class="ex-tag">Bíceps</span>
          <span class="ex-tag">Braquial</span>
          <span class="ex-tag orange">Halteres</span>
        </div>
        <div class="ex-instruction">
          Em pé ou sentada, segure os halteres com a palma voltada para o corpo (pegada neutra). <strong>Ao subir, gire o punho para fora</strong> (supinação) de forma que a palma fique voltada para cima no topo. Alternando um braço de cada vez. A rotação ativa a cabeça longa do bíceps com mais intensidade.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>A rotação começa na metade do movimento</li>
            <li>Cotovelos próximos ao corpo, sem abrir</li>
            <li>Contrair no topo por 1 segundo</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 4 -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/YyvSfVjQeL0/maxresdefault.jpg" alt="Cadeira Extensora Unilateral" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Cadeira+Extensora'">
        <span class="ex-num">04</span>
        <span class="ex-reps">4 × 8 (cada lado)</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">CADEIRA EXTENSORA<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Unilateral</small></div>
        <div class="ex-tags">
          <span class="ex-tag">Quadríceps</span>
          <span class="ex-tag orange">Máquina</span>
        </div>
        <div class="ex-instruction">
          Sente-se ajustando o encosto para a coxa estar bem apoiada. Coloque apenas uma perna no suporte. <strong>Estenda o joelho completamente</strong>, contraindo o quadríceps no topo. Desça de forma controlada sem deixar cair o peso. Trabalho unilateral corrige desequilíbrios musculares.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Sem inclinar o tronco ao levantar</li>
            <li>Desça em 3 segundos (fase excêntrica)</li>
            <li>Sempre começar pelo lado mais fraco</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 5 -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/sVkwuVDdKCA/maxresdefault.jpg" alt="Elevação Frontal com Barra" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Elevação+Frontal+Barra'">
        <span class="ex-num">05</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">ELEVAÇÃO FRONTAL<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Com barra — Ombro frente</small></div>
        <div class="ex-tags">
          <span class="ex-tag">Deltóide Anterior</span>
          <span class="ex-tag orange">Barra</span>
        </div>
        <div class="ex-instruction">
          Em pé, segure a barra com pegada pronada (palmas para baixo) na largura dos ombros. <strong>Eleve a barra à frente do corpo</strong> até a altura dos ombros (ou levemente acima). Desça com controle. Não balance o tronco — o movimento deve ser isolado no ombro.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Joelhos levemente flexionados, core ativo</li>
            <li>Não use momentum: movimento lento e controlado</li>
            <li>Evite subir acima da linha do ombro</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 6 -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/5BpBHGQ8TJE/maxresdefault.jpg" alt="Sissy Squat" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Sissy+Squat'">
        <span class="ex-num">06</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">SISSY SQUAT<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Ajoelhado no colchonete</small></div>
        <div class="ex-tags">
          <span class="ex-tag">Quadríceps</span>
          <span class="ex-tag">Reto Femoral</span>
          <span class="ex-tag orange">Peso Corporal</span>
        </div>
        <div class="ex-instruction">
          Ajoelhada no colchonete, mantenha o tronco ereto. <strong>Incline o corpo para trás controladamente</strong>, deixando os joelhos avançarem na direção do chão. Retorne à posição inicial contraindo o quadríceps. A variação ajoelhada reduz o impacto no joelho e foca no reto femoral.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Colchonete é essencial para proteger os joelhos</li>
            <li>Mantenha quadril em extensão (não deixe cair)</li>
            <li>Avance gradualmente na amplitude com o tempo</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 7 -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/gRVjAtPip0Y/maxresdefault.jpg" alt="Supino Máquina" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Supino+Máquina'">
        <span class="ex-num">07</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">SUPINO MÁQUINA<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Ou com halteres</small></div>
        <div class="ex-tags">
          <span class="ex-tag">Peitoral</span>
          <span class="ex-tag">Tríceps</span>
          <span class="ex-tag orange">Máquina / Halteres</span>
        </div>
        <div class="ex-instruction">
          Deitada ou sentada (dependendo da máquina), posicione as mãos na largura dos ombros. <strong>Empurre para frente até os cotovelos quase estenderem</strong>, sem travar. Volte controlando. Com halteres: deitar no banco, descer os halteres até o nível do peito com cotovelos a 45°.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Escápulas retraídas e deprimidas (ombros "em baixo")</li>
            <li>Não trave o cotovelo no topo do movimento</li>
            <li>Pressione o peito ao expirar</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 8 -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/taI4XduLpTk/maxresdefault.jpg" alt="Crucifixo no Cross" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Crucifixo+Cross'">
        <span class="ex-num">08</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">CRUCIFIXO NO CROSS<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Polia — Peitoral</small></div>
        <div class="ex-tags">
          <span class="ex-tag">Peitoral</span>
          <span class="ex-tag">Deltóide Anterior</span>
          <span class="ex-tag orange">Cross / Polia</span>
        </div>
        <div class="ex-instruction">
          Posicione-se no centro do cross com as polias na altura dos ombros (ou acima). Segure os cabos e avance um passo. <strong>Traga os braços à frente em arco</strong>, cruzando levemente as mãos na frente do peito. Abra controlando. Mantenha cotovelos levemente flexionados durante todo o movimento.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Polia alta = foco na porção inferior do peitoral</li>
            <li>Polia baixa = foco na porção superior</li>
            <li>Não balance — mantenha tronco estável</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 9 -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/FeJnFO3BSLE/maxresdefault.jpg" alt="Elevação Lateral Simultânea" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Elevação+Lateral'">
        <span class="ex-num">09</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">ELEVAÇÃO LATERAL<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Simultânea c/ halteres</small></div>
        <div class="ex-tags">
          <span class="ex-tag">Deltóide Lateral</span>
          <span class="ex-tag orange">Halteres</span>
        </div>
        <div class="ex-instruction">
          Em pé, segure os halteres ao lado do corpo. Com cotovelos levemente flexionados, <strong>eleve os braços lateralmente</strong> até a altura dos ombros. O cotovelo lidera o movimento. Desça de forma controlada. Evite subir acima da linha do ombro para não sobrecarregar o trapézio.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Incline levemente o halter (polegar levemente abaixo)</li>
            <li>Use cargas leves com boa forma — esse músculo é pequeno</li>
            <li>Fase excêntrica lenta: 3 segundos descendo</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 10 -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/Xyd_fa5zoEU/maxresdefault.jpg" alt="Abs Supra" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Abdominal+Supra'">
        <span class="ex-num">10</span>
        <span class="ex-reps">4 × 20</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">ABS SUPRA<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Crunch supraumbilical</small></div>
        <div class="ex-tags">
          <span class="ex-tag">Reto Abdominal</span>
          <span class="ex-tag">Core</span>
          <span class="ex-tag orange">Peso Corporal</span>
        </div>
        <div class="ex-instruction">
          Deitada com joelhos dobrados e pés no chão. Mãos atrás da cabeça sem puxar o pescoço. <strong>Eleve apenas os ombros e escápulas do chão</strong> — o lombar permanece apoiado. Contraia o abdômen no topo, expire e desça controlando. Movimento pequeno e eficaz focado no reto abdominal superior.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Olhar para o teto, não para os joelhos</li>
            <li>Não puxe a cabeça com as mãos</li>
            <li>Lombar sempre em contato com o chão</li>
          </ul>
        </div>
      </div>
    </div>

  </div><!-- /exercise-grid A -->
</div><!-- /section A -->

<!-- ===== TREINO B ===== -->
<div class="section">
  <div class="section-header">
    <div class="section-letter" style="color:var(--accent2);opacity:0.15">B</div>
    <div class="section-info">
      <div class="section-tag" style="color:var(--accent2)">Treino B</div>
      <div class="section-title">POSTERIORES · DORSAIS<br>GLÚTEOS · LOMBAR · TRÍCEPS</div>
      <div class="section-muscles">11 exercícios · Foco posterior</div>
    </div>
    <div class="section-count">11</div>
  </div>

  <div class="exercise-grid">

    <!-- 1B -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/NTdvkCdFXBs/maxresdefault.jpg" alt="Agachamento Sumô Smith" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Agachamento+Sumô'">
        <span class="ex-num" style="background:var(--accent2)">01</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">AGACHAMENTO NO SMITH<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Posição sumô — glúteos</small></div>
        <div class="ex-tags">
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Glúteos</span>
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Adutores</span>
          <span class="ex-tag orange">Smith Machine</span>
        </div>
        <div class="ex-instruction">
          Pés afastados além da largura dos ombros, com pontas voltadas para fora (45°). <strong>Desça mantendo o tronco ereto</strong> e os joelhos apontados na direção dos pés. O agachamento sumô recruta mais glúteos e adutores. Suba espremendo os glúteos no topo do movimento.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Joelhos não podem colapsar para dentro</li>
            <li>Desça até as coxas ficarem paralelas ao chão</li>
            <li>Apertar os glúteos no topo para maior ativação</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 2B -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/9JC1EKwYJEo/maxresdefault.jpg" alt="Puxada Unilateral Pulley" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Puxada+Unilateral'">
        <span class="ex-num" style="background:var(--accent2)">02</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">PUXADA UNILATERAL<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">No pulley — pegada neutra</small></div>
        <div class="ex-tags">
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Grande Dorsal</span>
          <span class="ex-tag orange">Pulley</span>
        </div>
        <div class="ex-instruction">
          Com a alça unilateral, puxe de cima para baixo com um braço de cada vez. <strong>Inicie o movimento deprimindo a escápula</strong> (ombro para baixo) e depois flexione o cotovelo, trazendo-o em direção ao quadril. Pegada neutra (palma para dentro) aumenta o range de movimento.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Inicie com o ombro — não com o cotovelo</li>
            <li>Leve inclinação do tronco para trás é normal</li>
            <li>Contrair o dorsal ao trazer o cotovelo ao lado do corpo</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 3B -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/G8l_8chR5BE/maxresdefault.jpg" alt="Remada Curvada Supinada" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Remada+Curvada'">
        <span class="ex-num" style="background:var(--accent2)">03</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">REMADA CURVADA<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Na barra — pegada supinada</small></div>
        <div class="ex-tags">
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Dorsais</span>
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Bíceps</span>
          <span class="ex-tag orange">Barra</span>
        </div>
        <div class="ex-instruction">
          Com pegada supinada (palmas para cima), incline o tronco a 45° e <strong>puxe a barra em direção ao umbigo</strong>. Cotovelos ficam próximos ao corpo. A pegada supinada enfatiza o grande dorsal inferior e recruta mais bíceps em relação à pegada pronada.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Tronco paralelo ao chão (ou perto disso)</li>
            <li>Não curve demais a lombar — core ativo</li>
            <li>Escápulas juntas no topo do movimento</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 4B -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/D7KaRcUTQeE/maxresdefault.jpg" alt="Avanço com Halteres" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Avanço+Halteres'">
        <span class="ex-num" style="background:var(--accent2)">04</span>
        <span class="ex-reps">4 × 20</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">AVANÇO<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Caminhando com halteres</small></div>
        <div class="ex-tags">
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Glúteos</span>
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Quadríceps</span>
          <span class="ex-tag orange">Halteres</span>
        </div>
        <div class="ex-instruction">
          Com halteres nas mãos, dê um passo largo à frente. <strong>Desça o joelho de trás próximo ao chão</strong> sem tocar. O joelho da frente não deve ultrapassar muito a ponta do pé. Empurre o pé da frente para avançar com a outra perna. Alternando as pernas pela sala.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Tronco ereto — não incline para frente</li>
            <li>Passo largo o suficiente para ângulo de 90° no joelho</li>
            <li>20 repetições = 10 de cada perna</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 5B -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/0TMgMB9ZCWU/maxresdefault.jpg" alt="Remada no Cross Corda" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Remada+Cross+Corda'">
        <span class="ex-num" style="background:var(--accent2)">05</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">REMADA NO CROSS<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">C/ corda na polia alta</small></div>
        <div class="ex-tags">
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Dorsais</span>
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Romboides</span>
          <span class="ex-tag orange">Polia Alta</span>
        </div>
        <div class="ex-instruction">
          De frente para a polia alta com a corda. Em pé ou levemente inclinada, <strong>puxe a corda em direção ao peito/queixo</strong>, separando as pontas da corda ao chegar perto do rosto. Cotovelos viajam para trás. Foco nas escápulas se juntando.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Separe as pontas da corda no final do movimento</li>
            <li>Puxe com os cotovelos, não com as mãos</li>
            <li>Mantenha o core firme — não balance</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 6B -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/ttvAwiDnhLc/maxresdefault.jpg" alt="Crucifixo Invertido no Cross" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Crucifixo+Invertido'">
        <span class="ex-num" style="background:var(--accent2)">06</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">CRUCIFIXO INVERTIDO<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">No cross — posterior</small></div>
        <div class="ex-tags">
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Deltóide Posterior</span>
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Romboides</span>
          <span class="ex-tag orange">Cross</span>
        </div>
        <div class="ex-instruction">
          Polias cruzadas (cabo direito na mão esquerda, e vice-versa). <strong>Abra os braços lateralmente</strong> em arco com cotovelos levemente flexionados. Mantenha o tronco estável, levemente inclinado. Sinta o posterior do ombro trabalhando ao abrir e retornar controlando a carga.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Use carga leve — o deltóide posterior é pequeno</li>
            <li>Cotovelo levemente acima da linha do ombro</li>
            <li>Não use o trapézio para ajudar — mantenha ombros baixos</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 7B -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/vB5OHsJ3EMc/maxresdefault.jpg" alt="Tríceps Corda" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Tríceps+Corda'">
        <span class="ex-num" style="background:var(--accent2)">07</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">TRÍCEPS CORDA<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Polia</small></div>
        <div class="ex-tags">
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Tríceps</span>
          <span class="ex-tag orange">Polia</span>
        </div>
        <div class="ex-instruction">
          De frente para a polia, segure a corda com as duas mãos. <strong>Estenda os cotovelos para baixo</strong>, separando as pontas da corda ao final para maior ativação da cabeça lateral do tríceps. Cotovelos fixos ao lado do corpo durante todo o movimento.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Separe as pontas da corda no final (abre o tríceps)</li>
            <li>Cotovelos não se afastam do corpo</li>
            <li>Postura ereta — não incline o tronco</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 8B -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/0326dy_-CzM/maxresdefault.jpg" alt="Tríceps Banco" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Tríceps+Banco'">
        <span class="ex-num" style="background:var(--accent2)">08</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">TRÍCEPS BANCO<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Dips no banco</small></div>
        <div class="ex-tags">
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Tríceps</span>
          <span class="ex-tag orange">Peso Corporal</span>
        </div>
        <div class="ex-instruction">
          Apoie as mãos no banco atrás de você com os dedos voltados para fora e os cotovelos apontados para trás. <strong>Desça o corpo flexionando os cotovelos até 90°</strong>, mantendo-os paralelos. Empurre para subir. Pernas estendidas para mais dificuldade, dobradas para facilitar.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Cotovelos vão para trás — não para os lados</li>
            <li>Não desça demais para proteger o ombro</li>
            <li>Quadril próximo ao banco durante o movimento</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 9B -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/cc6UVRS7PW4/maxresdefault.jpg" alt="Superhomem Isométrico" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Superman+Isométrico'">
        <span class="ex-num" style="background:var(--accent2)">09</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">SUPERHOMEM ISOMÉTRICO<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Extensão lombar</small></div>
        <div class="ex-tags">
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Lombar</span>
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Glúteos</span>
          <span class="ex-tag orange">Peso Corporal</span>
        </div>
        <div class="ex-instruction">
          Deite de bruços no chão com os braços estendidos à frente. <strong>Eleve simultaneamente braços e pernas do chão</strong>, contraindo glúteos e lombar. Mantenha a posição por 2-3 segundos (isometria) e desça. O movimento fortalece toda a cadeia posterior.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Olhar para o chão — não force o pescoço</li>
            <li>Respire durante a contração isométrica</li>
            <li>Suba apenas o quanto conseguir sem dor lombar</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 10B -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/ASdvN_XEl_c/maxresdefault.jpg" alt="Prancha" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Prancha+Plank'">
        <span class="ex-num" style="background:var(--accent2)">10</span>
        <span class="ex-reps">3 × 45"</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">PRANCHA<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Plank isométrico</small></div>
        <div class="ex-tags">
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Core</span>
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Estabilizadores</span>
          <span class="ex-tag orange">Peso Corporal</span>
        </div>
        <div class="ex-instruction">
          Apoie os antebraços e pontas dos pés no chão. <strong>Mantenha o corpo em linha reta</strong> da cabeça aos calcanhares. Core contraído, glúteos apertados, sem deixar o quadril subir ou cair. Respire normalmente durante os 45 segundos de isometria.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Não deixe o quadril cair — é o erro mais comum</li>
            <li>Olhar para o chão, pescoço neutro</li>
            <li>Aperte glúteos e abdômen simultaneamente</li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 11B -->
    <div class="ex-card">
      <div class="ex-img-wrap">
        <img src="https://i.ytimg.com/vi/1uDiW5--rAE/maxresdefault.jpg" alt="Stiff" onerror="this.src='https://via.placeholder.com/400x200/1c1c1c/888?text=Stiff+Deadlift'">
        <span class="ex-num" style="background:var(--accent2)">11</span>
        <span class="ex-reps">4 × 10</span>
      </div>
      <div class="ex-body">
        <div class="ex-name">STIFF<br><small style="font-size:12px;color:var(--muted);font-family:'DM Sans'">Levantamento terra com pernas retas</small></div>
        <div class="ex-tags">
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Posterior de Coxa</span>
          <span class="ex-tag" style="background:rgba(245,163,66,0.08);color:var(--accent2);border-color:rgba(245,163,66,0.2)">Glúteos</span>
          <span class="ex-tag orange">Barra / Halteres</span>
        </div>
        <div class="ex-instruction">
          Em pé com pés na largura do quadril, segure a barra ou halteres à frente do corpo. <strong>Incline o tronco para frente empurrando o quadril para trás</strong>, mantendo a coluna neutra (sem arredondar). Desça até sentir o alongamento no posterior da coxa. Suba contraindo glúteos e isquiotibiais.
        </div>
        <div class="ex-tips">
          <div class="tip-title">Dicas de Execução</div>
          <ul class="tip-list">
            <li>Coluna sempre neutra — nunca arredonde a lombar</li>
            <li>Barra/halteres deslizam próximos ao corpo</li>
            <li>Joelhos levemente flexionados, não travados</li>
            <li>Sentir o alongamento no posterior = amplitude correta</li>
          </ul>
        </div>
      </div>
    </div>

  </div><!-- /exercise-grid B -->
</div><!-- /section B -->

<footer>
  TREINO FÊ LINARD &nbsp;·&nbsp; 4× POR SEMANA &nbsp;·&nbsp; TREINO A + TREINO B &nbsp;·&nbsp; HIIT NA ESCADA 20'
</footer>

</body>
</html>
