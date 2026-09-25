```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<meta name="theme-color" content="#17111f">
<title>369 — Manifest Your Goals</title>

<style>
*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

:root{
  --bg:#0d0b12;
  --surface:#17131e;
  --surface2:#211a2b;
  --border:rgba(255,255,255,.08);
  --text:#f8f5fb;
  --muted:#aaa2b5;
  --gold:#d9b36c;
  --gold2:#f0d59b;
  --purple:#9d7bea;
  --green:#62d39a;
  --red:#ed7474;
  --shadow:0 18px 50px rgba(0,0,0,.25);
  --radius:20px;
}

html{
  scroll-behavior:smooth;
}

body{
  font-family:
    -apple-system,
    BlinkMacSystemFont,
    "Noto Sans Myanmar",
    "Myanmar Text",
    sans-serif;
  background:
    radial-gradient(circle at 80% -10%,rgba(157,123,234,.15),transparent 35%),
    radial-gradient(circle at -10% 30%,rgba(217,179,108,.08),transparent 30%),
    var(--bg);
  color:var(--text);
  min-height:100vh;
}

button,
input,
textarea,
select{
  font:inherit;
}

button{
  cursor:pointer;
  border:0;
}

.app{
  min-height:100vh;
}

/* =========================
   SIDEBAR
========================= */

.sidebar{
  position:fixed;
  left:0;
  top:0;
  width:255px;
  height:100vh;
  padding:24px 16px;
  background:rgba(17,13,23,.94);
  border-right:1px solid var(--border);
  backdrop-filter:blur(20px);
  z-index:100;
  display:flex;
  flex-direction:column;
}

.logo{
  display:flex;
  align-items:center;
  gap:12px;
  padding:4px 8px 28px;
}

.logo-mark{
  width:44px;
  height:44px;
  border-radius:14px;
  display:grid;
  place-items:center;
  font-size:20px;
  font-weight:900;
  color:#17111f;
  background:linear-gradient(135deg,var(--gold2),var(--gold));
  box-shadow:0 8px 25px rgba(217,179,108,.2);
}

.logo-text strong{
  display:block;
  font-size:17px;
  letter-spacing:.5px;
}

.logo-text span{
  color:var(--muted);
  font-size:11px;
}

.nav{
  display:flex;
  flex-direction:column;
  gap:5px;
}

.nav-btn{
  width:100%;
  display:flex;
  align-items:center;
  gap:12px;
  padding:13px 14px;
  border-radius:13px;
  background:transparent;
  color:var(--muted);
  text-align:left;
  transition:.2s;
}

.nav-btn:hover{
  background:rgba(255,255,255,.05);
  color:var(--text);
}

.nav-btn.active{
  color:var(--text);
  background:linear-gradient(90deg,rgba(217,179,108,.15),rgba(157,123,234,.08));
  border:1px solid rgba(217,179,108,.12);
}

.nav-icon{
  width:22px;
  text-align:center;
  font-size:18px;
}

.sidebar-bottom{
  margin-top:auto;
  padding:14px 8px 0;
  border-top:1px solid var(--border);
}

.mini-profile{
  display:flex;
  align-items:center;
  gap:10px;
}

.avatar{
  width:38px;
  height:38px;
  border-radius:50%;
  display:grid;
  place-items:center;
  background:linear-gradient(135deg,#5d477d,#30253e);
  font-weight:800;
}

.profile-name{
  font-size:13px;
  font-weight:700;
}

.profile-status{
  color:var(--muted);
  font-size:11px;
}

/* =========================
   MAIN
========================= */

.main{
  margin-left:255px;
  min-height:100vh;
}

.topbar{
  height:76px;
  padding:0 30px;
  display:flex;
  align-items:center;
  justify-content:space-between;
  border-bottom:1px solid var(--border);
  background:rgba(13,11,18,.65);
  backdrop-filter:blur(18px);
  position:sticky;
  top:0;
  z-index:50;
}

.page-title h1{
  font-size:21px;
}

.page-title p{
  color:var(--muted);
  font-size:12px;
  margin-top:3px;
}

.top-actions{
  display:flex;
  align-items:center;
  gap:10px;
}

.icon-btn{
  width:40px;
  height:40px;
  border-radius:12px;
  background:var(--surface);
  border:1px solid var(--border);
  color:var(--text);
}

.mobile-menu{
  display:none;
}

.content{
  padding:28px 30px 100px;
  max-width:1400px;
  margin:auto;
}

.view{
  display:none;
}

.view.active{
  display:block;
}

/* =========================
   CARDS
========================= */

.hero{
  border:1px solid rgba(217,179,108,.14);
  background:
    radial-gradient(circle at 85% 15%,rgba(157,123,234,.22),transparent 30%),
    linear-gradient(135deg,#21182b,#17131e);
  border-radius:28px;
  padding:30px;
  box-shadow:var(--shadow);
  margin-bottom:20px;
}

.hero-top{
  display:flex;
  justify-content:space-between;
  gap:20px;
  align-items:center;
}

.eyebrow{
  color:var(--gold2);
  font-size:11px;
  font-weight:800;
  letter-spacing:1.6px;
  text-transform:uppercase;
  margin-bottom:9px;
}

.hero h2{
  font-size:31px;
  line-height:1.2;
  max-width:600px;
}

.hero p{
  color:var(--muted);
  max-width:620px;
  line-height:1.7;
  margin-top:10px;
  font-size:14px;
}

.hero-number{
  min-width:145px;
  height:145px;
  border-radius:50%;
  display:grid;
  place-items:center;
  text-align:center;
  background:
    radial-gradient(circle,#211a2b 57%,transparent 58%),
    conic-gradient(var(--gold) var(--progress,0%),rgba(255,255,255,.08) 0);
  box-shadow:inset 0 0 30px rgba(0,0,0,.3);
}

.hero-number strong{
  display:block;
  font-size:31px;
}

.hero-number span{
  color:var(--muted);
  font-size:11px;
}

.stats-grid{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:14px;
  margin-bottom:20px;
}

.stat-card{
  background:rgba(23,19,30,.9);
  border:1px solid var(--border);
  border-radius:18px;
  padding:20px;
}

.stat-label{
  color:var(--muted);
  font-size:12px;
}

.stat-value{
  margin-top:9px;
  font-size:26px;
  font-weight:850;
}

.stat-small{
  color:var(--muted);
  font-size:11px;
  margin-top:4px;
}

.grid-2{
  display:grid;
  grid-template-columns:1.35fr 1fr;
  gap:20px;
}

.card{
  background:rgba(23,19,30,.9);
  border:1px solid var(--border);
  border-radius:var(--radius);
  padding:22px;
  box-shadow:0 10px 30px rgba(0,0,0,.08);
}

.card-header{
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:10px;
  margin-bottom:18px;
}

.card-title{
  font-size:16px;
  font-weight:800;
}

.card-subtitle{
  color:var(--muted);
  font-size:11px;
  margin-top:3px;
}

/* =========================
   BUTTONS
========================= */

.primary-btn{
  background:linear-gradient(135deg,var(--gold2),var(--gold));
  color:#1b1420;
  font-weight:850;
  padding:12px 18px;
  border-radius:12px;
  transition:.2s;
}

.primary-btn:hover{
  transform:translateY(-1px);
  filter:brightness(1.06);
}

.secondary-btn{
  background:var(--surface2);
  color:var(--text);
  border:1px solid var(--border);
  padding:11px 16px;
  border-radius:12px;
}

.danger-btn{
  background:rgba(237,116,116,.1);
  color:#ff9b9b;
  border:1px solid rgba(237,116,116,.15);
  padding:10px 14px;
  border-radius:11px;
}

.small-btn{
  padding:8px 12px;
  border-radius:9px;
  font-size:12px;
}

/* =========================
   PRACTICE
========================= */

.practice-list{
  display:flex;
  flex-direction:column;
  gap:10px;
}

.practice-item{
  display:flex;
  align-items:center;
  gap:14px;
  padding:15px;
  border:1px solid var(--border);
  background:rgba(255,255,255,.025);
  border-radius:15px;
}

.practice-number{
  width:44px;
  height:44px;
  flex:0 0 44px;
  border-radius:13px;
  display:grid;
  place-items:center;
  font-size:18px;
  font-weight:900;
  background:rgba(217,179,108,.1);
  color:var(--gold2);
}

.practice-info{
  flex:1;
}

.practice-info strong{
  display:block;
  font-size:14px;
}

.practice-info span{
  display:block;
  color:var(--muted);
  font-size:11px;
  margin-top:3px;
}

.complete{
  border-color:rgba(98,211,154,.2);
  background:rgba(98,211,154,.04);
}

.complete .practice-number{
  color:var(--green);
  background:rgba(98,211,154,.1);
}

/* =========================
   AFFIRMATION
========================= */

.quote-card{
  min-height:210px;
  display:flex;
  flex-direction:column;
  justify-content:center;
  position:relative;
  overflow:hidden;
}

.quote-mark{
  position:absolute;
  top:-25px;
  right:10px;
  font-size:150px;
  color:rgba(217,179,108,.06);
  line-height:1;
}

.quote{
  font-size:21px;
  line-height:1.6;
  font-weight:700;
  position:relative;
  z-index:1;
}

.quote-meta{
  color:var(--gold);
  font-size:11px;
  margin-top:16px;
}

/* =========================
   GOALS
========================= */

.goal-grid{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:15px;
}

.goal-card{
  background:rgba(23,19,30,.9);
  border:1px solid var(--border);
  border-radius:18px;
  padding:18px;
}

.goal-top{
  display:flex;
  align-items:center;
  justify-content:space-between;
}

.goal-icon{
  width:42px;
  height:42px;
  border-radius:13px;
  display:grid;
  place-items:center;
  background:rgba(157,123,234,.1);
}

.goal-percent{
  font-weight:850;
  color:var(--gold2);
}

.goal-card h3{
  margin-top:15px;
  font-size:15px;
}

.goal-card p{
  color:var(--muted);
  font-size:11px;
  margin-top:4px;
}

.progress{
  height:7px;
  background:rgba(255,255,255,.07);
  border-radius:20px;
  overflow:hidden;
  margin-top:16px;
}

.progress span{
  display:block;
  height:100%;
  border-radius:20px;
  background:linear-gradient(90deg,var(--purple),var(--gold));
}

.goal-footer{
  display:flex;
  justify-content:space-between;
  margin-top:9px;
  color:var(--muted);
  font-size:10px;
}

/* =========================
   JOURNAL
========================= */

textarea,
input,
select{
  width:100%;
  background:#110e17;
  color:var(--text);
  border:1px solid var(--border);
  outline:none;
  border-radius:12px;
  padding:13px 14px;
}

textarea{
  min-height:180px;
  resize:vertical;
  line-height:1.7;
}

input:focus,
textarea:focus,
select:focus{
  border-color:rgba(217,179,108,.45);
}

.form-group{
  margin-bottom:15px;
}

.form-group label{
  display:block;
  color:var(--muted);
  font-size:12px;
  margin-bottom:7px;
}

.journal-list{
  display:flex;
  flex-direction:column;
  gap:10px;
}

.journal-entry{
  padding:15px;
  background:rgba(255,255,255,.025);
  border:1px solid var(--border);
  border-radius:14px;
}

.journal-date{
  color:var(--gold);
  font-size:11px;
  margin-bottom:6px;
}

.journal-text{
  color:#ddd6e3;
  font-size:13px;
  line-height:1.7;
  white-space:pre-wrap;
}

/* =========================
   HISTORY
========================= */

.calendar{
  display:grid;
  grid-template-columns:repeat(7,1fr);
  gap:7px;
}

.cal-head{
  color:var(--muted);
  font-size:10px;
  text-align:center;
  padding:5px;
}

.cal-day{
  min-height:44px;
  border-radius:10px;
  background:rgba(255,255,255,.025);
  border:1px solid var(--border);
  display:grid;
  place-items:center;
  font-size:11px;
  color:var(--muted);
}

.cal-day.done{
  background:rgba(98,211,154,.13);
  color:var(--green);
  border-color:rgba(98,211,154,.2);
}

.cal-day.today{
  outline:2px solid rgba(217,179,108,.4);
}

/* =========================
   SETTINGS
========================= */

.settings-list{
  display:flex;
  flex-direction:column;
  gap:10px;
}

.setting-row{
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:15px;
  padding:16px;
  border:1px solid var(--border);
  border-radius:14px;
  background:rgba(255,255,255,.02);
}

.setting-info strong{
  display:block;
  font-size:13px;
}

.setting-info span{
  display:block;
  color:var(--muted);
  font-size:11px;
  margin-top:3px;
}

.switch{
  width:48px;
  height:28px;
  padding:3px;
  border-radius:20px;
  background:#302a36;
  transition:.2s;
}

.switch span{
  display:block;
  width:22px;
  height:22px;
  background:#fff;
  border-radius:50%;
  transition:.2s;
}

.switch.on{
  background:var(--gold);
}

.switch.on span{
  transform:translateX(20px);
}

/* =========================
   MODAL
========================= */

.modal{
  position:fixed;
  inset:0;
  background:rgba(0,0,0,.68);
  backdrop-filter:blur(8px);
  display:none;
  align-items:center;
  justify-content:center;
  padding:20px;
  z-index:300;
}

.modal.show{
  display:flex;
}

.modal-box{
  width:min(500px,100%);
  max-height:90vh;
  overflow:auto;
  background:#18131f;
  border:1px solid var(--border);
  border-radius:22px;
  padding:22px;
  box-shadow:0 30px 80px rgba(0,0,0,.45);
}

.modal-header{
  display:flex;
  align-items:center;
  justify-content:space-between;
  margin-bottom:20px;
}

.close-btn{
  width:36px;
  height:36px;
  border-radius:10px;
  background:var(--surface2);
  color:var(--text);
}

.modal-actions{
  display:flex;
  justify-content:flex-end;
  gap:8px;
  margin-top:18px;
}

/* =========================
   TOAST
========================= */

.toast{
  position:fixed;
  left:50%;
  bottom:28px;
  transform:translate(-50%,120px);
  padding:12px 18px;
  border-radius:12px;
  background:#29212f;
  color:#fff;
  border:1px solid var(--border);
  box-shadow:var(--shadow);
  z-index:500;
  opacity:0;
  transition:.3s;
  font-size:13px;
}

.toast.show{
  opacity:1;
  transform:translate(-50%,0);
}

/* =========================
   EMPTY
========================= */

.empty{
  text-align:center;
  padding:35px 20px;
  color:var(--muted);
}

.empty-icon{
  font-size:35px;
  margin-bottom:10px;
}

/* =========================
   MOBILE
========================= */

.overlay{
  display:none;
}

@media(max-width:900px){
  .sidebar{
    transform:translateX(-100%);
    transition:.25s;
  }

  .sidebar.open{
    transform:translateX(0);
  }

  .main{
    margin-left:0;
  }

  .mobile-menu{
    display:block;
  }

  .overlay.show{
    display:block;
    position:fixed;
    inset:0;
    background:rgba(0,0,0,.55);
    z-index:90;
  }

  .stats-grid{
    grid-template-columns:repeat(2,1fr);
  }

  .goal-grid{
    grid-template-columns:repeat(2,1fr);
  }
}

@media(max-width:680px){
  .topbar{
    height:68px;
    padding:0 15px;
  }

  .content{
    padding:18px 14px 100px;
  }

  .page-title h1{
    font-size:18px;
  }

  .page-title p{
    display:none;
  }

  .hero{
    padding:21px;
    border-radius:21px;
  }

  .hero-top{
    flex-direction:column;
    align-items:flex-start;
  }

  .hero h2{
    font-size:25px;
  }

  .hero-number{
    align-self:center;
    min-width:125px;
    width:125px;
    height:125px;
  }

  .grid-2{
    grid-template-columns:1fr;
  }

  .goal-grid{
    grid-template-columns:1fr;
  }

  .stats-grid{
    gap:9px;
  }

  .stat-card{
    padding:15px;
  }

  .stat-value{
    font-size:22px;
  }

  .card{
    padding:17px;
  }

  .practice-item{
    padding:12px;
  }

  .practice-item .secondary-btn{
    padding:9px 10px;
    font-size:11px;
  }
}

@media(max-width:400px){
  .stats-grid{
    grid-template-columns:1fr 1fr;
  }

  .stat-value{
    font-size:19px;
  }
}
</style>
</head>

<body>

<div class="app">

  <!-- SIDEBAR -->
  <aside class="sidebar" id="sidebar">

    <div class="logo">
      <div class="logo-mark">369</div>
      <div class="logo-text">
        <strong>369</strong>
        <span>Manifest Your Goals</span>
      </div>
    </div>

    <nav class="nav">

      <button class="nav-btn active" data-view="dashboard">
        <span class="nav-icon">⌂</span>
        <span data-i18n="dashboard">Dashboard</span>
      </button>

      <button class="nav-btn" data-view="practice">
        <span class="nav-icon">3</span>
        <span data-i18n="practice">369 Practice</span>
      </button>

      <button class="nav-btn" data-view="goals">
        <span class="nav-icon">◎</span>
        <span data-i18n="goals">My Goals</span>
      </button>

      <button class="nav-btn" data-view="journal">
        <span class="nav-icon">✎</span>
        <span data-i18n="journal">Journal</span>
      </button>

      <button class="nav-btn" data-view="history">
        <span class="nav-icon">▦</span>
        <span data-i18n="history">History</span>
      </button>

      <button class="nav-btn" data-view="settings">
        <span class="nav-icon">⚙</span>
        <span data-i18n="settings">Settings</span>
      </button>

    </nav>

    <div class="sidebar-bottom">
      <div class="mini-profile">
        <div class="avatar">3</div>
        <div>
          <div class="profile-name">369 Member</div>
          <div class="profile-status">Personal Growth</div>
        </div>
      </div>
    </div>

  </aside>

  <div class="overlay" id="overlay"></div>

  <!-- MAIN -->
  <main class="main">

    <header class="topbar">

      <div style="display:flex;align-items:center;gap:10px">

        <button class="icon-btn mobile-menu" id="menuBtn">☰</button>

        <div class="page-title">
          <h1 id="pageTitle">Dashboard</h1>
          <p id="pageSubtitle">Your daily manifestation journey</p>
        </div>

      </div>

      <div class="top-actions">
        <button class="icon-btn" id="quickAddBtn" title="Quick Add">＋</button>
      </div>

    </header>

    <section class="content">

      <!-- ================= DASHBOARD ================= -->
      <section class="view active" id="view-dashboard">

        <div class="hero">

          <div class="hero-top">

            <div>
              <div class="eyebrow">369 DAILY PRACTICE</div>

              <h2 id="greeting">Good day 👋</h2>

              <p id="dashboardIntro">
                Focus your thoughts, write your intention and take action toward the life you want
              </p>

              <button class="primary-btn" style="margin-top:20px" onclick="showView('practice')">
                Start Today's 369
              </button>
            </div>

            <div class="hero-number" id="heroProgress">
              <div>
                <strong id="heroPercent">0%</strong>
                <span>today</span>
              </div>
            </div>

          </div>

        </div>

        <div class="stats-grid">

          <div class="stat-card">
            <div class="stat-label">🔥 Current Streak</div>
            <div class="stat-value" id="statStreak">0</div>
            <div class="stat-small">days</div>
          </div>

          <div class="stat-card">
            <div class="stat-label">✦ Total Practices</div>
            <div class="stat-value" id="statTotal">0</div>
            <div class="stat-small">completed</div>
          </div>

          <div class="stat-card">
            <div class="stat-label">◎ Active Goals</div>
            <div class="stat-value" id="statGoals">0</div>
            <div class="stat-small">goals</div>
          </div>

          <div class="stat-card">
            <div class="stat-label">✓ Completion</div>
            <div class="stat-value" id="statCompletion">0%</div>
            <div class="stat-small">overall</div>
          </div>

        </div>

        <div class="grid-2">

          <div class="card">

            <div class="card-header">
              <div>
                <div class="card-title">Today's 369</div>
                <div class="card-subtitle">Complete all three sessions</div>
              </div>

              <button class="secondary-btn small-btn" onclick="showView('practice')">
                Open
              </button>
            </div>

            <div class="practice-list" id="dashboardPractice"></div>

          </div>

          <div class="card quote-card">

            <div class="quote-mark">“</div>

            <div class="eyebrow">DAILY AFFIRMATION</div>

            <div class="quote" id="dailyQuote">
              I am creating the life I truly want
            </div>

            <div class="quote-meta" id="quoteMeta">
              Believe • Focus • Act
            </div>

            <button class="secondary-btn small-btn" style="width:max-content;margin-top:18px" id="newQuoteBtn">
              New affirmation
            </button>

          </div>

        </div>

      </section>


      <!-- ================= PRACTICE ================= -->
      <section class="view" id="view-practice">

        <div class="hero">

          <div class="eyebrow">YOUR 369 ROUTINE</div>

          <h2>Write it. Feel it. Believe it.</h2>

          <p>
            Choose one clear intention and write the same statement during your 3, 6 and 9 sessions
          </p>

        </div>

        <div class="grid-2">

          <div class="card">

            <div class="card-header">
              <div>
                <div class="card-title">Your Intention</div>
                <div class="card-subtitle">What are you focusing on today?</div>
              </div>
            </div>

            <div class="form-group">
              <label>369 Affirmation</label>
              <textarea id="intentionInput" placeholder="Example: I am confidently building a successful and meaningful life"></textarea>
            </div>

            <button class="primary-btn" id="saveIntentionBtn">
              Save Intention
            </button>

          </div>

          <div class="card">

            <div class="card-header">
              <div>
                <div class="card-title">Today's Sessions</div>
                <div class="card-subtitle" id="practiceDate"></div>
              </div>
            </div>

            <div class="practice-list" id="practiceList"></div>

          </div>

        </div>

        <div class="card" style="margin-top:20px">

          <div class="card-header">
            <div>
              <div class="card-title">How 369 Works</div>
              <div class="card-subtitle">A simple structured reflection routine</div>
            </div>
          </div>

          <div style="display:grid;grid-template-columns:repeat(3,1fr);gap:12px">

            <div class="stat-card">
              <div class="eyebrow">MORNING</div>
              <div class="stat-value">3×</div>
              <div class="stat-small">Write your intention three times</div>
            </div>

            <div class="stat-card">
              <div class="eyebrow">AFTERNOON</div>
              <div class="stat-value">6×</div>
              <div class="stat-small">Return to the same intention</div>
            </div>

            <div class="stat-card">
              <div class="eyebrow">EVENING</div>
              <div class="stat-value">9×</div>
              <div class="stat-small">Finish the daily practice</div>
            </div>

          </div>

        </div>

      </section>


      <!-- ================= GOALS ================= -->
      <section class="view" id="view-goals">

        <div class="card" style="margin-bottom:20px">

          <div class="card-header">
            <div>
              <div class="card-title">My Goals</div>
              <div class="card-subtitle">Turn intentions into measurable actions</div>
            </div>

            <button class="primary-btn" id="addGoalBtn">
              + Add Goal
            </button>
          </div>

          <div class="goal-grid" id="goalGrid"></div>

        </div>

      </section>


      <!-- ================= JOURNAL ================= -->
      <section class="view" id="view-journal">

        <div class="grid-2">

          <div class="card">

            <div class="card-header">
              <div>
                <div class="card-title">Daily Journal</div>
                <div class="card-subtitle">Write freely about today's journey</div>
              </div>
            </div>

            <div class="form-group">
              <label>Today's Reflection</label>
              <textarea id="journalInput" placeholder="What are you grateful for? What did you learn? What action will you take?"></textarea>
            </div>

            <button class="primary-btn" id="saveJournalBtn">
              Save Journal
            </button>

          </div>

          <div class="card">

            <div class="card-header">
              <div>
                <div class="card-title">Gratitude</div>
                <div class="card-subtitle">Three things you appreciate today</div>
              </div>
            </div>

            <div class="form-group">
              <label>1</label>
              <input id="gratitude1" placeholder="I am grateful for...">
            </div>

            <div class="form-group">
              <label>2</label>
              <input id="gratitude2" placeholder="I am grateful for...">
            </div>

            <div class="form-group">
              <label>3</label>
              <input id="gratitude3" placeholder="I am grateful for...">
            </div>

            <button class="secondary-btn" id="saveGratitudeBtn">
              Save Gratitude
            </button>

          </div>

        </div>

        <div class="card" style="margin-top:20px">

          <div class="card-header">
            <div>
              <div class="card-title">Journal History</div>
              <div class="card-subtitle">Your previous reflections</div>
            </div>
          </div>

          <div class="journal-list" id="journalList"></div>

        </div>

      </section>


      <!-- ================= HISTORY ================= -->
      <section class="view" id="view-history">

        <div class="stats-grid">

          <div class="stat-card">
            <div class="stat-label">Current Streak</div>
            <div class="stat-value" id="historyStreak">0</div>
          </div>

          <div class="stat-card">
            <div class="stat-label">Best Streak</div>
            <div class="stat-value" id="bestStreak">0</div>
          </div>

          <div class="stat-card">
            <div class="stat-label">Completed Days</div>
            <div class="stat-value" id="completedDays">0</div>
          </div>

          <div class="stat-card">
            <div class="stat-label">Total Sessions</div>
            <div class="stat-value" id="historySessions">0</div>
          </div>

        </div>

        <div class="card">

          <div class="card-header">
            <div>
              <div class="card-title" id="calendarTitle">Practice Calendar</div>
              <div class="card-subtitle">Your completed 369 days</div>
            </div>
          </div>

          <div class="calendar" id="calendar"></div>

        </div>

      </section>


      <!-- ================= SETTINGS ================= -->
      <section class="view" id="view-settings">

        <div class="grid-2">

          <div class="card">

            <div class="card-header">
              <div>
                <div class="card-title">Preferences</div>
                <div class="card-subtitle">Customize your 369 experience</div>
              </div>
            </div>

            <div class="settings-list">

              <div class="setting-row">
                <div class="setting-info">
                  <strong>Language</strong>
                  <span>Myanmar / English</span>
                </div>

                <select id="languageSelect" style="width:130px">
                  <option value="en">English</option>
                  <option value="my">မြန်မာ</option>
                </select>
              </div>

              <div class="setting-row">
                <div class="setting-info">
                  <strong>Daily Reminder</strong>
                  <span>Keep your routine consistent</span>
                </div>

                <button class="switch" id="reminderSwitch">
                  <span></span>
                </button>
              </div>

            </div>

          </div>

          <div class="card">

            <div class="card-header">
              <div>
                <div class="card-title">Data</div>
                <div class="card-subtitle">Manage your local app data</div>
              </div>
            </div>

            <div class="settings-list">

              <div class="setting-row">
                <div class="setting-info">
                  <strong>Export Data</strong>
                  <span>Download your 369 data as JSON</span>
                </div>

                <button class="secondary-btn small-btn" id="exportBtn">
                  Export
                </button>
              </div>

              <div class="setting-row">
                <div class="setting-info">
                  <strong>Reset App</strong>
                  <span>Delete all locally stored data</span>
                </div>

                <button class="danger-btn small-btn" id="resetBtn">
                  Reset
                </button>
              </div>

            </div>

          </div>

        </div>

      </section>

    </section>

  </main>
</div>


<!-- GOAL MODAL -->
<div class="modal" id="goalModal">

  <div class="modal-box">

    <div class="modal-header">
      <div>
        <div class="card-title">Create Goal</div>
        <div class="card-subtitle">Define something meaningful</div>
      </div>

      <button class="close-btn" onclick="closeModal('goalModal')">×</button>
    </div>

    <div class="form-group">
      <label>Goal Name</label>
      <input id="goalName" placeholder="Example: Build my business">
    </div>

    <div class="form-group">
      <label>Category</label>
      <select id="goalCategory">
        <option>💰 Money</option>
        <option>💼 Career</option>
        <option>🚀 Business</option>
        <option>❤️ Relationships</option>
        <option>🌱 Personal Growth</option>
        <option>🏡 Lifestyle</option>
        <option>✨ Other</option>
      </select>
    </div>

    <div class="form-group">
      <label>Target Date</label>
      <input type="date" id="goalDate">
    </div>

    <div class="form-group">
      <label>Progress %</label>
      <input type="number" id="goalProgress" min="0" max="100" value="0">
    </div>

    <div class="modal-actions">
      <button class="secondary-btn" onclick="closeModal('goalModal')">Cancel</button>
      <button class="primary-btn" id="saveGoalBtn">Create Goal</button>
    </div>

  </div>

</div>


<!-- QUICK ADD MODAL -->
<div class="modal" id="quickModal">

  <div class="modal-box">

    <div class="modal-header">
      <div>
        <div class="card-title">Quick Add</div>
        <div class="card-subtitle">Choose what you want to create</div>
      </div>

      <button class="close-btn" onclick="closeModal('quickModal')">×</button>
    </div>

    <div style="display:grid;gap:10px">

      <button class="secondary-btn" onclick="closeModal('quickModal');showView('practice')">
        ✦ Start 369 Practice
      </button>

      <button class="secondary-btn" onclick="closeModal('quickModal');openGoalModal()">
        ◎ Add Goal
      </button>

      <button class="secondary-btn" onclick="closeModal('quickModal');showView('journal')">
        ✎ Write Journal
      </button>

    </div>

  </div>

</div>


<div class="toast" id="toast"></div>


<script>
"use strict";

/* =========================================================
   369 APP V1
   LocalStorage based
========================================================= */

const STORAGE_KEY = "369_manifest_app_v1";

const defaultData = {
  intention: "",
  practices: {},
  goals: [],
  journals: [],
  gratitude: {},
  settings: {
    language: "en",
    reminder: false
  }
};

let data = loadData();

const quotes = [
  "I am creating the life I truly want",
  "I trust myself to take the next right step",
  "I am worthy of meaningful success",
  "I focus on what I can build today",
  "I welcome growth, clarity and abundance",
  "I am becoming more disciplined every day",
  "My actions are aligned with my goals",
  "I choose progress over perfection",
  "I believe in my ability to create change",
  "I am grateful for the opportunities in front of me"
];

const translations = {
  en:{
    dashboard:"Dashboard",
    practice:"369 Practice",
    goals:"My Goals",
    journal:"Journal",
    history:"History",
    settings:"Settings"
  },
  my:{
    dashboard:"ပင်မစာမျက်နှာ",
    practice:"369 လေ့ကျင့်မှု",
    goals:"ကျွန်ုပ်၏ ရည်မှန်းချက်များ",
    journal:"မှတ်တမ်း",
    history:"မှတ်တမ်းများ",
    settings:"ဆက်တင်"
  }
};

const pageInfo = {
  dashboard:{
    en:["Dashboard","Your daily manifestation journey"],
    my:["ပင်မစာမျက်နှာ","နေ့စဉ် ရည်မှန်းချက်ခရီးစဉ်"]
  },
  practice:{
    en:["369 Practice","Complete your 3 • 6 • 9 routine"],
    my:["369 လေ့ကျင့်မှု","3 • 6 • 9 နေ့စဉ်လုပ်ဆောင်မှု"]
  },
  goals:{
    en:["My Goals","Turn intentions into measurable actions"],
    my:["ကျွန်ုပ်၏ ရည်မှန်းချက်များ","ရည်ရွယ်ချက်ကို လုပ်ဆောင်ချက်အဖြစ် ပြောင်းလဲပါ"]
  },
  journal:{
    en:["Journal","Reflect, appreciate and learn"],
    my:["မှတ်တမ်း","ပြန်လည်သုံးသပ်ပြီး တန်ဖိုးထားပါ"]
  },
  history:{
    en:["History","Track your consistency"],
    my:["မှတ်တမ်းများ","သင်၏ လုပ်ဆောင်မှုမှန်ကန်မှုကို ကြည့်ပါ"]
  },
  settings:{
    en:["Settings","Customize your experience"],
    my:["ဆက်တင်","App အတွေ့အကြုံကို ပြင်ဆင်ပါ"]
  }
};


/* =========================================================
   STORAGE
========================================================= */

function loadData(){
  try{
    const raw = localStorage.getItem(STORAGE_KEY);

    if(!raw){
      return JSON.parse(JSON.stringify(defaultData));
    }

    const parsed = JSON.parse(raw);

    return {
      ...JSON.parse(JSON.stringify(defaultData)),
      ...parsed,
      settings:{
        ...defaultData.settings,
        ...(parsed.settings || {})
      }
    };

  }catch(error){
    console.error(error);
    return JSON.parse(JSON.stringify(defaultData));
  }
}

function saveData(){
  localStorage.setItem(STORAGE_KEY,JSON.stringify(data));
}


/* =========================================================
   DATE
========================================================= */

function dateKey(date = new Date()){
  const y = date.getFullYear();
  const m = String(date.getMonth()+1).padStart(2,"0");
  const d = String(date.getDate()).padStart(2,"0");

  return `${y}-${m}-${d}`;
}

function formatDate(key){
  const date = new Date(key+"T00:00:00");

  return date.toLocaleDateString(
    data.settings.language === "my" ? "my-MM" : "en-US",
    {
      year:"numeric",
      month:"short",
      day:"numeric"
    }
  );
}

function todayData(){
  const key = dateKey();

  if(!data.practices[key]){
    data.practices[key] = {
      morning:false,
      afternoon:false,
      evening:false
    };
  }

  return data.practices[key];
}


/* =========================================================
   PRACTICE
========================================================= */

function practiceCount(day){
  if(!day) return 0;

  return [
    day.morning,
    day.afternoon,
    day.evening
  ].filter(Boolean).length;
}

function togglePractice(type){

  if(!data.intention.trim()){
    showToast(
      data.settings.language === "my"
      ? "အရင်ဆုံး 369 intention တစ်ခုရေးပြီး Save လုပ်ပါ"
      : "Write and save your 369 intention first"
    );

    showView("practice");
    return;
  }

  const day = todayData();

  day[type] = !day[type];

  saveData();

  renderAll();

  if(day[type]){
    showToast(
      data.settings.language === "my"
      ? "ဒီ session ပြီးပါပြီ ✓"
      : "Session completed ✓"
    );
  }
}

function practiceHTML(day){

  const items = [
    {
      type:"morning",
      number:3,
      title:"Morning",
      my:"မနက်ပိုင်း"
    },
    {
      type:"afternoon",
      number:6,
      title:"Afternoon",
      my:"နေ့လယ်ပိုင်း"
    },
    {
      type:"evening",
      number:9,
      title:"Evening",
      my:"ညပိုင်း"
    }
  ];

  const isMy = data.settings.language === "my";

  return items.map(item=>{

    const done = !!day[item.type];

    return `
      <div class="practice-item ${done ? "complete":""}">

        <div class="practice-number">
          ${done ? "✓" : item.number}
        </div>

        <div class="practice-info">
          <strong>${isMy ? item.my : item.title}</strong>
          <span>
            ${isMy
              ? `${item.number} ကြိမ် ရေးပါ`
              : `Write your intention ${item.number} times`
            }
          </span>
        </div>

        <button
          class="${done ? "secondary-btn":"primary-btn"} small-btn"
          onclick="togglePractice('${item.type}')"
        >
          ${done
            ? (isMy ? "ပြီးပြီ" : "Done")
            : (isMy ? "စလုပ်" : "Start")
          }
        </button>

      </div>
    `;

  }).join("");
}


/* =========================================================
   STREAK
========================================================= */

function completedDay(key){
  return practiceCount(data.practices[key]) === 3;
}

function getStreak(){

  let streak = 0;
  const d = new Date();

  if(!completedDay(dateKey(d))){
    d.setDate(d.getDate()-1);
  }

  while(completedDay(dateKey(d))){
    streak++;
    d.setDate(d.getDate()-1);

    if(streak > 10000) break;
  }

  return streak;
}

function getBestStreak(){

  const keys = Object.keys(data.practices).sort();

  let best = 0;
  let current = 0;
  let previous = null;

  keys.forEach(key=>{

    if(!completedDay(key)){
      current = 0;
      previous = key;
      return;
    }

    if(previous){

      const a = new Date(previous+"T00:00:00");
      const b = new Date(key+"T00:00:00");

      const diff = Math.round((b-a)/86400000);

      if(diff === 1){
        current++;
      }else{
        current = 1;
      }

    }else{
      current = 1;
    }

    best = Math.max(best,current);
    previous = key;

  });

  return best;
}


/* =========================================================
   DASHBOARD
========================================================= */

function renderDashboard(){

  const today = todayData();
  const count = practiceCount(today);
  const percent = Math.round((count/3)*100);

  document.getElementById("heroPercent").textContent = percent+"%";

  document.getElementById("heroProgress")
    .style.setProperty("--progress",percent+"%");

  document.getElementById("statStreak").textContent = getStreak();

  const totalSessions = Object.values(data.practices)
    .reduce((sum,day)=>sum+practiceCount(day),0);

  document.getElementById("statTotal").textContent = totalSessions;
  document.getElementById("statGoals").textContent = data.goals.length;

  const totalPossible = Object.keys(data.practices).length * 3;

  const overall = totalPossible
    ? Math.round((totalSessions/totalPossible)*100)
    : 0;

  document.getElementById("statCompletion").textContent = overall+"%";

  document.getElementById("dashboardPractice").innerHTML =
    practiceHTML(today);

  const hour = new Date().getHours();

  let greeting = "Good day 👋";

  if(hour < 12) greeting = "Good morning 👋";
  else if(hour < 18) greeting = "Good afternoon 👋";
  else greeting = "Good evening 👋";

  if(data.settings.language === "my"){
    if(hour < 12) greeting = "မင်္ဂလာနံနက်ခင်းပါ 👋";
    else if(hour < 18) greeting = "မင်္ဂလာနေ့လယ်ခင်းပါ 👋";
    else greeting = "မင်္ဂလာညနေခင်းပါ 👋";
  }

  document.getElementById("greeting").textContent = greeting;
}


/* =========================================================
   PRACTICE VIEW
========================================================= */

function renderPractice(){

  const day = todayData();

  document.getElementById("practiceList").innerHTML =
    practiceHTML(day);

  document.getElementById("intentionInput").value =
    data.intention || "";

  document.getElementById("practiceDate").textContent =
    formatDate(dateKey());

}


/* =========================================================
   GOALS
========================================================= */

function renderGoals(){

  const grid = document.getElementById("goalGrid");

  if(!data.goals.length){

    grid.innerHTML = `
      <div class="empty" style="grid-column:1/-1">
        <div class="empty-icon">◎</div>
        <div>No goals yet</div>
        <div style="font-size:11px;margin-top:5px">
          Create your first meaningful goal
        </div>
      </div>
    `;

    return;
  }

  grid.innerHTML = data.goals.map((goal,index)=>{

    const progress = Math.max(
      0,
      Math.min(100,Number(goal.progress)||0)
    );

    return `
      <div class="goal-card">

        <div class="goal-top">
          <div class="goal-icon">${goal.category.split(" ")[0]}</div>
          <div class="goal-percent">${progress}%</div>
        </div>

        <h3>${escapeHTML(goal.name)}</h3>

        <p>
          ${escapeHTML(goal.category)}
          ${goal.date ? " • "+formatDate(goal.date):""}
        </p>

        <div class="progress">
          <span style="width:${progress}%"></span>
        </div>

        <div class="goal-footer">
          <span>Progress</span>

          <button
            class="danger-btn small-btn"
            onclick="deleteGoal(${index})"
          >
            Delete
          </button>
        </div>

      </div>
    `;

  }).join("");
}

function openGoalModal(){

  document.getElementById("goalName").value = "";
  document.getElementById("goalCategory").value = "💰 Money";
  document.getElementById("goalDate").value = "";
  document.getElementById("goalProgress").value = 0;

  document.getElementById("goalModal").classList.add("show");
}

function saveGoal(){

  const name = document.getElementById("goalName").value.trim();

  if(!name){
    showToast("Please enter a goal name");
    return;
  }

  const progress = Number(
    document.getElementById("goalProgress").value
  ) || 0;

  data.goals.push({
    id:Date.now(),
    name,
    category:document.getElementById("goalCategory").value,
    date:document.getElementById("goalDate").value,
    progress:Math.max(0,Math.min(100,progress))
  });

  saveData();
  closeModal("goalModal");
  renderAll();

  showToast("Goal created ✓");
}

function deleteGoal(index){

  if(!confirm("Delete this goal?")) return;

  data.goals.splice(index,1);

  saveData();
  renderAll();

  showToast("Goal deleted");
}


/* =========================================================
   JOURNAL
========================================================= */

function renderJournal(){

  const list = document.getElementById("journalList");

  if(!data.journals.length){

    list.innerHTML = `
      <div class="empty">
        <div class="empty-icon">✎</div>
        <div>No journal entries yet</div>
      </div>
    `;

  }else{

    list.innerHTML = data.journals
      .slice()
      .reverse()
      .map((entry,index)=>`

        <div class="journal-entry">

          <div class="journal-date">
            ${formatDate(entry.date)}
          </div>

          <div class="journal-text">
            ${escapeHTML(entry.text)}
          </div>

        </div>

      `).join("");

  }

  const todayGratitude = data.gratitude[dateKey()] || [];

  document.getElementById("gratitude1").value =
    todayGratitude[0] || "";

  document.getElementById("gratitude2").value =
    todayGratitude[1] || "";

  document.getElementById("gratitude3").value =
    todayGratitude[2] || "";
}

function saveJournal(){

  const text = document.getElementById("journalInput")
    .value.trim();

  if(!text){
    showToast("Please write something first");
    return;
  }

  data.journals.push({
    id:Date.now(),
    date:dateKey(),
    text
  });

  document.getElementById("journalInput").value = "";

  saveData();
  renderJournal();

  showToast("Journal saved ✓");
}

function saveGratitude(){

  data.gratitude[dateKey()] = [
    document.getElementById("gratitude1").value.trim(),
    document.getElementById("gratitude2").value.trim(),
    document.getElementById("gratitude3").value.trim()
  ];

  saveData();

  showToast("Gratitude saved ✓");
}


/* =========================================================
   HISTORY / CALENDAR
========================================================= */

function renderHistory(){

  const current = getStreak();
  const best = getBestStreak();

  const completed = Object.keys(data.practices)
    .filter(completedDay).length;

  const sessions = Object.values(data.practices)
    .reduce((sum,day)=>sum+practiceCount(day),0);

  document.getElementById("historyStreak").textContent = current;
  document.getElementById("bestStreak").textContent = best;
  document.getElementById("completedDays").textContent = completed;
  document.getElementById("historySessions").textContent = sessions;

  const now = new Date();

  const year = now.getFullYear();
  const month = now.getMonth();

  document.getElementById("calendarTitle").textContent =
    now.toLocaleDateString(
      data.settings.language === "my" ? "my-MM":"en-US",
      {
        month:"long",
        year:"numeric"
      }
    );

  const first = new Date(year,month,1);
  const last = new Date(year,month+1,0);

  let startDay = first.getDay();

  const calendar = document.getElementById("calendar");

  const heads = data.settings.language === "my"
    ? ["တ","တ","ဗု","ရ","ကြာ","သော","စ"]
    : ["Sun","Mon","Tue","Wed","Thu","Fri","Sat"];

  let html = heads.map(h=>`
    <div class="cal-head">${h}</div>
  `).join("");

  for(let i=0;i<startDay;i++){
    html += `<div></div>`;
  }

  for(let day=1;day<=last.getDate();day++){

    const key =
      `${year}-${String(month+1).padStart(2,"0")}-${String(day).padStart(2,"0")}`;

    const done = completedDay(key);
    const today = key === dateKey();

    html += `
      <div class="cal-day ${done?"done":""} ${today?"today":""}">
        ${day}
      </div>
    `;
  }

  calendar.innerHTML = html;
}


/* =========================================================
   SETTINGS
========================================================= */

function renderSettings(){

  document.getElementById("languageSelect").value =
    data.settings.language;

  document.getElementById("reminderSwitch")
    .classList.toggle("on",data.settings.reminder);

  applyLanguage();
}

function applyLanguage(){

  const lang = data.settings.language;

  document.querySelectorAll("[data-i18n]")
    .forEach(el=>{

      const key = el.dataset.i18n;

      if(translations[lang][key]){
        el.textContent = translations[lang][key];
      }

    });

  const active =
    document.querySelector(".nav-btn.active");

  if(active){

    const view = active.dataset.view;

    document.getElementById("pageTitle").textContent =
      pageInfo[view][lang][0];

    document.getElementById("pageSubtitle").textContent =
      pageInfo[view][lang][1];

  }
}


/* =========================================================
   NAVIGATION
========================================================= */

function showView(view){

  document.querySelectorAll(".view")
    .forEach(v=>v.classList.remove("active"));

  const target = document.getElementById("view-"+view);

  if(target) target.classList.add("active");

  document.querySelectorAll(".nav-btn")
    .forEach(btn=>{
      btn.classList.toggle(
        "active",
        btn.dataset.view === view
      );
    });

  const lang = data.settings.language;

  document.getElementById("pageTitle").textContent =
    pageInfo[view][lang][0];

  document.getElementById("pageSubtitle").textContent =
    pageInfo[view][lang][1];

  closeSidebar();

  window.scrollTo({
    top:0,
    behavior:"smooth"
  });
}


/* =========================================================
   MODAL
========================================================= */

function closeModal(id){
  document.getElementById(id).classList.remove("show");
}


/* =========================================================
   QUOTES
========================================================= */

function newQuote(){

  const quote =
    quotes[Math.floor(Math.random()*quotes.length)];

  document.getElementById("dailyQuote").textContent =
    quote;

  document.getElementById("quoteMeta").textContent =
    data.settings.language === "my"
    ? "ယုံကြည်ပါ • အာရုံစိုက်ပါ • လုပ်ဆောင်ပါ"
    : "Believe • Focus • Act";
}


/* =========================================================
   EXPORT
========================================================= */

function exportData(){

  const blob = new Blob(
    [JSON.stringify(data,null,2)],
    {type:"application/json"}
  );

  const url = URL.createObjectURL(blob);

  const a = document.createElement("a");

  a.href = url;
  a.download = "369-backup-"+dateKey()+".json";

  document.body.appendChild(a);
  a.click();
  a.remove();

  URL.revokeObjectURL(url);

  showToast("Data exported ✓");
}


/* =========================================================
   RESET
========================================================= */

function resetApp(){

  const yes = confirm(
    "This will permanently delete your 369 data. Continue?"
  );

  if(!yes) return;

  localStorage.removeItem(STORAGE_KEY);

  data = loadData();

  renderAll();

  showToast("App data reset");
}


/* =========================================================
   MOBILE SIDEBAR
========================================================= */

function closeSidebar(){

  document.getElementById("sidebar")
    .classList.remove("open");

  document.getElementById("overlay")
    .classList.remove("show");
}

function toggleSidebar(){

  document.getElementById("sidebar")
    .classList.toggle("open");

  document.getElementById("overlay")
    .classList.toggle("show");
}


/* =========================================================
   TOAST
========================================================= */

let toastTimer;

function showToast(message){

  const toast = document.getElementById("toast");

  toast.textContent = message;
  toast.classList.add("show");

  clearTimeout(toastTimer);

  toastTimer = setTimeout(()=>{
    toast.classList.remove("show");
  },2500);
}


/* =========================================================
   SECURITY / DISPLAY
========================================================= */

function escapeHTML(value){

  return String(value)
    .replaceAll("&","&amp;")
    .replaceAll("<","&lt;")
    .replaceAll(">","&gt;")
    .replaceAll('"',"&quot;")
    .replaceAll("'","&#039;");
}


/* =========================================================
   RENDER ALL
========================================================= */

function renderAll(){

  renderDashboard();
  renderPractice();
  renderGoals();
  renderJournal();
  renderHistory();
  renderSettings();

}


/* =========================================================
   EVENTS
========================================================= */

document.querySelectorAll(".nav-btn")
  .forEach(btn=>{

    btn.addEventListener("click",()=>{
      showView(btn.dataset.view);
    });

  });


document.getElementById("menuBtn")
  .addEventListener("click",toggleSidebar);


document.getElementById("overlay")
  .addEventListener("click",closeSidebar);


document.getElementById("quickAddBtn")
  .addEventListener("click",()=>{
    document.getElementById("quickModal")
      .classList.add("show");
  });


document.getElementById("newQuoteBtn")
  .addEventListener("click",newQuote);


document.getElementById("saveIntentionBtn")
  .addEventListener("click",()=>{

    const value =
      document.getElementById("intentionInput")
        .value.trim();

    if(!value){
      showToast("Please write your intention");
      return;
    }

    data.intention = value;

    saveData();

    showToast("369 intention saved ✓");
  });


document.getElementById("addGoalBtn")
  .addEventListener("click",openGoalModal);


document.getElementById("saveGoalBtn")
  .addEventListener("click",saveGoal);


document.getElementById("saveJournalBtn")
  .addEventListener("click",saveJournal);


document.getElementById("saveGratitudeBtn")
  .addEventListener("click",saveGratitude);


document.getElementById("languageSelect")
  .addEventListener("change",event=>{

    data.settings.language = event.target.value;

    saveData();
    renderAll();

    showToast(
      event.target.value === "my"
      ? "ဘာသာစကား ပြောင်းပြီးပါပြီ"
      : "Language changed"
    );

  });


document.getElementById("reminderSwitch")
  .addEventListener("click",()=>{

    data.settings.reminder =
      !data.settings.reminder;

    saveData();
    renderSettings();

    showToast(
      data.settings.reminder
      ? "Reminder enabled"
      : "Reminder disabled"
    );

  });


document.getElementById("exportBtn")
  .addEventListener("click",exportData);


document.getElementById("resetBtn")
  .addEventListener("click",resetApp);


/* Close modal when clicking outside */

document.querySelectorAll(".modal")
  .forEach(modal=>{

    modal.addEventListener("click",event=>{

      if(event.target === modal){
        modal.classList.remove("show");
      }

    });

  });


/* =========================================================
   INITIALIZE
========================================================= */

renderAll();

</script>

</body>
</html>
```
