# Italy-checklist
Checklist to Italy 
<!DOCTYPE html>
<html lang="cs">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Itálie 🇮🇹 Checklist</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Lato:wght@300;400;700&display=swap');
  :root {
    --green: #2d6a4f; --green-light: #52b788; --cream: #fefae0;
    --red: #c1121f; --gold: #e9c46a; --dark: #1b1b1b; --gray: #6b7280; --card: #ffffff;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: 'Lato', sans-serif; background: var(--cream); color: var(--dark); min-height: 100vh; padding: 0 0 60px; }
  header { background: var(--green); color: white; padding: 28px 24px 20px; position: relative; overflow: hidden; }
  header::after { content: '🇮🇹'; position: absolute; right: 20px; top: 14px; font-size: 52px; opacity: 0.25; }
  header h1 { font-family: 'Playfair Display', serif; font-size: 28px; }
  header p { font-size: 13px; font-weight: 300; opacity: 0.85; margin-top: 4px; }
  .progress-bar-wrap { background: rgba(255,255,255,0.2); border-radius: 99px; height: 8px; margin-top: 14px; overflow: hidden; }
  .progress-bar { height: 100%; background: var(--gold); border-radius: 99px; transition: width 0.4s ease; width: 0%; }
  .progress-label { font-size: 11px; opacity: 0.8; margin-top: 5px; text-align: right; }
  .tabs { display: flex; background: white; border-bottom: 2px solid #e5e7eb; overflow-x: auto; scrollbar-width: none; position: sticky; top: 0; z-index: 10; }
  .tab { padding: 12px 16px; font-size: 12px; font-weight: 700; text-transform: uppercase; letter-spacing: 0.8px; color: var(--gray); cursor: pointer; border-bottom: 3px solid transparent; white-space: nowrap; transition: all 0.2s; }
  .tab.active { color: var(--green); border-bottom-color: var(--green); }
  .section { display: none; padding: 16px; }
  .section.active { display: block; }
  .category { background: var(--card); border-radius: 14px; margin-bottom: 14px; overflow: hidden; box-shadow: 0 1px 4px rgba(0,0,0,0.07); }
  .cat-header { padding: 12px 16px; font-family: 'Playfair Display', serif; font-size: 16px; color: white; display: flex; align-items: center; gap: 8px; }
  .cat-header.zelena { background: var(--green); } .cat-header.cervena { background: var(--red); } .cat-header.zlata { background: #b5851b; } .cat-header.modra { background: #1d4e89; }
  .item { display: flex; align-items: center; gap: 12px; padding: 11px 16px; border-bottom: 1px solid #f3f4f6; cursor: pointer; transition: background 0.15s; -webkit-tap-highlight-color: transparent; }
  .item:last-child { border-bottom: none; }
  .checkbox { width: 22px; height: 22px; border-radius: 6px; border: 2px solid #d1d5db; flex-shrink: 0; display: flex; align-items: center; justify-content: center; transition: all 0.2s; background: white; }
  .item.checked .checkbox { background: var(--green-light); border-color: var(--green-light); }
  .item.checked .checkbox::after { content: '✓'; color: white; font-size: 13px; font-weight: 700; }
  .item.checked .item-text { text-decoration: line-through; color: #9ca3af; }
  .item-text { font-size: 14px; line-height: 1.4; transition: color 0.2s; }
  .badge-new { margin-left: auto; background: var(--red); color: white; font-size: 9px; font-weight: 700; padding: 2px 6px; border-radius: 99px; flex-shrink: 0; }
  .tip-box { background: #e8f5e9; border-left: 4px solid var(--green-light); border-radius: 8px; padding: 12px 14px; font-size: 13px; color: #2d5a3d; margin-bottom: 14px; line-height: 1.5; }
</style>
</head>
<body>
<header>
  <h1>Itálie – 10 dní ☀️</h1>
  <p>8 lidí · apartmán · checklist</p>
  <div class="progress-bar-wrap"><div class="progress-bar" id="progressBar"></div></div>
  <div class="progress-label" id="progressLabel">0 / 0 zabaleno</div>
</header>
<div class="tabs">
  <div class="tab active" onclick="showTab('muj')">📋 Můj seznam</div>
  <div class="tab" onclick="showTab('tipy')">💡 Tipy navíc</div>
</div>
<div class="section active" id="muj">
  <div class="category"><div class="cat-header zelena">📄 Doklady & peníze</div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Doklady</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Eura</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Itinerář</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Nákupní tašky</div></div>
  </div>
  <div class="category"><div class="cat-header zelena">👕 Oblečení</div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Dlouhé šaty</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Svetřík / dlouhé šory</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Lehká bunda / pláštěnka</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Pokrývka hlavy</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Plavky</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Boty do moře</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Žabky / pantofle</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Dešník</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Společenské oblečení na večeři</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Pohodlné boty na dlažbu</div></div>
  </div>
  <div class="category"><div class="cat-header zelena">🧴 Hygiena & krása</div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Hygiena (zubní atd.)</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Deodorant</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Krém na obličej</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Opalovák + po opalování</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Make-up</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Manikúra / štipátko</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Hřeben, gumičky</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Tyčinky do uší</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Vložky, intimky</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Chladící vložky</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Dezinfekce na ruce / normální</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Mast na nohy</div></div>
  </div>
  <div class="category"><div class="cat-header cervena">💊 Zdraví & lékárna</div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Léky – Fenistil</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Psiolobalzám</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Bepanthen</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Lékárnička</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Žaludeční kapky / Algifen</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Náplasti</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Pytlíky na blinkání</div></div>
  </div>
  <div class="category"><div class="cat-header modra">📱 Technika & ostatní</div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Konta, tablet, sluchátka</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Nabíječky, powerbank</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Kartáček na zuby, pasta</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Ručníky (rychleschnoucí)</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Polštářek</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Síťka</div></div>
  </div>
  <div class="category"><div class="cat-header zelena">🏖️ Pláž & bazén</div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Plavky (záložní pár)</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Pikniková deka + kulatá deka</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Plovací brýle, kruh</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Kyblíček</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Vějíř</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Sluneční brýle</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Plážová taška (velká, voděodolná)</div></div>
  </div>
  <div class="category"><div class="cat-header zlata">🍝 Jídlo & pití</div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Kafe, cukr, sůl, pepř</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Voda na cestu</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Rizoto</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Nom nom (svačiny / pamlsky)</div></div>
  </div>
</div>
<div class="section" id="tipy">
  <div class="tip-box"><strong>☀️ Na 10 dní v létě v Itálii doporučuji:</strong> Itálie bývá velmi horká – nezapomeň na silný opalovák (SPF 50+) a velkou lahev vody vždy u sebe.</div>
  <div class="category"><div class="cat-header cervena">🏠 Apartmán pro 8 lidí</div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Mycí prostředky na nádobí</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Houbičky, utěrky</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Toaletní papír zásoby</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Kávovaru filtry / kapsle</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Adaptér (Itálie – typ F/L)</div></div>
  </div>
  <div class="category"><div class="cat-header modra">🌡️ Horko & komfort</div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Repelent proti komárům</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Náramky / nálepky proti komárům</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Chladicí sprej na tělo</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Lehký šátek / pareo</div></div>
  </div>
  <div class="category"><div class="cat-header zlata">📸 Zábava & výlety</div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Stažené mapy offline</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Karty / stolní hra na večery</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Vodotěsné pouzdro na telefon</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Ledvinka / taška přes rameno</div></div>
  </div>
  <div class="category"><div class="cat-header cervena">💊 Zdraví navíc</div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Průjmové léky</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Ibalgin / Paralen</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Rehydratační sáčky</div></div>
    <div class="item" onclick="toggle(this)"><div class="checkbox"></div><div class="item-text">Pojistná karta (EHIC) – nutnost!</div></div>
  </div>
</div>
<script>
  function toggle(el) { el.classList.toggle('checked'); updateProgress(); }
  function showTab(id) {
    document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
    document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
    document.getElementById(id).classList.add('active');
    event.target.classList.add('active');
    updateProgress();
  }
  function updateProgress() {
    const all = document.querySelectorAll('.item');
    const checked = document.querySelectorAll('.item.checked');
    const pct = all.length ? (checked.length / all.length * 100) : 0;
    document.getElementById('progressBar').style.width = pct + '%';
    document.getElementById('progressLabel').textContent = checked.length + ' / ' + all.length + ' zabaleno';
  }
  updateProgress();
</script>
</body>
</html>
