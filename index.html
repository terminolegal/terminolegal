from pathlib import Path
import zipfile, textwrap, json, os

project = Path("/mnt/data/termino-legal-v0.1")
project.mkdir(exist_ok=True)

files = {
"index.html": """<!doctype html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Término Legal — conteo de términos jurídicos." />
  <title>Término Legal | Conteo de términos jurídicos</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <main class="app">
    <header class="brand">
      <div class="brand-mark" aria-hidden="true">
        <span class="mark-t">T</span><span class="mark-l">L</span>
      </div>
      <div>
        <div class="brand-name">TÉRMINO <span>LEGAL</span></div>
        <div class="brand-subtitle">CONTEO DE TÉRMINOS JURÍDICOS</div>
      </div>
    </header>

    <section class="hero">
      <p class="eyebrow">VERSIÓN 0.1</p>
      <h1>Cuenta tu término.</h1>
      <p class="intro">Calcula una fecha de vencimiento usando días hábiles o días calendario.</p>
    </section>

    <section class="card" aria-label="Calculadora de términos">
      <div class="field">
        <label for="startDate">Fecha de inicio</label>
        <input id="startDate" type="date" />
        <small>El conteo inicia el día siguiente a la fecha indicada.</small>
      </div>

      <div class="grid">
        <div class="field">
          <label for="days">Número de días</label>
          <input id="days" type="number" min="1" step="1" placeholder="Ej. 10" />
        </div>

        <div class="field">
          <label>Tipo de término</label>
          <div class="segmented">
            <label><input type="radio" name="termType" value="business" checked><span>Días hábiles</span></label>
            <label><input type="radio" name="termType" value="calendar"><span>Días calendario</span></label>
          </div>
        </div>
      </div>

      <button id="calculateBtn" type="button">CALCULAR TÉRMINO</button>
      <p id="error" class="error" role="alert" hidden></p>
    </section>

    <section id="result" class="result" hidden aria-live="polite">
      <p class="eyebrow">RESULTADO</p>
      <h2 id="resultDate">—</h2>
      <p id="resultSummary" class="result-summary">—</p>
      <div class="details">
        <div><span>Fecha de inicio</span><strong id="detailStart">—</strong></div>
        <div><span>Fecha de vencimiento</span><strong id="detailEnd">—</strong></div>
        <div><span>Tipo de conteo</span><strong id="detailType">—</strong></div>
      </div>
      <p class="notice">Versión 0.1: este cálculo aplica fines de semana para días hábiles. Los festivos, suspensiones de términos y reglas jurídicas especiales se incorporarán en versiones posteriores.</p>
    </section>

    <footer>
      <span>© 2026 TÉRMINO LEGAL</span>
      <span>Calculador jurídico — versión experimental</span>
    </footer>
  </main>
  <script src="app.js"></script>
</body>
</html>
""",

"styles.css": """*{box-sizing:border-box}
:root{--navy:#10243e;--gold:#b9964f;--ink:#17202b;--muted:#687383;--line:#e4e8ed;--bg:#f7f8fa}
body{margin:0;background:var(--bg);color:var(--ink);font-family:Inter,system-ui,-apple-system,BlinkMacSystemFont,"Segoe UI",sans-serif}
.app{width:min(900px,92%);margin:0 auto;padding:34px 0 24px}
.brand{display:flex;align-items:center;gap:14px}
.brand-mark{width:48px;height:48px;border:2px solid var(--navy);border-radius:50%;display:flex;align-items:center;justify-content:center;font-family:Georgia,serif;font-weight:700;letter-spacing:-8px;padding-right:6px}
.mark-t{color:var(--navy);font-size:25px}.mark-l{color:var(--gold);font-size:25px}
.brand-name{font-weight:700;letter-spacing:.14em;font-size:17px;color:var(--navy)}
.brand-name span{color:var(--gold)}
.brand-subtitle{font-size:9px;letter-spacing:.18em;color:var(--muted);margin-top:4px}
.hero{text-align:center;padding:70px 0 38px}
.eyebrow{font-size:10px;letter-spacing:.22em;color:var(--gold);font-weight:700;margin:0 0 12px}
h1{font-family:Georgia,"Times New Roman",serif;font-size:48px;line-height:1.05;color:var(--navy);margin:0 0 15px}
.intro{color:var(--muted);font-size:16px;max-width:580px;margin:auto;line-height:1.6}
.card,.result{background:#fff;border:1px solid var(--line);border-radius:18px;box-shadow:0 12px 35px rgba(16,36,62,.06);padding:30px}
.field{margin-bottom:22px}
label{display:block;font-size:13px;font-weight:600;color:var(--navy);margin-bottom:9px}
input[type=date],input[type=number]{width:100%;height:50px;border:1px solid #ccd3dc;border-radius:10px;padding:0 14px;font:inherit;color:var(--ink);background:#fff}
input:focus{outline:2px solid rgba(185,150,79,.25);border-color:var(--gold)}
small{display:block;color:var(--muted);font-size:11px;margin-top:7px}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:20px}
.segmented{display:grid;grid-template-columns:1fr 1fr;height:50px;border:1px solid #ccd3dc;border-radius:10px;overflow:hidden}
.segmented label{margin:0;position:relative}
.segmented input{position:absolute;opacity:0}
.segmented span{height:50px;display:flex;align-items:center;justify-content:center;font-size:12px;color:var(--muted);cursor:pointer}
.segmented input:checked+span{background:var(--navy);color:#fff}
button{width:100%;height:52px;border:0;border-radius:10px;background:var(--navy);color:#fff;font-weight:700;letter-spacing:.08em;cursor:pointer}
button:hover{transform:translateY(-1px);box-shadow:0 7px 18px rgba(16,36,62,.16)}
.error{color:#a52b2b;background:#fff2f2;border:1px solid #f0caca;border-radius:8px;padding:11px;margin:15px 0 0;font-size:13px}
.result{margin-top:20px;text-align:center}
.result h2{font-family:Georgia,"Times New Roman",serif;font-size:38px;color:var(--navy);margin:0 0 8px}
.result-summary{color:var(--gold);font-weight:700;margin:0 0 24px}
.details{display:grid;grid-template-columns:repeat(3,1fr);border-top:1px solid var(--line);border-bottom:1px solid var(--line);margin:0 0 20px}
.details div{padding:16px 8px}.details div+div{border-left:1px solid var(--line)}
.details span{display:block;color:var(--muted);font-size:10px;text-transform:uppercase;letter-spacing:.08em;margin-bottom:6px}
.details strong{font-size:13px;color:var(--navy)}
.notice{font-size:11px;line-height:1.6;color:var(--muted);margin:0}
footer{display:flex;justify-content:space-between;color:#8b95a2;font-size:10px;padding:25px 3px 0;letter-spacing:.04em}
@media(max-width:650px){.app{padding-top:22px}.hero{padding:52px 0 28px}h1{font-size:39px}.grid{grid-template-columns:1fr;gap:0}.details{grid-template-columns:1fr}.details div+div{border-left:0;border-top:1px solid var(--line)}footer{flex-direction:column;gap:8px}}
""",

"app.js": """const startDateInput = document.getElementById("startDate");
const daysInput = document.getElementById("days");
const calculateBtn = document.getElementById("calculateBtn");
const errorBox = document.getElementById("error");
const result = document.getElementById("result");

const resultDate = document.getElementById("resultDate");
const resultSummary = document.getElementById("resultSummary");
const detailStart = document.getElementById("detailStart");
const detailEnd = document.getElementById("detailEnd");
const detailType = document.getElementById("detailType");

const pad = n => String(n).padStart(2, "0");

function parseLocalDate(value) {
  const [y, m, d] = value.split("-").map(Number);
  return new Date(y, m - 1, d);
}

function formatDate(date) {
  return new Intl.DateTimeFormat("es-CO", {
    day: "2-digit", month: "long", year: "numeric"
  }).format(date);
}

function formatShortDate(date) {
  return new Intl.DateTimeFormat("es-CO", {
    day: "2-digit", month: "2-digit", year: "numeric"
  }).format(date);
}

function isWeekend(date) {
  const day = date.getDay();
  return day === 0 || day === 6;
}

/*
  V0.1:
  - La fecha ingresada es la fecha que origina el término.
  - El conteo comienza al día siguiente.
  - Días hábiles = lunes a viernes.
  - Días calendario = todos los días.
  - No se incluyen aún festivos, suspensiones ni reglas especiales.
*/
function calculateTerm(start, numberOfDays, type) {
  const current = new Date(start.getTime());
  let counted = 0;

  while (counted < numberOfDays) {
    current.setDate(current.getDate() + 1);

    if (type === "calendar" || !isWeekend(current)) {
      counted++;
    }
  }

  return current;
}

function showError(message) {
  errorBox.textContent = message;
  errorBox.hidden = false;
  result.hidden = true;
}

function clearError() {
  errorBox.hidden = true;
  errorBox.textContent = "";
}

calculateBtn.addEventListener("click", () => {
  clearError();

  if (!startDateInput.value) {
    showError("Selecciona una fecha de inicio.");
    return;
  }

  const days = Number(daysInput.value);
  if (!Number.isInteger(days) || days < 1) {
    showError("Ingresa un número entero de días mayor o igual a 1.");
    return;
  }

  const type = document.querySelector('input[name="termType"]:checked').value;
  const start = parseLocalDate(startDateInput.value);
  const end = calculateTerm(start, days, type);
  const label = type === "business" ? "días hábiles" : "días calendario";

  resultDate.textContent = formatDate(end).toUpperCase();
  resultSummary.textContent = `${days} ${label}`;
  detailStart.textContent = formatShortDate(start);
  detailEnd.textContent = formatShortDate(end);
  detailType.textContent = type === "business" ? "Días hábiles" : "Días calendario";
  result.hidden = false;

  result.scrollIntoView({ behavior: "smooth", block: "nearest" });
});

// Fecha de hoy como valor inicial para facilitar las pruebas.
const today = new Date();
startDateInput.value = `${today.getFullYear()}-${pad(today.getMonth()+1)}-${pad(today.getDate())}`;
""",

"README.md": """# Término Legal — Versión 0.1

Primer MVP del contador de términos jurídicos.

## Qué hace

- Recibe una fecha de inicio.
- Recibe un número entero de días.
- Permite elegir:
  - días hábiles (lunes a viernes);
  - días calendario.
- Cuenta desde el día siguiente a la fecha ingresada.
- Muestra la fecha de vencimiento y los datos del cálculo.
- Funciona sin servidor y sin base de datos.

## Qué NO hace todavía

Esta versión NO incorpora:

- festivos colombianos;
- vacancia judicial;
- suspensiones territoriales;
- reanudación de términos;
- términos por jurisdicción;
- reglas especiales de cómputo;
- fundamento normativo;
- calendario jurídico vivo.

Es deliberadamente una V0.1 para validar la experiencia y el núcleo matemático.

## Cómo probarla

No requiere instalación.

1. Abre `index.html` en un navegador.
2. Selecciona la fecha.
3. Ingresa el número de días.
4. Selecciona días hábiles o calendario.
5. Presiona "CALCULAR TÉRMINO".

## Publicación gratuita

Puedes subir estos archivos a un repositorio de GitHub y conectarlo con Vercel para publicarlo.

## Próxima versión propuesta

V0.2 — calendario colombiano y desglose día por día.

Después:

V0.3 — reglas jurídicas y fundamento.

V0.4 — suspensiones y reanudaciones.

V0.5 — términos jurídicos preconfigurados.
"""
}

for name, content in files.items():
    (project / name).write_text(content, encoding="utf-8")

zip_path = Path("/mnt/data/termino-legal-v0.1.zip")
with zipfile.ZipFile(zip_path, "w", zipfile.ZIP_DEFLATED) as z:
    for p in project.iterdir():
        z.write(p, p.name)

print(f"Proyecto creado: {zip_path}")
print("Archivos:", ", ".join(files.keys()))
