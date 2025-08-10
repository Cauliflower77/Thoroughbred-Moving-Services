# Thoroughbred-Moving-Services
Moving Labor Marketplace
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>HT‑AIOS — Thoroughbred Moving Tech Composite v18.9</title>
  <meta name="theme-color" content="#0a102a" />
  <meta name="version" content="v18.9-composite" />
  <style>
    :root{
      --bg:#0a102a; --bg2:#0b1440; --card:#0f1a44; --panel:#0e183f; --ink:#0a0f2a;
      --text:#e7ecff; --muted:#9fb0ff99; --accent:#6ee7ff; --accent2:#74f7c5;
      --ok:#36d399; --warn:#fbbf24; --danger:#f87171; --border:#273261; --chip:#11225b;
      --shadow: 0 12px 40px rgba(0,0,0,.35); --radius:16px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{margin:0;background:
      radial-gradient(1200px 600px at 10% -10%,#10215f,transparent),
      linear-gradient(180deg,var(--bg) 0%, #0a153a 100%);
      color:var(--text);font:15px/1.5 system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, Noto Sans, Arial, "Apple Color Emoji","Segoe UI Emoji"}
    header{position:sticky;top:0;z-index:30;background:rgba(10,16,42,.7);backdrop-filter: blur(10px); border-bottom:1px solid var(--border)}
    nav{max-width:1200px;margin:0 auto;display:flex;align-items:center;gap:16px;padding:12px 16px}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{width:36px;height:36px;border-radius:10px;background:conic-gradient(from 200deg at 50% 50%,var(--accent),#77a1ff 30%, #9e7bff 60%, var(--accent2));box-shadow: inset 0 0 18px #ffffff40, 0 6px 18px #0008}
    h1{font-size:18px;margin:0;letter-spacing:.2px}
    .badge{font-size:12px;color:#bcd3ff;background:#0f2558;padding:4px 8px;border:1px solid #28407b;border-radius:999px}
    .tabs{margin-left:auto;display:flex;gap:8px;flex-wrap:wrap}
    .tab{padding:8px 12px;border:1px solid var(--border);color:var(--text);border-radius:10px;background:#0b1440;cursor:pointer;user-select:none}
    .tab.active{background:linear-gradient(180deg,#10215f,#0b1440);box-shadow: inset 0 0 0 1px #2a3d85}

    main{max-width:1200px;margin:20px auto;padding:0 16px 80px}
    .grid{display:grid;grid-template-columns: 1.2fr .8fr;gap:16px}
    .card{background:linear-gradient(180deg,var(--card),#0e1b49);border:1px solid var(--border);border-radius:var(--radius);box-shadow:var(--shadow)}
    .card h2{margin:0 0 8px;font-size:18px}
    .card .hd{display:flex;align-items:center;justify-content:space-between;padding:14px 16px;border-bottom:1px solid var(--border)}
    .card .bd{padding:16px}
    .muted{color:var(--muted)}

    .row{display:grid;grid-template-columns: repeat(12,1fr);gap:12px}
    .f{display:flex;flex-direction:column;gap:6px}
    .f label{font-size:12px;color:#c7d7ff}
    input,select,textarea{width:100%;background:#0b1440;color:var(--text);border:1px solid #2a3974;border-radius:12px;padding:10px 12px}
    input[type="number"]{appearance:textfield}
    textarea{min-height:84px;resize:vertical}
    .chip{display:inline-flex;align-items:center;gap:6px;padding:6px 10px;border-radius:999px;border:1px solid #2a3974;background:var(--chip);font-size:12px}
    .btn{border:1px solid #2a3d85;background:linear-gradient(180deg,#16307b,#0f2558);color:#e7ecff;border-radius:12px;padding:10px 14px;cursor:pointer}
    .btn.secondary{background:linear-gradient(180deg,#0d1d52,#0b163d)}
    .btn.ghost{background:transparent}
    .btn:disabled{opacity:.6;cursor:not-allowed}
    .stack{display:flex;gap:8px;flex-wrap:wrap}
    .total{font-size:28px;font-weight:700}
    .kv{display:flex;justify-content:space-between;border-bottom:1px dashed #2a3974;padding:8px 0}

    .notice{background:#081138;border:1px solid #233a78;border-radius:12px;padding:10px 12px}
    .ok{color:var(--ok)} .warn{color:var(--warn)} .danger{color:var(--danger)}

    footer{position:fixed;bottom:0;left:0;right:0;background:rgba(10,16,42,.7);backdrop-filter: blur(8px);border-top:1px solid var(--border)}
    .foot{max-width:1200px;margin:0 auto;padding:10px 16px;display:flex;gap:10px;align-items:center;justify-content:space-between}

    .pill{background:#0d1d52;border:1px solid #2a3d85;border-radius:999px;padding:6px 10px;font-size:12px}
    .hl{background:linear-gradient(90deg, #8ee7ff40, transparent 60%);border-radius:8px}

    .two{display:grid;grid-template-columns:1fr 1fr;gap:12px}
    .three{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
    .four{display:grid;grid-template-columns:repeat(4,1fr);gap:12px}

    .hidden{display:none}
    .small{font-size:12px}
    .center{display:flex;align-items:center;justify-content:center}
  </style>
</head>
<body>
  <header>
    <nav>
      <div class="brand">
        <div class="logo" aria-hidden="true"></div>
        <h1>Thoroughbred Moving Services</h1>
        <span class="badge" id="buildBadge">build v18.9 composite</span>
      </div>
      <div class="tabs" id="tabs">
        <div class="tab active" data-tab="home">Home</div>
        <div class="tab" data-tab="quote">Instant Quote</div>
        <div class="tab" data-tab="book">Book</div>
        <div class="tab" data-tab="provider">Provider</div>
        <div class="tab" data-tab="admin">Admin</div>
        <div class="tab" data-tab="debug">Debug</div>
      </div>
    </nav>
  </header>

  <main>
    <!-- HOME -->
    <section id="home" class="view">
      <div class="grid">
        <div class="card">
          <div class="hd">
            <div>
              <h2>Local pros who show up ready</h2>
              <div class="muted">Serving Dunnellon, Ocala, Gainesville, The Villages, and Central Florida</div>
            </div>
            <div class="stack">
              <span class="chip">Insured</span>
              <span class="chip">Careful and fast</span>
              <span class="chip">Same day when available</span>
            </div>
          </div>
          <div class="bd">
            <div class="two">
              <div>
                <p class="hl">We offer crews of 2, 3, or 4 for load and unload. Pack and unpack available. Cleaning available on request.</p>
                <div class="notice" style="margin-top:10px">
                  <b>Local in town special</b>
                  <div>$499 up to 4 hours labor with 2 men and truck. $150 depot down to reserve.</div>
                  <div class="small muted">Out of town starts at $999 contact for details.</div>
                </div>
                <div class="stack" style="margin-top:12px">
                  <button class="btn" data-goto="quote">Get an instant quote</button>
                  <button class="btn secondary" data-goto="book">Book now</button>
                </div>
              </div>
              <div>
                <div class="card" style="background:#0d1d52;border-color:#2a3d85">
                  <div class="hd"><h2>Today at a glance</h2></div>
                  <div class="bd" id="todayGlance">
                    <div class="kv"><span>Open jobs</span><b id="openJobs">0</b></div>
                    <div class="kv"><span>Crews on duty</span><b id="crewsOn">0</b></div>
                    <div class="kv"><span>Next start</span><b id="nextStart">None</b></div>
                    <div class="kv"><span>Coverage</span><b>GNV OCA DNL VIL</b></div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <aside class="card">
          <div class="hd"><h2>Notes</h2><span class="muted small">Clear terms protect both sides</span></div>
          <div class="bd small">
            <ul>
              <li>Four hour minimum for local special then hourly.</li>
              <li>Depot down is applied to the bill. Non refundable if cancelled same day.</li>
              <li>Truck provided for the local special only. Standard hourly labor is labor only.</li>
              <li>Out of town starts at $999 which covers dispatch and first 50 miles. Contact for a custom quote.</li>
              <li>We do not list storage box services here. If you need storage delivery, ask and we will connect you to a preferred partner flow.</li>
            </ul>
          </div>
        </aside>
      </div>
    </section>

    <!-- QUOTE -->
    <section id="quote" class="view hidden">
      <div class="grid">
        <div class="card">
          <div class="hd"><h2>Instant quote</h2><span class="muted small" id="pricingVersion">pricing v1</span></div>
          <div class="bd">
            <form id="qForm" onsubmit="event.preventDefault(); calcQuote();">
              <div class="row">
                <div class="f" style="grid-column: span 4">
                  <label>Service</label>
                  <select id="svc">
                    <option value="labor">Labor only load or unload</option>
                    <option value="pack">Pack or unpack</option>
                    <option value="clean">Cleaning</option>
                    <option value="localSpecial">Local in town special 2 men and truck</option>
                    <option value="out">Out of town trip</option>
                  </select>
                </div>
                <div class="f" style="grid-column: span 4">
                  <label>Crew size</label>
                  <select id="crew">
                    <option>2</option>
                    <option>3</option>
                    <option>4</option>
                  </select>
                </div>
                <div class="f" style="grid-column: span 4">
                  <label>Estimated hours</label>
                  <input type="number" id="hours" min="1" step="1" value="4" />
                </div>
                <div class="f" style="grid-column: span 4">
                  <label>Estimated miles from Dunnellon depot</label>
                  <input type="number" id="miles" min="0" step="1" value="10" />
                </div>
                <div class="f" style="grid-column: span 4">
                  <label>Stairs flights total</label>
                  <input type="number" id="stairs" min="0" step="1" value="0" />
                </div>
                <div class="f" style="grid-column: span 4">
                  <label>Heavy items count</label>
                  <input type="number" id="heavy" min="0" step="1" value="0" />
                </div>
                <div class="f" style="grid-column: span 6">
                  <label>Date</label>
                  <input type="date" id="date" />
                </div>
                <div class="f" style="grid-column: span 6">
                  <label>Start window</label>
                  <select id="window">
                    <option>Morning</option>
                    <option>Midday</option>
                    <option>Afternoon</option>
                  </select>
                </div>
              </div>

              <div class="stack" style="margin:10px 0">
                <label class="chip"><input type="checkbox" id="sameDay"/> <span>Same day</span></label>
                <label class="chip"><input type="checkbox" id="weekend"/> <span>Weekend</span></label>
                <label class="chip"><input type="checkbox" id="needsStorage"/> <span>Also need storage delivery</span></label>
              </div>

              <div class="two">
                <div class="card">
                  <div class="hd"><h2>Estimate</h2></div>
                  <div class="bd" id="est"></div>
                </div>
                <div class="card">
                  <div class="hd"><h2>Next steps</h2></div>
                  <div class="bd">
                    <div class="notice" id="specialMsg" hidden></div>
                    <div class="stack">
                      <button class="btn" type="submit">Calculate</button>
                      <button class="btn secondary" type="button" onclick="copyQuote()">Copy quote</button>
                      <button class="btn ghost" type="button" onclick="window.print()">Print</button>
                    </div>
                  </div>
                </div>
              </div>

            </form>
          </div>
        </div>
        <aside class="card">
          <div class="hd"><h2>Policy guardrails</h2></div>
          <div class="bd small">
            <ul>
              <li>Payment due at completion except for depot down to reserve the local special.</li>
              <li>Time billed from arrival to completion. Travel billed when outside core zone.</li>
              <li>Heavy item fee for safes, pianos, gun safes, appliances over 250 lb.</li>
              <li>We can pause to avoid rain when safe. Weather delays do not reduce billable time.</li>
              <li>Customer should secure parking permits when required.</li>
            </ul>
          </div>
        </aside>
      </div>
    </section>

    <!-- BOOK -->
    <section id="book" class="view hidden">
      <div class="grid">
        <div class="card">
          <div class="hd"><h2>Book your move</h2><span class="muted small">Fast secure intake</span></div>
          <div class="bd">
            <form id="bForm" onsubmit="event.preventDefault(); makeBooking();">
              <div class="row">
                <div class="f" style="grid-column: span 6"><label>Full name</label><input id="bName" required /></div>
                <div class="f" style="grid-column: span 6"><label>Phone</label><input id="bPhone" required /></div>
                <div class="f" style="grid-column: span 8"><label>Email</label><input id="bEmail" type="email" required /></div>
                <div class="f" style="grid-column: span 4"><label>Crew size</label>
                  <select id="bCrew"><option>2</option><option>3</option><option>4</option></select></div>
                <div class="f" style="grid-column: span 4"><label>Service</label>
                  <select id="bSvc"><option value="labor">Labor only</option><option value="pack">Pack or unpack</option><option value="clean">Cleaning</option><option value="localSpecial">Local in town special</option><option value="out">Out of town</option></select></div>
                <div class="f" style="grid-column: span 4"><label>Date</label><input id="bDate" type="date" required/></div>
                <div class="f" style="grid-column: span 4"><label>Start window</label>
                  <select id="bWin"><option>Morning</option><option>Midday</option><option>Afternoon</option></select></div>
                <div class="f" style="grid-column: span 4"><label>From address</label><input id="bFrom"/></div>
                <div class="f" style="grid-column: span 4"><label>To address</label><input id="bTo"/></div>
                <div class="f" style="grid-column: span 12"><label>Notes</label><textarea id="bNotes" placeholder="Stairs, elevators, heavy items, gate codes"></textarea></div>
              </div>
              <div class="stack" style="margin-top:10px">
                <button class="btn" type="submit">Reserve</button>
                <button class="btn secondary" type="button" onclick="prefillDeposit()">Send $150 depot down link</button>
              </div>
            </form>
          </div>
        </div>
        <aside class="card">
          <div class="hd"><h2>What happens next</h2></div>
          <div class="bd small">
            <ol>
              <li>You receive a confirmation by email and text.</li>
              <li>We assign a 2, 3, or 4 person crew based on your selection.</li>
              <li>Day of service we text when en route with an ETA.</li>
            </ol>
            <div class="notice small">Need storage delivery as well? After you reserve, reply to your confirmation and we will route you to a preferred partner flow that handles that piece smoothly.</div>
          </div>
        </aside>
      </div>
    </section>

    <!-- PROVIDER -->
    <section id="provider" class="view hidden">
      <div class="grid">
        <div class="card">
          <div class="hd"><h2>Provider console</h2><span class="muted small">For crew and dispatch</span></div>
          <div class="bd">
            <div class="two">
              <div>
                <div class="stack">
                  <span class="pill">Clock in <input type="time" id="pIn"> </span>
                  <span class="pill">Clock out <input type="time" id="pOut"> </span>
                  <button class="btn" onclick="logHours()">Log hours</button>
                </div>
                <div class="notice small" style="margin-top:10px" id="hoursLog">No entries</div>
                <h3>Open bookings</h3>
                <div id="pJobs" class="small"></div>
              </div>
              <div>
                <h3>Job note</h3>
                <textarea id="pNote" placeholder="Arrival, completion, issues, customer code"></textarea>
                <div class="stack" style="margin-top:8px">
                  <button class="btn" onclick="saveNote()">Save</button>
                  <button class="btn secondary" onclick="copyNote()">Copy</button>
                </div>
                <div class="small muted" style="margin-top:8px">Do not post customer codes publicly. Use this console only.</div>
              </div>
            </div>
          </div>
        </div>
        <aside class="card">
          <div class="hd"><h2>Reminders</h2></div>
          <div class="bd small">
            <ul>
              <li>Document start and finish time. Take doorway and floor protection photos when needed.</li>
              <li>Use blankets and wrap on wood and glass.</li>
              <li>Confirm owner approval on any items that will not fit or need disassembly.</li>
            </ul>
          </div>
        </aside>
      </div>
    </section>

    <!-- ADMIN -->
    <section id="admin" class="view hidden">
      <div class="grid">
        <div class="card">
          <div class="hd"><h2>Admin pricing and policy</h2><span class="muted small">Local storage only in browser</span></div>
          <div class="bd">
            <form id="pForm" onsubmit="event.preventDefault(); savePricing();">
              <div class="three">
                <div class="f"><label>Base dispatch</label><input type="number" id="baseTrip" value="79"/></div>
                <div class="f"><label>Per mile outside core</label><input type="number" id="perMile" value="2"/></div>
                <div class="f"><label>Hourly per mover</label><input type="number" id="hourly" value="55"/></div>
                <div class="f"><label>Minimum hours</label><input type="number" id="minHours" value="2"/></div>
                <div class="f"><label>Stairs per flight</label><input type="number" id="stairsFee" value="20"/></div>
                <div class="f"><label>Heavy item fee</label><input type="number" id="heavyFee" value="45"/></div>
                <div class="f"><label>Same day fee</label><input type="number" id="sameDayFee" value="75"/></div>
                <div class="f"><label>Weekend fee</label><input type="number" id="weekendFee" value="40"/></div>
                <div class="f"><label>Discount percent</label><input type="number" id="discountPct" value="0" step=".01"/></div>
                <div class="f"><label>Tax percent</label><input type="number" id="taxPct" value="0" step=".01"/></div>
                <div class="f"><label>Local special flat</label><input type="number" id="localFlat" value="499"/></div>
                <div class="f"><label>Local special hours</label><input type="number" id="localHours" value="4"/></div>
                <div class="f"><label>Deposit down</label><input type="number" id="depositDown" value="150"/></div>
                <div class="f"><label>Out of town base</label><input type="number" id="outBase" value="999"/></div>
                <div class="f"><label>Out included miles</label><input type="number" id="outMiles" value="50"/></div>
              </div>
              <div class="stack" style="margin-top:10px">
                <button class="btn" type="submit">Save</button>
                <button class="btn secondary" type="button" onclick="resetPricing()">Reset defaults</button>
                <button class="btn ghost" type="button" onclick="exportSettings()">Export settings</button>
                <input type="file" id="importFile" accept="application/json" style="display:none"/>
                <button class="btn ghost" type="button" onclick="document.getElementById('importFile').click()">Import settings</button>
              </div>
            </form>
          </div>
        </div>
        <aside class="card">
          <div class="hd"><h2>Legal notes</h2></div>
          <div class="bd small">
            <ul>
              <li>This is an estimate engine. Final bill may adjust to actual time and travel.</li>
              <li>No scraping or automated access of partner portals from here. Links only.</li>
              <li>Customer data remains on device unless you export it.</li>
            </ul>
          </div>
        </aside>
      </div>
    </section>

    <!-- DEBUG -->
    <section id="debug" class="view hidden">
      <div class="grid">
        <div class="card">
          <div class="hd"><h2>Debug and tools</h2><span class="muted small">For owner only</span></div>
          <div class="bd">
            <div class="two">
              <div>
                <h3>Data</h3>
                <div class="stack">
                  <button class="btn" onclick="downloadFile('bookings.json', JSON.stringify(state.bookings,null,2))">Download bookings</button>
                  <button class="btn secondary" onclick="downloadFile('pricing.json', localStorage.getItem('pricing')||'{}')">Download pricing</button>
                  <button class="btn ghost" onclick="localStorage.clear(); alert('Local storage cleared')">Clear storage</button>
                </div>
                <h3 style="margin-top:18px">Reveal partner hub</h3>
                <div class="stack"><button class="btn" onclick="revealPartners()">Open</button></div>
              </div>
              <div>
                <h3>Quiet boost</h3>
                <div class="small muted">This page tags your quote copies with UTM and job notes that make intake faster when you route to a partner flow. No external calls.</div>
                <div class="notice small" id="tagStatus">Tags ready</div>
              </div>
            </div>
          </div>
        </div>
        <aside class="card" id="partners" style="display:none">
          <div class="hd"><h2>Preferred partner hub</h2><span class="muted small">Links open in a new tab</span></div>
          <div class="bd small">
            <p>When a customer needs storage delivery, send them here. These links carry tracking parameters and copyable intake blurbs. Replace placeholders with your actual profile links.</p>
            <div class="two">
              <div class="card">
                <div class="hd"><h2>Gainesville</h2></div>
                <div class="bd">
                  <a class="btn" target="_blank" id="mhGnv" href="#">Open Gainesville profile</a>
                  <textarea id="mhGnvNote" class="small" style="margin-top:8px" readonly></textarea>
                </div>
              </div>
              <div class="card">
                <div class="hd"><h2>Ocala</h2></div>
                <div class="bd">
                  <a class="btn" target="_blank" id="mhOca" href="#">Open Ocala profile</a>
                  <textarea id="mhOcaNote" class="small" style="margin-top:8px" readonly></textarea>
                </div>
              </div>
            </div>
            <div class="notice small" style="margin-top:8px">Set your real links in Admin Export file under key <code>mhLinks</code> or by calling <code>setMhLinks()</code> in console.</div>
          </div>
        </aside>
      </div>
    </section>

  </main>

  <footer>
    <div class="foot">
      <div class="stack small">
        <span class="muted">HT‑AIOS Composite</span>
        <span class="pill">v18.9</span>
        <span class="pill">Owner pro mode <input type="checkbox" id="proToggle"></span>
      </div>
      <div class="stack small">
        <a class="pill" href="#" onclick="window.scrollTo({top:0,behavior:'smooth'})">Top</a>
        <a class="pill" href="#" onclick="location.hash='quote'">Quote</a>
        <a class="pill" href="#" onclick="location.hash='book'">Book</a>
      </div>
    </div>
  </footer>

  <script>
    const $ = sel => document.querySelector(sel);
    const $$ = sel => Array.from(document.querySelectorAll(sel));

    const state = {
      bookings: JSON.parse(localStorage.getItem('bookings')||'[]'),
      pricing: loadPricing(),
    };

    function loadPricing(){
      const d = {
        baseTrip:79, perMile:2, hourlyPerMover:55, minHours:2,
        stairsPerFlight:20, heavyItem:45, sameDayFee:75, weekendFee:40,
        discountPct:0, taxPct:0,
        localFlat:499, localHours:4, depositDown:150,
        outBase:999, outMiles:50,
        mhLinks:{ gnv:"https://example.com/your-movinghelper-gainesville", oca:"https://example.com/your-movinghelper-ocala" }
      };
      try { return Object.assign(d, JSON.parse(localStorage.getItem('pricing')||'{}')); } catch(e){ return d; }
    }

    function savePricing(){
      const p = state.pricing;
      p.baseTrip = num('#baseTrip');
      p.perMile = num('#perMile');
      p.hourlyPerMover = num('#hourly');
      p.minHours = num('#minHours');
      p.stairsPerFlight = num('#stairsFee');
      p.heavyItem = num('#heavyFee');
      p.sameDayFee = num('#sameDayFee');
      p.weekendFee = num('#weekendFee');
      p.discountPct = num('#discountPct');
      p.taxPct = num('#taxPct');
      p.localFlat = num('#localFlat');
      p.localHours = num('#localHours');
      p.depositDown = num('#depositDown');
      p.outBase = num('#outBase');
      p.outMiles = num('#outMiles');
      localStorage.setItem('pricing', JSON.stringify(p));
      $('#pricingVersion').textContent = 'pricing saved ' + new Date().toLocaleString();
      alert('Saved');
      updateMhUi();
    }

    function resetPricing(){ localStorage.removeItem('pricing'); state.pricing = loadPricing(); fillAdmin(); alert('Defaults restored'); updateMhUi(); }

    function fillAdmin(){
      const p = state.pricing;
      set('#baseTrip', p.baseTrip); set('#perMile', p.perMile); set('#hourly', p.hourlyPerMover);
      set('#minHours', p.minHours); set('#stairsFee', p.stairsPerFlight); set('#heavyFee', p.heavyItem);
      set('#sameDayFee', p.sameDayFee); set('#weekendFee', p.weekendFee); set('#discountPct', p.discountPct); set('#taxPct', p.taxPct);
      set('#localFlat', p.localFlat); set('#localHours', p.localHours); set('#depositDown', p.depositDown);
      set('#outBase', p.outBase); set('#outMiles', p.outMiles);
    }

    function num(sel){ return Math.max(0, Number($(sel).value||0)); }
    function set(sel, v){ $(sel).value = v; }

    function clamp(x,min,max){ return Math.min(Math.max(x,min),max); }

    function money(n){ return '$' + (Math.round(n*100)/100).toFixed(2); }

    function ServiceLabel(code){
      return ({ labor:'Labor only', pack:'Pack or unpack', clean:'Cleaning', localSpecial:'Local in town special', out:'Out of town' })[code]||code;
    }

    function computeTotals(form, p){
      const svc = form.svc;
      const crew = form.crew;
      const hours = Math.max(p.minHours, form.hours);
      const travel = Math.max(0, form.miles) * p.perMile + p.baseTrip;
      const stairs = Math.max(0, form.stairs) * p.stairsPerFlight;
      const heavy = Math.max(0, form.heavy) * p.heavyItem;
      const flags = (form.sameDay? p.sameDayFee:0) + (form.weekend? p.weekendFee:0);

      let labor = crew * p.hourlyPerMover * hours;
      let special = 0;

      if(svc==='localSpecial'){
        special = p.localFlat; // covers truck and 2 movers up to localHours
        // If crew bigger than 2, add the extra mover hours at hourly rate beyond included two
        const includedMovers = 2; const extraMovers = Math.max(0, crew - includedMovers);
        const extraHours = Math.max(0, hours - p.localHours); // regular hourly for any time beyond included hours for all movers
        labor = 0; // included inside special flat for first two movers and included hours
        if(extraMovers>0){ labor += extraMovers * p.hourlyPerMover * hours; }
        if(extraHours>0){ labor += includedMovers * p.hourlyPerMover * extraHours + extraMovers * p.hourlyPerMover * extraHours; }
      }

      if(svc==='out'){
        // Out of town base covers dispatch and first outMiles
        const extraMiles = Math.max(0, form.miles - p.outMiles);
        const outTravel = p.outBase + extraMiles * p.perMile;
        return finalize(outTravel + labor + stairs + heavy + flags, p.discountPct, p.taxPct, {travel: outTravel, labor, stairs, heavy, flags, special:0});
      }

      return finalize(travel + labor + stairs + heavy + flags + special, p.discountPct, p.taxPct, {travel, labor, stairs, heavy, flags, special});
    }

    function finalize(sub, discPct, taxPct, parts){
      const discount = sub * clamp(discPct,0,1);
      const taxed = (sub - discount) * (1 + clamp(taxPct,0,1));
      const total = Math.round(taxed*100)/100;
      return { total, parts, discount, tax: taxed - (sub - discount), sub };
    }

    function calcQuote(){
      const p = state.pricing;
      const form = {
        svc: $('#svc').value,
        crew: Number($('#crew').value),
        hours: Number($('#hours').value||0),
        miles: Number($('#miles').value||0),
        stairs: Number($('#stairs').value||0),
        heavy: Number($('#heavy').value||0),
        sameDay: $('#sameDay').checked,
        weekend: $('#weekend').checked,
      };

      const res = computeTotals(form, p);
      const parts = res.parts;

      const rows = [
        ['Dispatch and travel', parts.travel],
        ['Labor', parts.labor],
        ['Stairs', parts.stairs],
        ['Heavy items', parts.heavy],
        ['Same day or weekend', parts.flags],
        ['Local special flat', parts.special]
      ]
      .filter(x=>x[1]>0)
      .map(([k,v])=>`<div class="kv"><span>${k}</span><b>${money(v)}</b></div>`)
      .join('');

      const svcLabel = ServiceLabel(form.svc);

      $('#est').innerHTML = `
        <div class="kv"><span class="muted">Service</span><b>${svcLabel} • Crew ${form.crew}</b></div>
        ${rows}
        <div class="kv"><span>Discount</span><b>${res.discount?('-'+money(res.discount)):'$0.00'}</b></div>
        <div class="kv"><span>Tax</span><b>${money(res.tax)}</b></div>
        <div class="kv" style="border-bottom:none"><span class="total">Total estimate</span><span class="total">${money(res.total)}</span></div>
      `;

      const specialMsg = $('#specialMsg');
      specialMsg.hidden = true;

      if($('#svc').value==='localSpecial'){
        specialMsg.hidden = false;
        specialMsg.innerHTML = `Reserve with a ${money(p.depositDown)} depot down. Includes ${p.localHours} hours with 2 movers and truck. Time beyond that is billed hourly.`;
      }

      const needsStorage = $('#needsStorage').checked;
      if(needsStorage){
        specialMsg.hidden = false;
        specialMsg.innerHTML = `You noted storage delivery. After you reserve we will route you to our preferred partner flow for storage delivery. This keeps things smooth.`;
      }

      // Tag last quote for partner routing speed
      localStorage.setItem('lastQuote', JSON.stringify({form, res, at:Date.now()}));
    }

    function copyQuote(){
      const t = document.createElement('textarea');
      const p = state.pricing;
      const last = JSON.parse(localStorage.getItem('lastQuote')||'null');
      if(!last){ alert('Calculate first'); return; }
      const f = last.form; const r = last.res;
      const tag = `utm_source=site&utm_medium=quote&utm_campaign=ht_${new Date().toISOString().slice(0,10)}`;
      t.value = [
        `Service: ${ServiceLabel(f.svc)} | Crew ${f.crew}`,
        `Hours: ${f.hours} | Miles: ${f.miles}`,
        `Stairs: ${f.stairs} | Heavy: ${f.heavy}`,
        `Same day: ${f.sameDay?'Yes':'No'} | Weekend: ${f.weekend?'Yes':'No'}`,
        `Estimate: ${money(r.total)}`,
        `Deposit to reserve local special: ${money(p.depositDown)}`,
        `Tag: ${tag}`
      ].join('\n');
      document.body.appendChild(t); t.select(); document.execCommand('copy'); t.remove();
      $('#tagStatus').textContent = 'Quote copied with tracking tag';
      alert('Copied');
    }

    function makeBooking(){
      const b = {
        name: $('#bName').value.trim(), phone: $('#bPhone').value.trim(), email: $('#bEmail').value.trim(),
        crew: Number($('#bCrew').value), svc: $('#bSvc').value, date: $('#bDate').value, window: $('#bWin').value,
        from: $('#bFrom').value.trim(), to: $('#bTo').value.trim(), notes: $('#bNotes').value.trim(),
        at: Date.now(), id: 'B' + Math.random().toString(36).slice(2,8).toUpperCase()
      };
      state.bookings.push(b);
      localStorage.setItem('bookings', JSON.stringify(state.bookings));
      alert('Reserved ' + b.id);
      renderProvider();
    }

    function prefillDeposit(){
      const p = state.pricing;
      const msg = `To reserve the local special, pay the depot down of ${money(p.depositDown)}. Reply DONE after payment.`;
      navigator.clipboard.writeText(msg).then(()=>alert('Deposit message copied')); 
    }

    function renderProvider(){
      const jobs = state.bookings.slice(-10).reverse().map(b=>{
        return `<div class="notice" style="margin-top:8px">
          <div><b>${b.name}</b> • ${ServiceLabel(b.svc)} • Crew ${b.crew}</div>
          <div class="small muted">${b.date||'TBD'} ${b.window||''} • ${b.from||''} → ${b.to||''}</div>
          <div class="small">Notes: ${b.notes||'None'}</div>
          <div class="small">Code: ${b.id}</div>
        </div>`
      }).join('') || '<div class="muted small">No bookings yet</div>';
      $('#pJobs').innerHTML = jobs;

      // Home glance
      $('#openJobs').textContent = state.bookings.length;
      $('#crewsOn').textContent = Math.min(state.bookings.length, 3);
      const next = state.bookings.at(-1);
      $('#nextStart').textContent = next? (next.date||'TBD') + ' ' + (next.window||''): 'None';
    }

    function logHours(){
      const i = $('#pIn').value || '08:00';
      const o = $('#pOut').value || '17:00';
      const txt = `Crew hours logged ${i} to ${o} on ${new Date().toLocaleDateString()}`;
      $('#hoursLog').textContent = txt;
      navigator.clipboard.writeText(txt);
    }

    function saveNote(){ const v = $('#pNote').value.trim(); if(!v) return; localStorage.setItem('lastNote', v); alert('Saved'); }
    function copyNote(){ const v = localStorage.getItem('lastNote')||''; if(!v) { alert('Save a note first'); return;} navigator.clipboard.writeText(v).then(()=>alert('Copied')); }

    function downloadFile(name, text){
      const a = document.createElement('a');
      a.href = URL.createObjectURL(new Blob([text], {type:'application/json'}));
      a.download = name; a.click(); URL.revokeObjectURL(a.href);
    }

    // Import settings
    document.getElementById('importFile').addEventListener('change', (e)=>{
      const file = e.target.files[0]; if(!file) return;
      const fr = new FileReader();
      fr.onload = () => { try{ localStorage.setItem('pricing', fr.result); state.pricing = loadPricing(); fillAdmin(); updateMhUi(); alert('Imported'); } catch(err){ alert('Invalid file'); } };
      fr.readAsText(file);
    });

    function exportSettings(){ downloadFile('pricing.json', JSON.stringify(state.pricing,null,2)); }

    function revealPartners(){ $('#partners').style.display = 'block'; updateMhUi(); }

    function setMhLinks(obj){ state.pricing.mhLinks = Object.assign(state.pricing.mhLinks||{}, obj||{}); localStorage.setItem('pricing', JSON.stringify(state.pricing)); updateMhUi(); }

    function updateMhUi(){
      const {mhLinks} = state.pricing;
      const tag = '?utm_source=site&utm_medium=partner_hub&utm_campaign=ht_ref';
      const g = (mhLinks.gnv||'#') + tag; const o = (mhLinks.oca||'#') + tag;
      const last = JSON.parse(localStorage.getItem('lastQuote')||'null');
      const blurb = (city) => {
        const base = `Referral from Thoroughbred site for storage delivery in ${city}. We are handling labor and customer wants smooth storage handling. Please prioritize.`;
        const q = last? ` Quote ${ServiceLabel(last.form.svc)} crew ${last.form.crew} hours ${last.form.hours} miles ${last.form.miles} est ${money(last.res.total)}.`:'';
        const id = state.bookings.at(-1)?.id || 'N A';
        return base + q + ` Job code ${id}.`;
      };
      const gEl = $('#mhGnv'); if(gEl){ gEl.href = g; }
      const oEl = $('#mhOca'); if(oEl){ oEl.href = o; }
      const gn = $('#mhGnvNote'); if(gn){ gn.value = blurb('Gainesville'); }
      const on = $('#mhOcaNote'); if(on){ on.value = blurb('Ocala'); }
    }

    // Tab router
    function showTab(name){
      $$('.view').forEach(v=>v.classList.add('hidden'));
      $('#' + name).classList.remove('hidden');
      $$('#tabs .tab').forEach(t=>t.classList.toggle('active', t.dataset.tab===name));
      location.hash = name;
    }
    $$('#tabs .tab').forEach(t=> t.addEventListener('click', ()=> showTab(t.dataset.tab)));

    // hash routing and pro toggle
    window.addEventListener('hashchange', ()=>{ const h = location.hash.replace('#','')||'home'; if($('#'+h)) showTab(h); });
    $('#proToggle').addEventListener('change', (e)=>{ if(e.target.checked) revealPartners(); else $('#partners').style.display='none'; });

    // boot
    (function boot(){
      fillAdmin(); renderProvider(); updateMhUi();
      const h = location.hash.replace('#','')||'home'; showTab(h);
      // set default date two days out
      const d = new Date(); d.setDate(d.getDate()+2);
      const iso = d.toISOString().slice(0,10);
      if($('#date')) $('#date').value = iso; if($('#bDate')) $('#bDate').value = iso;

      // quick access to partner hub with ?pro=1
      const params = new URLSearchParams(location.search); if(params.get('pro')) { $('#proToggle').checked = true; revealPartners(); }
    })();
  </script>
</body>
</html>
