<!DOCTYPE html>

<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CALI ÉLITE — Programme 12 Mois</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=DM+Sans:wght@300;400;500;600&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{
  --gold:#B8924A;--gold-light:#D4AA6A;--gold-pale:#F5ECD7;
  --white:#FFFFFF;--off-white:#FAFAF8;--cream:#F7F4EF;--pearl:#F0EDE8;
  --charcoal:#1A1A1A;--dark:#2C2C2C;--mid:#6B6B6B;--light:#A8A8A8;
  --border:#E8E4DE;--shadow:0 2px 20px rgba(0,0,0,.07);--shadow-lg:0 8px 40px rgba(0,0,0,.12);
  --radius:16px;--radius-sm:10px;
  --blue:#2A5F8A;--red:#8A2A2A;--green:#2A6B3A;--orange:#C4622D;
}
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'DM Sans',sans-serif;background:var(--off-white);color:var(--charcoal);min-height:100vh;overflow-x:hidden;}

/* ── HEADER ── */
header{background:var(–white);border-bottom:1px solid var(–border);padding:0 24px;position:sticky;top:0;z-index:100;box-shadow:0 1px 12px rgba(0,0,0,.05);}
.header-inner{max-width:1100px;margin:0 auto;display:flex;align-items:center;justify-content:space-between;height:64px;}
.logo{font-family:‘Playfair Display’,serif;font-size:22px;font-weight:900;color:var(–charcoal);letter-spacing:-.5px;}
.logo span{color:var(–gold);}
.header-meta{font-size:12px;color:var(–mid);font-family:‘DM Mono’,monospace;letter-spacing:.5px;}

/* ── NAV ── */
nav{background:var(–white);border-bottom:1px solid var(–border);padding:0 24px;overflow-x:auto;scrollbar-width:none;}
nav::-webkit-scrollbar{display:none;}
.nav-inner{max-width:1100px;margin:0 auto;display:flex;}
.nav-btn{padding:14px 16px;background:none;border:none;font-family:‘DM Sans’,sans-serif;font-size:13px;font-weight:500;color:var(–mid);cursor:pointer;white-space:nowrap;border-bottom:2px solid transparent;transition:all .2s;display:flex;align-items:center;gap:5px;}
.nav-btn:hover{color:var(–charcoal);}
.nav-btn.active{color:var(–gold);border-bottom-color:var(–gold);font-weight:600;}

/* ── MAIN ── */
main{max-width:1100px;margin:0 auto;padding:28px 24px 100px;}
.tab{display:none;}
.tab.active{display:block;}
.page-title{font-family:‘Playfair Display’,serif;font-size:26px;font-weight:700;margin-bottom:4px;}
.page-sub{font-size:13px;color:var(–mid);margin-bottom:24px;}

/* ── CARDS ── */
.card{background:var(–white);border-radius:var(–radius);border:1px solid var(–border);padding:24px;box-shadow:var(–shadow);}
.card-title{font-family:‘Playfair Display’,serif;font-size:16px;font-weight:700;margin-bottom:14px;display:flex;align-items:center;gap:8px;}
.grid-2{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
.grid-3{display:grid;grid-template-columns:1fr 1fr 1fr;gap:14px;}
@media(max-width:768px){.grid-2,.grid-3{grid-template-columns:1fr;}}

/* accès direct — pas d’écran de connexion */

/* ── FÉLICITATIONS ── */
.congrats-overlay{position:fixed;inset:0;background:rgba(0,0,0,.5);z-index:400;display:none;align-items:center;justify-content:center;}
.congrats-overlay.show{display:flex;}
.congrats-box{background:var(–white);border-radius:var(–radius);padding:40px;text-align:center;max-width:360px;width:90%;box-shadow:var(–shadow-lg);animation:popIn .4s cubic-bezier(.34,1.56,.64,1);}
@keyframes popIn{from{transform:scale(.7);opacity:0;}to{transform:scale(1);opacity:1;}}
.congrats-emoji{font-size:60px;margin-bottom:10px;}
.congrats-title{font-family:‘Playfair Display’,serif;font-size:22px;font-weight:700;margin-bottom:8px;}
.congrats-sub{font-size:13px;color:var(–mid);margin-bottom:20px;line-height:1.6;}
.congrats-btn{padding:11px 28px;background:var(–charcoal);color:var(–white);border:none;border-radius:var(–radius-sm);font-family:‘DM Sans’,sans-serif;font-size:13px;font-weight:600;cursor:pointer;}

/* ════════════════════════════
ACCUEIL
════════════════════════════ */
.home-hero{border-radius:var(–radius);padding:32px 36px;color:var(–white);margin-bottom:24px;position:relative;overflow:hidden;min-height:180px;display:flex;flex-direction:column;justify-content:flex-end;}
.home-hero-bg{position:absolute;inset:0;background:linear-gradient(135deg,#1A1A1A 0%,#2d2d2d 100%);}
.home-hero-accent{position:absolute;top:-60px;right:-60px;width:260px;height:260px;border-radius:50%;background:var(–gold);opacity:.07;}
.home-hero-content{position:relative;z-index:1;}
.home-hero-greeting{font-family:‘DM Mono’,monospace;font-size:11px;letter-spacing:2px;color:var(–gold-light);margin-bottom:10px;text-transform:uppercase;}
.home-hero-msg{font-family:‘Playfair Display’,serif;font-size:24px;font-weight:700;line-height:1.4;margin-bottom:12px;}
.home-hero-submsg{font-size:13px;color:rgba(255,255,255,.55);line-height:1.5;}
.home-hero-badges{display:flex;gap:8px;margin-top:16px;flex-wrap:wrap;}
.home-badge{padding:5px 13px;border-radius:20px;font-size:11px;font-weight:700;letter-spacing:.5px;}
.home-badge-phase{background:var(–gold);color:var(–white);}
.home-badge-deload{background:var(–orange);color:var(–white);}
.home-badge-rest{background:rgba(255,255,255,.15);color:rgba(255,255,255,.8);}

.home-stats{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;margin-bottom:24px;}
@media(max-width:600px){.home-stats{grid-template-columns:repeat(2,1fr);}}
.home-stat{background:var(–white);border:1px solid var(–border);border-radius:var(–radius-sm);padding:18px 14px;text-align:center;box-shadow:var(–shadow);}
.home-stat-val{font-family:‘Playfair Display’,serif;font-size:28px;font-weight:700;color:var(–charcoal);line-height:1;margin-bottom:4px;}
.home-stat-val.gold{color:var(–gold);}
.home-stat-val.green{color:var(–green);}
.home-stat-label{font-size:10px;color:var(–mid);letter-spacing:.5px;text-transform:uppercase;}

.home-shortcuts{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-bottom:24px;}
@media(max-width:500px){.home-shortcuts{grid-template-columns:1fr;}}
.shortcut-btn{background:var(–white);border:1.5px solid var(–border);border-radius:var(–radius);padding:18px;text-align:center;cursor:pointer;transition:all .2s;box-shadow:var(–shadow);}
.shortcut-btn:hover{border-color:var(–gold);transform:translateY(-2px);box-shadow:var(–shadow-lg);}
.shortcut-icon{font-size:28px;margin-bottom:8px;}
.shortcut-label{font-size:13px;font-weight:600;color:var(–charcoal);}
.shortcut-sub{font-size:11px;color:var(–mid);margin-top:2px;}

.home-bottom{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
@media(max-width:600px){.home-bottom{grid-template-columns:1fr;}}
.tip-daily-card{background:var(–charcoal);border-radius:var(–radius);padding:22px;color:var(–white);position:relative;overflow:hidden;}
.tip-daily-card::after{content:’”’;position:absolute;bottom:-20px;right:14px;font-family:‘Playfair Display’,serif;font-size:110px;color:var(–gold);opacity:.1;line-height:1;}
.tip-daily-label{font-size:10px;letter-spacing:2px;color:var(–gold-light);margin-bottom:10px;font-family:‘DM Mono’,monospace;}
.tip-daily-text{font-family:‘Playfair Display’,serif;font-size:15px;line-height:1.6;position:relative;z-index:1;}
.tip-daily-src{font-size:11px;color:rgba(255,255,255,.4);margin-top:8px;}
.tip-daily-nav{display:flex;gap:6px;margin-top:12px;}
.tip-daily-nav button{padding:4px 12px;background:rgba(255,255,255,.1);border:1px solid rgba(255,255,255,.15);border-radius:12px;color:var(–white);font-size:11px;cursor:pointer;font-family:‘DM Sans’,sans-serif;transition:all .2s;}
.tip-daily-nav button:hover{background:var(–gold);}

.upcoming-card{background:var(–white);border:1px solid var(–border);border-radius:var(–radius);padding:22px;box-shadow:var(–shadow);}
.upcoming-item{display:flex;align-items:center;gap:12px;padding:8px 0;border-bottom:1px solid var(–border);}
.upcoming-item:last-child{border:none;}
.upcoming-day{font-family:‘DM Mono’,monospace;font-size:10px;color:var(–mid);width:28px;flex-shrink:0;}
.upcoming-name{font-size:13px;font-weight:600;flex:1;}
.upcoming-badge{font-size:10px;padding:2px 8px;border-radius:10px;font-weight:700;}

/* ════════════════════════════
PROGRAMME
════════════════════════════ */
.week-day-bar{display:flex;gap:8px;margin-bottom:24px;overflow-x:auto;padding-bottom:4px;}
.week-day-btn{flex-shrink:0;padding:10px 14px;border-radius:var(–radius-sm);border:1.5px solid var(–border);background:var(–white);cursor:pointer;text-align:center;transition:all .2s;min-width:72px;}
.week-day-btn:hover{border-color:var(–gold-light);}
.week-day-btn.active{background:var(–charcoal);border-color:var(–charcoal);color:var(–white);}
.week-day-btn.today-day{border-color:var(–gold);box-shadow:0 0 0 2px var(–gold-pale);}
.week-day-btn.today-day.active{background:var(–gold);border-color:var(–gold);}
.week-day-name{font-size:11px;font-weight:700;letter-spacing:.5px;color:inherit;}
.week-day-session{font-size:10px;color:var(–mid);margin-top:2px;}
.week-day-btn.active .week-day-session{color:rgba(255,255,255,.6);}
.week-day-dot{width:6px;height:6px;border-radius:50%;margin:4px auto 0;}

.phase-selector{display:flex;gap:8px;margin-bottom:20px;flex-wrap:wrap;}
.phase-tab{padding:7px 16px;border-radius:20px;border:1.5px solid var(–border);background:var(–white);font-size:12px;font-weight:600;cursor:pointer;transition:all .2s;color:var(–mid);}
.phase-tab.active{background:var(–charcoal);color:var(–white);border-color:var(–charcoal);}
.phase-tab:hover:not(.active){border-color:var(–gold);color:var(–gold);}

.seance-view{background:var(–white);border:1px solid var(–border);border-radius:var(–radius);overflow:hidden;box-shadow:var(–shadow);}
.seance-view-header{background:linear-gradient(135deg,var(–charcoal),#2d2d2d);color:var(–white);padding:22px 24px;}
.seance-view-title{font-family:‘Playfair Display’,serif;font-size:22px;font-weight:700;margin-bottom:4px;}
.seance-view-sub{font-size:13px;color:rgba(255,255,255,.55);}
.seance-view-badges{display:flex;gap:8px;margin-top:12px;flex-wrap:wrap;}
.sv-badge{padding:4px 12px;border-radius:20px;font-size:11px;font-weight:700;}
.sv-badge-push{background:#EBF2F8;color:var(–blue);}
.sv-badge-pull{background:#FBEAEA;color:var(–red);}
.sv-badge-legs{background:#EAF3EC;color:var(–green);}
.sv-badge-skills{background:#FDF3E7;color:var(–orange);}
.sv-badge-rest{background:var(–pearl);color:var(–mid);}
.sv-badge-core{background:#EAF3EC;color:var(–green);}

.seance-progress-bar{height:5px;background:rgba(255,255,255,.15);}
.seance-progress-fill{height:100%;background:var(–gold);transition:width .4s;}

.seance-section-label{padding:12px 20px;background:var(–cream);border-bottom:1px solid var(–border);display:flex;align-items:center;gap:8px;}
.seance-section-tag{padding:2px 10px;border-radius:10px;font-size:10px;font-weight:700;letter-spacing:.5px;}
.tag-cali{background:#EBF2F8;color:var(–blue);}
.tag-salle{background:#FDF3E7;color:var(–orange);}
.tag-skills{background:#FDF9EE;color:var(–gold);border:1px solid var(–gold-light);}
.tag-core{background:#EAF3EC;color:var(–green);}
.seance-section-name{font-size:12px;font-weight:700;color:var(–mid);}

.exo-row{display:flex;align-items:flex-start;gap:12px;padding:14px 20px;border-bottom:1px solid var(–border);transition:background .15s;cursor:pointer;}
.exo-row:hover{background:var(–cream);}
.exo-row.done-row{background:#EAF3EC;}
.exo-row-check{width:24px;height:24px;border-radius:50%;border:2px solid var(–border);display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:1px;transition:all .2s;font-size:12px;}
.exo-row.done-row .exo-row-check{background:var(–green);border-color:var(–green);color:white;}
.exo-row-info{flex:1;}
.exo-row-name{font-size:13px;font-weight:600;color:var(–charcoal);margin-bottom:2px;}
.exo-row-meta{font-size:11px;color:var(–mid);display:flex;gap:10px;flex-wrap:wrap;}
.exo-row-sets{font-family:‘DM Mono’,monospace;font-size:11px;color:var(–blue);font-weight:600;}
.exo-row-prog{font-size:11px;color:var(–gold);}
.exo-timer-btn{padding:5px 12px;background:var(–pearl);border:1px solid var(–border);border-radius:8px;font-size:11px;font-weight:600;cursor:pointer;color:var(–dark);font-family:‘DM Sans’,sans-serif;transition:all .2s;flex-shrink:0;}
.exo-timer-btn:hover{background:var(–gold-pale);border-color:var(–gold);}

/* Timer inline sticky */
.timer-sticky{position:sticky;bottom:0;background:var(–white);border-top:2px solid var(–gold);padding:14px 20px;display:flex;align-items:center;gap:14px;box-shadow:0 -4px 20px rgba(0,0,0,.1);z-index:50;}
.timer-sticky-display{font-family:‘DM Mono’,monospace;font-size:28px;font-weight:500;min-width:70px;}
.timer-sticky-display.ts-running{color:var(–green);}
.timer-sticky-display.ts-warning{color:var(–orange);}
.timer-sticky-display.ts-done{color:var(–gold);}
.timer-sticky-presets{display:flex;gap:6px;flex-wrap:wrap;}
.ts-preset{padding:5px 10px;border-radius:8px;border:1.5px solid var(–border);background:var(–cream);font-size:11px;font-weight:600;cursor:pointer;transition:all .2s;font-family:‘DM Sans’,sans-serif;}
.ts-preset:hover,.ts-preset.ts-active{background:var(–charcoal);color:var(–white);border-color:var(–charcoal);}
.timer-sticky-controls{display:flex;gap:6px;margin-left:auto;}
.ts-btn{padding:8px 16px;border:none;border-radius:8px;font-family:‘DM Sans’,sans-serif;font-size:12px;font-weight:600;cursor:pointer;transition:all .2s;}
.ts-btn-go{background:var(–green);color:var(–white);}
.ts-btn-pause{background:var(–orange);color:var(–white);}
.ts-btn-reset{background:var(–pearl);border:1px solid var(–border);color:var(–dark);}
.timer-sticky-progress{height:3px;background:var(–pearl);}
.timer-sticky-bar{height:100%;background:linear-gradient(90deg,var(–green),var(–gold-light));transition:width .5s linear;}
@media(max-width:600px){.timer-sticky{flex-wrap:wrap;gap:8px;}.timer-sticky-controls{margin-left:0;}}

.seance-empty{padding:40px;text-align:center;color:var(–mid);font-size:14px;}

/* Programme table */
.prog-table{width:100%;border-collapse:collapse;font-size:12.5px;}
.prog-table th{background:var(–charcoal);color:var(–white);padding:9px 12px;text-align:left;font-size:11px;font-weight:600;letter-spacing:.5px;}
.prog-table td{padding:9px 12px;border-bottom:1px solid var(–border);vertical-align:top;line-height:1.5;}
.prog-table tr:last-child td{border-bottom:none;}
.prog-table tr:nth-child(even) td{background:var(–cream);}
.prog-name-cell{font-weight:600;}
.prog-prog{font-size:10px;color:var(–gold);margin-top:2px;}
.phase-content{display:none;}
.phase-content.active{display:block;}
.skills-grid{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:12px;}
@media(max-width:600px){.skills-grid{grid-template-columns:1fr;}}
.skill-card{background:var(–cream);border:1px solid var(–border);border-radius:var(–radius-sm);padding:14px;}
.skill-target{font-size:11px;color:var(–gold);font-weight:600;margin-top:6px;padding:4px 8px;background:var(–gold-pale);border-radius:6px;display:inline-block;}

/* ════════════════════════════
EXERCICES
════════════════════════════ */
.exo-lib-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px;}
@media(max-width:700px){.exo-lib-grid{grid-template-columns:1fr;}}
.exo-lib-card{background:var(–white);border:1px solid var(–border);border-radius:var(–radius);padding:18px;cursor:pointer;transition:all .2s;box-shadow:var(–shadow);}
.exo-lib-card:hover{border-color:var(–gold);transform:translateY(-2px);box-shadow:var(–shadow-lg);}
.exo-lib-name{font-family:‘Playfair Display’,serif;font-size:14px;font-weight:700;margin-bottom:4px;}
.exo-lib-cat{font-size:11px;color:var(–gold);font-weight:600;letter-spacing:.5px;margin-bottom:8px;}
.exo-lib-desc{font-size:12px;color:var(–mid);line-height:1.5;}
.filter-pills{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:20px;}
.pill{padding:6px 14px;border-radius:20px;border:1.5px solid var(–border);background:var(–white);font-size:12px;font-weight:500;cursor:pointer;transition:all .2s;color:var(–mid);}
.pill.active{background:var(–charcoal);color:var(–white);border-color:var(–charcoal);}
.search-bar{width:100%;padding:12px 16px;border:1.5px solid var(–border);border-radius:var(–radius-sm);font-family:‘DM Sans’,sans-serif;font-size:14px;background:var(–white);color:var(–charcoal);margin-bottom:16px;outline:none;transition:border-color .2s;}
.search-bar:focus{border-color:var(–gold);}

/* ════════════════════════════
MODAL
════════════════════════════ */
.modal-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.5);z-index:200;align-items:center;justify-content:center;padding:20px;}
.modal-overlay.open{display:flex;}
.modal{background:var(–white);border-radius:var(–radius);padding:28px;max-width:560px;width:100%;max-height:85vh;overflow-y:auto;box-shadow:var(–shadow-lg);}
.modal-close{float:right;background:none;border:none;font-size:22px;cursor:pointer;color:var(–mid);}
.modal-title{font-family:‘Playfair Display’,serif;font-size:20px;font-weight:700;margin-bottom:4px;}
.modal-cat{font-size:12px;color:var(–gold);font-weight:600;letter-spacing:.5px;margin-bottom:16px;}
.modal-sec{font-weight:700;font-size:11px;letter-spacing:1px;text-transform:uppercase;color:var(–charcoal);margin:14px 0 6px;padding-bottom:4px;border-bottom:1px solid var(–border);}
.modal-list{list-style:none;}
.modal-list li{padding:5px 0;font-size:13px;display:flex;gap:8px;line-height:1.5;border-bottom:1px dashed var(–border);}
.modal-list li:last-child{border:none;}
.modal-list li::before{content:‘→’;color:var(–gold);flex-shrink:0;font-weight:700;}
.modal-tip{background:var(–gold-pale);border-left:3px solid var(–gold);padding:10px 14px;border-radius:0 var(–radius-sm) var(–radius-sm) 0;font-size:12px;margin-top:14px;line-height:1.5;}

/* ════════════════════════════
NUTRITION
════════════════════════════ */
.nutr-macro-row{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;margin-bottom:20px;}
@media(max-width:600px){.nutr-macro-row{grid-template-columns:repeat(2,1fr);}}
.macro-card{background:var(–white);border:1px solid var(–border);border-radius:var(–radius-sm);padding:16px;text-align:center;box-shadow:var(–shadow);}
.macro-val{font-family:‘Playfair Display’,serif;font-size:24px;font-weight:700;line-height:1;margin-bottom:4px;}
.macro-label{font-size:11px;color:var(–mid);}
.macro-kcal .macro-val{color:var(–gold);}
.macro-prot .macro-val{color:var(–blue);}
.macro-carb .macro-val{color:var(–green);}
.macro-fat .macro-val{color:var(–orange);}
.timing-row{display:flex;gap:12px;padding:10px 0;border-bottom:1px solid var(–border);font-size:13px;align-items:flex-start;}
.timing-row:last-child{border:none;}
.timing-time{font-family:‘DM Mono’,monospace;font-size:11px;color:var(–gold);font-weight:600;width:60px;flex-shrink:0;padding-top:1px;}
.timing-train{background:var(–gold-pale);border-left:3px solid var(–gold);padding:8px 12px;border-radius:0 6px 6px 0;font-weight:600;font-size:13px;}
.food-cat-title{font-family:‘Playfair Display’,serif;font-size:16px;font-weight:700;padding:12px 0 8px;display:flex;align-items:center;gap:8px;}
.food-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-bottom:20px;}
@media(max-width:600px){.food-grid{grid-template-columns:1fr 1fr;}}
.food-item{background:var(–white);border:1px solid var(–border);border-radius:var(–radius-sm);padding:12px;box-shadow:var(–shadow);}
.food-name{font-weight:600;font-size:12px;margin-bottom:3px;}
.food-macro{font-size:11px;color:var(–mid);}
.food-portion{font-size:10px;color:var(–light);margin-top:2px;font-family:‘DM Mono’,monospace;}

/* ════════════════════════════
PHOTOS
════════════════════════════ */
.upload-zone{border:2px dashed var(–border);border-radius:var(–radius);padding:32px;text-align:center;background:var(–white);cursor:pointer;transition:all .2s;margin-bottom:20px;}
.upload-zone:hover{border-color:var(–gold);background:var(–gold-pale);}
.upload-zone input{display:none;}
.photo-form{background:var(–white);border:1px solid var(–border);border-radius:var(–radius);padding:20px;margin-bottom:20px;display:none;}
.photo-form.visible{display:block;}
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-bottom:12px;}
@media(max-width:500px){.form-row{grid-template-columns:1fr;}}
label{font-size:12px;font-weight:600;color:var(–dark);display:block;margin-bottom:4px;}
input[type=“date”],input[type=“text”],input[type=“number”],select,textarea{width:100%;padding:10px 12px;border:1.5px solid var(–border);border-radius:var(–radius-sm);font-family:‘DM Sans’,sans-serif;font-size:13px;background:var(–white);color:var(–charcoal);outline:none;transition:border-color .2s;}
input:focus,select:focus,textarea:focus{border-color:var(–gold);}
textarea{resize:vertical;min-height:60px;}
.btn{padding:10px 22px;border-radius:var(–radius-sm);font-family:‘DM Sans’,sans-serif;font-size:13px;font-weight:600;cursor:pointer;border:none;transition:all .2s;}
.btn-gold{background:var(–gold);color:var(–white);}
.btn-gold:hover{background:var(–gold-light);}
.btn-outline{background:transparent;border:1.5px solid var(–border);color:var(–mid);}
.btn-outline:hover{border-color:var(–charcoal);color:var(–charcoal);}
.timeline-week{margin-bottom:28px;}
.timeline-week-title{font-family:‘Playfair Display’,serif;font-size:15px;font-weight:700;margin-bottom:10px;padding-bottom:8px;border-bottom:2px solid var(–border);}
.photos-row{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;}
@media(max-width:600px){.photos-row{grid-template-columns:1fr 1fr;}}
.photo-thumb{background:var(–pearl);border-radius:var(–radius-sm);overflow:hidden;border:1px solid var(–border);transition:transform .2s;position:relative;}
.photo-thumb:hover{transform:scale(1.02);}
.photo-thumb img{width:100%;height:120px;object-fit:cover;display:block;}
.photo-thumb-info{padding:8px 10px;}
.photo-thumb-date{font-size:10px;color:var(–mid);font-family:‘DM Mono’,monospace;}
.photo-thumb-type{font-size:11px;font-weight:600;}
.photo-delete{position:absolute;top:6px;right:6px;background:rgba(0,0,0,.6);color:white;border:none;border-radius:50%;width:24px;height:24px;font-size:11px;cursor:pointer;display:flex;align-items:center;justify-content:center;}
.avant-apres-grid{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
@media(max-width:500px){.avant-apres-grid{grid-template-columns:1fr;}}
.aa-slot{background:var(–cream);border:1.5px dashed var(–border);border-radius:var(–radius-sm);padding:12px;}
.aa-label{font-size:11px;font-weight:700;color:var(–mid);margin-bottom:8px;text-transform:uppercase;letter-spacing:.5px;}

/* ════════════════════════════
PROGRESSION
════════════════════════════ */
.prog-item{background:var(–white);border:1px solid var(–border);border-radius:var(–radius-sm);padding:14px 16px;margin-bottom:10px;box-shadow:var(–shadow);}
.prog-row{display:flex;align-items:center;gap:10px;margin-bottom:8px;flex-wrap:wrap;}
.prog-name{font-weight:600;font-size:14px;flex:1;min-width:150px;}
.prog-current{font-family:‘DM Mono’,monospace;font-size:15px;color:var(–gold);}
.prog-bar-wrap{background:var(–pearl);border-radius:10px;height:6px;overflow:hidden;}
.prog-bar{height:100%;border-radius:10px;background:linear-gradient(90deg,var(–gold),var(–gold-light));transition:width .5s;}
.record-edit-btn{padding:4px 10px;background:var(–cream);border:1.5px solid var(–border);border-radius:6px;font-size:11px;font-weight:600;cursor:pointer;color:var(–dark);font-family:‘DM Sans’,sans-serif;transition:all .2s;}
.record-edit-btn:hover{border-color:var(–gold);color:var(–gold);}
.record-save-btn{padding:4px 10px;background:var(–gold);border:none;border-radius:6px;font-size:11px;font-weight:600;cursor:pointer;color:var(–white);font-family:‘DM Sans’,sans-serif;}
.record-input-inline{width:65px;padding:4px 8px;border:1.5px solid var(–gold);border-radius:6px;font-family:‘DM Mono’,monospace;font-size:13px;color:var(–charcoal);outline:none;background:var(–gold-pale);}
.criteria-list{display:flex;flex-direction:column;gap:8px;}
.crit-item{display:flex;align-items:center;gap:10px;padding:10px 14px;background:var(–white);border:1px solid var(–border);border-radius:var(–radius-sm);font-size:13px;cursor:pointer;transition:all .2s;box-shadow:var(–shadow);}
.crit-item.done{background:#EAF3EC;border-color:#90C6A0;}

/* Mensuration table */
.mensuration-section{margin-bottom:24px;}
.mensuration-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;}
@media(max-width:600px){.mensuration-grid{grid-template-columns:1fr 1fr;}}
.mensuration-card{background:var(–white);border:1px solid var(–border);border-radius:var(–radius-sm);padding:14px;box-shadow:var(–shadow);}
.mensuration-label{font-size:11px;color:var(–mid);margin-bottom:6px;font-weight:600;text-transform:uppercase;letter-spacing:.5px;}
.mensuration-val{font-family:‘Playfair Display’,serif;font-size:22px;font-weight:700;color:var(–charcoal);margin-bottom:2px;}
.mensuration-diff{font-size:11px;font-weight:600;}
.mensuration-diff.pos{color:var(–green);}
.mensuration-diff.neg{color:var(–red);}
.mensuration-diff.zero{color:var(–mid);}

.phase-history{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-top:12px;}
@media(max-width:600px){.phase-history{grid-template-columns:1fr;}}
.phase-hist-card{background:var(–cream);border:1px solid var(–border);border-radius:var(–radius-sm);padding:14px;}
.phase-hist-title{font-size:11px;font-weight:700;letter-spacing:.5px;color:var(–mid);margin-bottom:10px;text-transform:uppercase;}

/* ── TOAST ── */
.toast{position:fixed;bottom:24px;right:24px;background:var(–charcoal);color:var(–white);padding:12px 20px;border-radius:var(–radius-sm);font-size:13px;font-weight:500;z-index:300;transform:translateY(100px);opacity:0;transition:all .3s;box-shadow:var(–shadow-lg);}
.toast.show{transform:translateY(0);opacity:1;}

/* ── UTILS ── */
.empty-state{text-align:center;padding:48px 24px;color:var(–mid);}
.empty-icon{font-size:48px;margin-bottom:12px;}
.deload-banner{background:linear-gradient(90deg,#C4622D,#E08050);color:var(–white);border-radius:var(–radius-sm);padding:12px 16px;margin-bottom:16px;font-size:13px;font-weight:600;display:flex;align-items:center;gap:10px;}
@keyframes fadeIn{from{opacity:0;transform:translateY(6px);}to{opacity:1;transform:translateY(0);}}
.tab.active>*{animation:fadeIn .25s ease;}
</style>

</head>
<body>

<!-- accès direct -->

<!-- FÉLICITATIONS -->

<div class="congrats-overlay" id="congrats-overlay">
  <div class="congrats-box">
    <div class="congrats-emoji">🏆</div>
    <div class="congrats-title">Séance terminée !</div>
    <div class="congrats-sub" id="congrats-msg"></div>
    <button class="congrats-btn" onclick="document.getElementById('congrats-overlay').classList.remove('show')">Fermer</button>
  </div>
</div>

<header>
  <div class="header-inner">
    <div class="logo">CALI<span>ÉLITE</span></div>
    <div class="header-meta" id="header-date"></div>
  </div>
</header>
<nav>
  <div class="nav-inner">
    <button class="nav-btn active" onclick="switchTab('accueil')" data-tab="accueil">🏠 Accueil</button>
    <button class="nav-btn" onclick="switchTab('programme')" data-tab="programme">📋 Programme</button>
    <button class="nav-btn" onclick="switchTab('exercices')" data-tab="exercices">💪 Exercices</button>
    <button class="nav-btn" onclick="switchTab('nutrition')" data-tab="nutrition">🥗 Nutrition</button>
    <button class="nav-btn" onclick="switchTab('photos')" data-tab="photos">📸 Photos</button>
    <button class="nav-btn" onclick="switchTab('progression')" data-tab="progression">📈 Progression</button>
  </div>
</nav>

<main>

<!-- ══════════════════════════════ ACCUEIL ══════════════════════════════ -->

<div class="tab active" id="tab-accueil">
  <div class="home-hero" id="home-hero">
    <div class="home-hero-bg"></div>
    <div class="home-hero-accent"></div>
    <div class="home-hero-content">
      <div class="home-hero-greeting" id="home-greeting"></div>
      <div class="home-hero-msg" id="home-msg">Chargement...</div>
      <div class="home-hero-submsg" id="home-submsg"></div>
      <div class="home-hero-badges" id="home-badges"></div>
    </div>
  </div>

  <div class="home-stats" id="home-stats"></div>

  <div class="home-shortcuts">
    <div class="shortcut-btn" onclick="goToProgramme()">
      <div class="shortcut-icon">📋</div>
      <div class="shortcut-label">Séance du jour</div>
      <div class="shortcut-sub" id="shortcut-seance-sub">Voir le programme</div>
    </div>
    <div class="shortcut-btn" onclick="switchTab('progression')">
      <div class="shortcut-icon">📈</div>
      <div class="shortcut-label">Ma progression</div>
      <div class="shortcut-sub">Records & objectifs</div>
    </div>
    <div class="shortcut-btn" onclick="switchTab('photos')">
      <div class="shortcut-icon">📸</div>
      <div class="shortcut-label">Mes photos</div>
      <div class="shortcut-sub" id="shortcut-photos-sub">Évolution visuelle</div>
    </div>
  </div>

  <div class="home-bottom">
    <div class="tip-daily-card">
      <div class="tip-daily-label" id="tip-daily-cat">💡 CONSEIL DU JOUR</div>
      <div class="tip-daily-text" id="tip-daily-text"></div>
      <div class="tip-daily-src" id="tip-daily-src"></div>
      <div class="tip-daily-nav">
        <button onclick="prevTip()">← Préc.</button>
        <button onclick="nextTip()">Suiv. →</button>
        <button onclick="randomTip()">🎲</button>
      </div>
    </div>
    <div class="upcoming-card">
      <div class="card-title">📅 Prochaines séances</div>
      <div id="upcoming-list"></div>
    </div>
  </div>
</div>

<!-- ══════════════════════════════ PROGRAMME ══════════════════════════════ -->

<div class="tab" id="tab-programme">
  <div class="page-title">Programme</div>
  <div class="page-sub">Clique sur un jour pour voir la séance · séance d'aujourd'hui ouverte par défaut</div>

  <div id="deload-banner-wrap"></div>

  <!-- Sélecteur de phase -->

  <div class="phase-selector" id="phase-selector">
    <button class="phase-tab active" onclick="switchPhase('p1',this)">⚡ Phase 1 — Fondations (S1–S8)</button>
    <button class="phase-tab" onclick="switchPhase('p2',this)">🔥 Phase 2 — Construction (S9–S24)</button>
    <button class="phase-tab" onclick="switchPhase('p3',this)">💎 Phase 3 — Élite (S25–S52)</button>
  </div>

  <!-- Barre des jours de la semaine -->

  <div class="week-day-bar" id="week-day-bar"></div>

  <!-- Vue séance -->

  <div id="seance-view-wrap"></div>

  <!-- Contenu programme complet par phase (sous la séance) -->

  <div style="margin-top:28px;">
    <div class="phase-content active" id="pc-p1"></div>
    <div class="phase-content" id="pc-p2"></div>
    <div class="phase-content" id="pc-p3"></div>
  </div>
</div>

<!-- ══════════════════════════════ EXERCICES ══════════════════════════════ -->

<div class="tab" id="tab-exercices">
  <div class="page-title">Bibliothèque des exercices</div>
  <div class="page-sub">45+ exercices · description complète · position de départ · points clés · progression</div>
  <input class="search-bar" type="text" placeholder="🔍  Rechercher..." id="exo-search" oninput="filterExos()">
  <div class="filter-pills" id="filter-pills"></div>
  <div class="exo-lib-grid" id="exo-lib-grid"></div>
</div>

<!-- ══════════════════════════════ NUTRITION ══════════════════════════════ -->

<div class="tab" id="tab-nutrition">
  <div class="page-title">Nutrition Élite</div>
  <div class="page-sub">Macros · timing adapté à ton planning · 30+ aliments · suppléments</div>

  <div style="display:flex;gap:8px;flex-wrap:wrap;margin-bottom:16px;">
    <div class="filter-pills" style="margin-bottom:0;">
      <button class="pill active" onclick="setNutrMode('surplus',this)">Phases 1–2 (Surplus +300 kcal)</button>
      <button class="pill" onclick="setNutrMode('cut',this)">Phase 3 tardive (Révélation)</button>
    </div>
  </div>
  <div style="display:flex;gap:8px;flex-wrap:wrap;margin-bottom:20px;">
    <div class="filter-pills" style="margin-bottom:0;">
      <button class="pill active" onclick="setHoraire('A',this)">🕘 Horaire 8h45–16h45</button>
      <button class="pill" onclick="setHoraire('B',this)">🕙 Horaire 11h30–19h30</button>
    </div>
  </div>

  <div class="nutr-macro-row" id="nutr-macros"></div>
  <div class="grid-2" style="margin-bottom:24px;">
    <div class="card"><div class="card-title">⏰ Timing nutritionnel</div><div id="timing-list"></div></div>
    <div class="card"><div class="card-title">💧 Hydratation & Suppléments</div><div id="supps-list" style="font-size:13px;line-height:1.9;color:var(--mid);"></div></div>
  </div>
  <div id="food-cats"></div>
</div>

<!-- ══════════════════════════════ PHOTOS ══════════════════════════════ -->

<div class="tab" id="tab-photos">
  <div class="page-title">Photos d'évolution</div>
  <div class="page-sub">Upload · galerie chronologique · comparaison avant/après</div>

  <div style="margin-bottom:14px;">
    <button class="btn btn-gold" onclick="toggleAA()" style="margin-right:8px;">⚖️ Vue Avant / Après</button>
  </div>
  <div id="aa-section" style="display:none;margin-bottom:24px;">
    <div class="card">
      <div class="card-title">⚖️ Comparaison Avant / Après</div>
      <div class="avant-apres-grid">
        <div class="aa-slot"><div class="aa-label">📅 Avant</div><select id="aa-before" onchange="renderAA()" style="margin-bottom:8px;width:100%;padding:8px;border:1px solid var(--border);border-radius:6px;font-family:'DM Sans',sans-serif;font-size:12px;"></select><div id="aa-before-img"></div></div>
        <div class="aa-slot"><div class="aa-label">🏆 Après</div><select id="aa-after" onchange="renderAA()" style="margin-bottom:8px;width:100%;padding:8px;border:1px solid var(--border);border-radius:6px;font-family:'DM Sans',sans-serif;font-size:12px;"></select><div id="aa-after-img"></div></div>
      </div>
    </div>
  </div>

  <div class="upload-zone" onclick="document.getElementById('photo-input').click()">
    <input type="file" id="photo-input" accept="image/*" multiple onchange="handlePhotoUpload(event)">
    <div style="font-size:36px;margin-bottom:8px;">📸</div>
    <div style="font-size:15px;font-weight:600;">Ajouter des photos</div>
    <div style="font-size:12px;color:var(--mid);margin-top:4px;">Cliquez ou glissez vos photos ici</div>
  </div>

  <div class="photo-form" id="photo-form">
    <div class="card-title">📝 Informations</div>
    <div id="photo-preview-zone" style="margin-bottom:12px;"></div>
    <div class="form-row">
      <div><label>Date</label><input type="date" id="photo-date"></div>
      <div><label>Semaine</label><select id="photo-semaine"></select></div>
    </div>
    <div class="form-row">
      <div><label>Type</label><select id="photo-type"><option>Face avant</option><option>Profil gauche</option><option>Profil droit</option><option>Dos</option><option>Pose double biceps</option><option>Full body</option></select></div>
      <div><label>Poids (kg)</label><input type="number" id="photo-poids" step="0.1" placeholder="75.5"></div>
    </div>
    <div style="margin-bottom:12px;"><label>Note</label><textarea id="photo-note" placeholder="Observations..."></textarea></div>
    <div style="display:flex;gap:8px;">
      <button class="btn btn-gold" onclick="savePhoto()">💾 Sauvegarder</button>
      <button class="btn btn-outline" onclick="cancelPhoto()">Annuler</button>
    </div>
  </div>

  <div id="photo-gallery"></div>
</div>

<!-- ══════════════════════════════ PROGRESSION ══════════════════════════════ -->

<div class="tab" id="tab-progression">
  <div class="page-title">Progression & Records</div>
  <div class="page-sub">Records · mensurations corporelles · critères de passage · export/import données</div>

  <!-- Export / Import données -->

  <div class="card" style="margin-bottom:20px;background:var(--cream);">
    <div class="card-title">💾 Sauvegarde des données</div>
    <p style="font-size:13px;color:var(--mid);margin-bottom:14px;">Tes données sont sauvegardées dans ce navigateur sur cet appareil. Pour ne jamais les perdre (changement de navigateur, vidage de cache, autre appareil), exporte-les en JSON et réimporte-les à tout moment.</p>
    <div style="display:flex;gap:10px;flex-wrap:wrap;">
      <button class="btn btn-gold" onclick="exportData()">⬇️ Exporter mes données (.json)</button>
      <label class="btn btn-outline" style="cursor:pointer;">📂 Importer des données <input type="file" accept=".json" onchange="importData(event)" style="display:none;"></label>
    </div>
    <div id="import-status" style="font-size:12px;color:var(--green);margin-top:8px;display:none;"></div>
  </div>

  <!-- Paramètres -->

  <div class="card" style="margin-bottom:20px;">
    <div class="card-title">⚙️ Paramètres du programme</div>
    <div class="grid-2">
      <div>
        <label>Date de début</label>
        <input type="date" id="start-date-input" style="margin-top:4px;">
      </div>
      <div>
        <label>Prénom</label>
        <input type="text" id="prenom-input" style="margin-top:4px;" placeholder="Ton prénom">
      </div>
    </div>
    <button class="btn btn-gold" style="margin-top:12px;" onclick="updateParams()">Mettre à jour</button>
    <button class="btn btn-outline" style="margin-top:12px;margin-left:8px;" onclick="changePinPrompt()">🔑 Changer le PIN</button>
  </div>

  <!-- Mensurations corporelles -->

  <div class="card" style="margin-bottom:24px;">
    <div class="card-title">📏 Mensurations corporelles</div>
    <p style="font-size:12px;color:var(--mid);margin-bottom:16px;">Saisis tes mensurations actuelles. Chaque saisie est horodatée et organisée par phase pour suivre l'évolution.</p>
    <div id="mensuration-form-grid" style="display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-bottom:16px;">
    </div>
    <div style="display:flex;gap:8px;align-items:center;flex-wrap:wrap;margin-bottom:16px;">
      <select id="mensuration-phase" style="padding:8px 12px;border:1.5px solid var(--border);border-radius:8px;font-family:'DM Sans',sans-serif;font-size:13px;outline:none;">
        <option value="debut">Début de programme</option>
        <option value="p1-fin">Fin Phase 1 (S8)</option>
        <option value="p2-fin">Fin Phase 2 (S24)</option>
        <option value="p3-fin">Fin Phase 3 (S52)</option>
        <option value="actuel">Actuel</option>
      </select>
      <button class="btn btn-gold" onclick="saveMensurations()">💾 Enregistrer</button>
    </div>
    <div id="mensuration-history"></div>
  </div>

  <!-- Records -->

  <div style="margin-bottom:24px;">
    <div style="font-family:'Playfair Display',serif;font-size:17px;font-weight:700;margin-bottom:14px;">🏆 Records vs Objectifs 12 mois</div>
    <div id="records-list"></div>
  </div>

  <!-- Critères -->

  <div style="margin-bottom:20px;">
    <div style="font-family:'Playfair Display',serif;font-size:17px;font-weight:700;margin-bottom:14px;">✅ Critères Phase 1 → Phase 2</div>
    <div class="criteria-list" id="criteria-p1"></div>
  </div>
  <div style="margin-bottom:20px;">
    <div style="font-family:'Playfair Display',serif;font-size:17px;font-weight:700;margin-bottom:14px;">✅ Critères Phase 2 → Phase 3</div>
    <div class="criteria-list" id="criteria-p2"></div>
  </div>
</div>

</main>

<div class="modal-overlay" id="modal-overlay" onclick="closeModal(event)">
  <div class="modal" id="modal-content"></div>
</div>
<div class="toast" id="toast"></div>

<script>
// ═══════════════════════════════════════════════════
// DATA — PROGRAMME
// ═══════════════════════════════════════════════════
const JOURS_SEMAINE = ['Lun','Mar','Mer','Jeu','Ven','Sam','Dim'];
const BADGE_COLORS = {push:'#2A5F8A',pull:'#8A2A2A',legs:'#2A6B3A',skills:'#C4622D',rest:'#999',core:'#2A6B3A'};
const BADGE_CSS = {push:'sv-badge-push',pull:'sv-badge-pull',legs:'sv-badge-legs',skills:'sv-badge-skills',rest:'sv-badge-rest',core:'sv-badge-core'};

const PROGRAMME = {
  p1:{label:"Phase 1 — Fondations",semaines:"S1–S8",
    split:"4 séances/semaine — Upper/Lower alterné",
    objectif:"Réactiver le système neuromusculaire, technique irréprochable, renforcer tendons & ligaments.",
    jours:[
      {num:1,titre:"UPPER A",sous:"Push + Pull léger + Salle",badge:"push",sections:[
        {label:"CALISTHÉNIE (60%)",tag:"cali",exos:[
          {nom:"Pompes standard",sets:"4 × 8–10",quand:"4×12 parfaites → déclinées",note:"Coudes 45°, corps rigide, full ROM",prog:"→ Pompes déclinées"},
          {nom:"Dips assistés (pied sol)",sets:"3 × 8–10",quand:"3×12 sans aide → libres",note:"Lean avant, descente 90°",prog:"→ Dips libres"},
          {nom:"Pike push-up basique",sets:"3 × 6–8",quand:"3×10 → pieds surélevés",note:"Hanches hautes, tête entre les bras",prog:"→ Pieds surélevés"},
          {nom:"Hollow body hold",sets:"3 × 20 sec",quand:"3×30s → rock",note:"Dos plaqué sol, jambes tendues",prog:"→ Hollow rock"},
        ]},
        {label:"SALLE BASIC FIT (40%)",tag:"salle",exos:[
          {nom:"Développé couché haltères",sets:"3 × 10–12",quand:"+2kg à 3×12",note:"12–14 kg · descente 2–3 sec",prog:""},
          {nom:"Élévations latérales haltères",sets:"3 × 12–15",quand:"+2kg à 3×15",note:"6–8 kg · hauteur épaules",prog:""},
          {nom:"Triceps câble poulie haute",sets:"3 × 12–15",quand:"+2.5kg à 3×15",note:"Coudes collés, extension complète",prog:""},
        ]},
      ]},
      {num:2,titre:"LOWER + CORE",sous:"Jambes + Gainage + Mobilité",badge:"legs",sections:[
        {label:"SALLE (Lower)",tag:"salle",exos:[
          {nom:"Squat barre guidée ou haltères",sets:"4 × 10–12",quand:"+5kg à 3×12",note:"Barre seule ou 15kg · cuisses parallèles",prog:""},
          {nom:"Fentes marchées haltères",sets:"3 × 10 chaque",quand:"+2kg à 3×10",note:"8–10 kg · genou effleure sol",prog:""},
          {nom:"Romanian deadlift haltères",sets:"3 × 10–12",quand:"+2kg à 3×12",note:"16–18 kg · dos droit, hanches arrière",prog:""},
          {nom:"Leg curl machine",sets:"3 × 12",quand:"+5kg à 3×12",note:"Ischio-jambiers — essentiel repreneurs",prog:""},
          {nom:"Mollets debout (step)",sets:"4 × 15–20",quand:"+charge à 4×20",note:"Full ROM, pause en bas",prog:""},
        ]},
        {label:"CORE CALISTHÉNIE",tag:"core",exos:[
          {nom:"Planche avant (plank)",sets:"4 × 20–30 sec",quand:"3×30s → 4×45s",note:"Fessiers contractés, bassin neutre",prog:"→ RKC plank"},
          {nom:"Crunch bicycle lent",sets:"3 × 12 chaque",quand:"3×20",note:"Rotation vraie du torse",prog:""},
          {nom:"Leg raises au sol",sets:"3 × 10–12",quand:"3×15 → jambes tendues",note:"Dos plaqué, jambes ne touchent pas",prog:""},
          {nom:"Superman hold",sets:"3 × 10 × 2sec",quand:"+résistance",note:"Dos postérieur — souvent négligé",prog:""},
        ]},
      ]},
      {num:3,titre:"REPOS ACTIF",sous:"Marche 30 min + mobilité 15 min",badge:"rest",sections:[
        {label:"RÉCUPÉRATION ACTIVE",tag:"core",exos:[
          {nom:"Marche ou vélo léger",sets:"30 min",quand:"—",note:"FC <130 bpm",prog:""},
          {nom:"Mobilité (wrists, épaules, hanches)",sets:"15 min",quand:"—",note:"Wrist circles, thread needle, pigeon",prog:""},
        ]},
      ]},
      {num:4,titre:"UPPER B",sous:"Pull dominante + Push léger + Salle",badge:"pull",sections:[
        {label:"CALISTHÉNIE (60%)",tag:"cali",exos:[
          {nom:"Dead hang actif",sets:"3 × 30 sec",quand:"→ scapular 3×10",note:"Omoplates vers le bas, pas de balance",prog:"→ Scapular pull-ups"},
          {nom:"Traction assistée (élastique)",sets:"5 × max (3–5)",quand:"5×5 → réduire assistance",note:"Supination · bras TENDUS en bas",prog:"→ Traction libre"},
          {nom:"Inverted rows (barre basse)",sets:"4 × 8–12",quand:"Corps horizontal = max P1",note:"Coudes vers les hanches",prog:"→ Plus horizontal"},
          {nom:"Face pulls élastique",sets:"3 × 15",quand:"3×15 → +résistance",note:"Pouces vers oreilles · santé épaules",prog:""},
        ]},
        {label:"SALLE BASIC FIT (40%)",tag:"salle",exos:[
          {nom:"Tirage vertical (lat pulldown)",sets:"4 × 10–12",quand:"+5kg à 3×12",note:"30–35 kg · prise large, tire vers menton",prog:""},
          {nom:"Tirage horizontal câble",sets:"3 × 10–12",quand:"+5kg à 3×12",note:"30 kg · dos droit, coudes corps",prog:""},
          {nom:"Curl biceps haltères",sets:"3 × 10–12",quand:"+2kg à 3×12",note:"10–12 kg · supination complète, 3 sec",prog:""},
          {nom:"Curl marteau",sets:"2 × 12",quand:"—",note:"10 kg · brachial + avant-bras",prog:""},
        ]},
      ]},
      {num:5,titre:"LOWER + CORE + MOBILITÉ",sous:"Jambes + Core + Étirements 12 min",badge:"legs",sections:[
        {label:"SALLE + CORE CALI",tag:"salle",exos:[
          {nom:"Goblet squat haltères",sets:"4 × 12",quand:"+charge",note:"14–18 kg · descente profonde",prog:""},
          {nom:"Step-ups haltères sur banc",sets:"3 × 10 chaque",quand:"+2kg",note:"8–10 kg · genou aligné",prog:""},
          {nom:"Hip thrust barre",sets:"4 × 15",quand:"+charge",note:"Fessiers = stabilité bassin",prog:""},
          {nom:"Good morning barre légère",sets:"3 × 12",quand:"+charge",note:"10–20 kg · dos droit, érecteurs",prog:""},
          {nom:"Pallof press (élastique)",sets:"3 × 12 chaque",quand:"+résistance",note:"Anti-rotation = gainage fonctionnel",prog:""},
          {nom:"Ab wheel rollout (genoux)",sets:"3 × 6–10",quand:"3×10 → depuis pieds",note:"Ne creuse pas le bas du dos",prog:"→ Depuis pieds"},
          {nom:"Side plank",sets:"3 × 20–30 sec",quand:"45 sec chaque",note:"Corps droit, pas de rotation",prog:"→ 45s → 1 min"},
        ]},
      ]},
    ],
    skills:[
      {nom:"Planche",exo:"Lean avant progressif sol, bras tendus",vol:"5 × 10–15 sec",cible:"Tuck sol 15–20 sec"},
      {nom:"L-sit",exo:"Tuck L-sit entre chaises/parallèles",vol:"5 × 5–10 sec",cible:"Tuck L-sit 10 sec"},
      {nom:"Handstand",exo:"Kick-up contre mur",vol:"5 × 15–20 sec",cible:"Handstand mur 20 sec"},
      {nom:"Muscle-up prep",exo:"Dead hang + scapular pull-ups",vol:"Intégré Pull",cible:"3–5 tractions libres"},
    ],
    criteres:["3×12 pompes parfaites full ROM","5 tractions libres supination sans balancement","3×10 dips libres descente 90°","3×12 inverted rows à 45°","Planche sol 30 sec","Tuck L-sit 10 sec","Handstand mur 20 sec","Squat profond 3×12 sans douleur"]
  },
  p2:{label:"Phase 2 — Construction",semaines:"S9–S24",
    split:"4–5 séances/semaine — Push / Pull / Legs + Skills",
    objectif:"Transformation visible. Volume et intensité augmentés. Tractions vraies, dips profonds, premiers skills réels.",
    jours:[
      {num:1,titre:"PUSH",sous:"Pectoraux + Épaules + Triceps",badge:"push",sections:[
        {label:"CALISTHÉNIE (60%)",tag:"cali",exos:[
          {nom:"Pompes déclinées (banc 30–45 cm)",sets:"4 × 10–15",quand:"4×15 → +hauteur ou lest",note:"Descente 3 sec, explosion en montée",prog:"→ Pieds +haut + lest"},
          {nom:"Pompes diamant",sets:"3 × 8–12",quand:"3×12 → archer",note:"Coudes serrés contre le corps",prog:"→ Pompes archer"},
          {nom:"Pike push-up pieds surélevés",sets:"4 × 8–10",quand:"4×10 → contre mur",note:"Hanches très hautes",prog:"→ HSPU mur"},
          {nom:"Dips parallèles libres (profonds)",sets:"4 × 8–12",quand:"4×12 → +5 kg",note:"Descente 90°+, lean avant",prog:"→ Dips lestés"},
          {nom:"Pseudo planche push-up",sets:"3 × 5–8",quand:"→ mains aux hanches",note:"Protraction max, corps horizontal",prog:"→ Lean progressif"},
        ]},
        {label:"SALLE (40%)",tag:"salle",exos:[
          {nom:"Développé couché haltères",sets:"4 × 8–10",quand:"+2kg à 3×10",note:"18–24 kg · descente 3 sec",prog:""},
          {nom:"Développé incliné haltères",sets:"3 × 10–12",quand:"+2kg à 3×12",note:"14–18 kg · 30° inclinaison",prog:""},
          {nom:"Élévations latérales câbles",sets:"3 × 12–15",quand:"+2kg à 3×15",note:"8–12 kg · tension constante",prog:""},
          {nom:"Overhead press haltères",sets:"3 × 10–12",quand:"+2kg",note:"12–16 kg · poussée stricte",prog:""},
        ]},
      ]},
      {num:2,titre:"PULL",sous:"Dos + Biceps + Arrière Épaule",badge:"pull",sections:[
        {label:"CALISTHÉNIE (60%)",tag:"cali",exos:[
          {nom:"Tractions supination (chin-ups)",sets:"5 × max (obj. 5–8)",quand:"5×8 → prise pronation",note:"FULL ROM bras tendus. Pas de balancement.",prog:"→ Pronation ou lest"},
          {nom:"Tractions pronation (pull-ups)",sets:"4 × max (3–6)",quand:"4×8 → lest",note:"Introduit S12–14. Omoplates vers hanches.",prog:"→ Lest ou archer"},
          {nom:"Inverted rows horizontaux",sets:"4 × 10–15",quand:"4×15 → pieds 30 cm",note:"Corps parallèle au sol = niveau max",prog:"→ Pieds surélevés"},
          {nom:"Face pulls élastique",sets:"3 × 15–20",quand:"+résistance",note:"Santé épaules — ne jamais supprimer",prog:""},
          {nom:"Skin the cat (intro S14)",sets:"3 × 3–5",quand:"→ 3×8",note:"Genoux fléchis. Shoulder prep obligatoire.",prog:"→ Rotation complète"},
        ]},
        {label:"SALLE (40%)",tag:"salle",exos:[
          {nom:"Tirage vertical supination serré",sets:"4 × 8–10",quand:"+5kg",note:"45–55 kg · même pattern que chin-up",prog:""},
          {nom:"Tirage horizontal rowing câble",sets:"4 × 10–12",quand:"+5kg",note:"50–60 kg · dos droit",prog:""},
          {nom:"Shrugs haltères",sets:"3 × 15",quand:"+2kg",note:"24–28 kg · trapèzes supérieurs",prog:""},
          {nom:"Curl barre EZ",sets:"4 × 8–10",quand:"+2.5kg",note:"30–35 kg total · excentrique 3 sec",prog:""},
          {nom:"Curl incliné haltères",sets:"3 × 10–12",quand:"+2kg",note:"10–12 kg · étirement biceps maximal",prog:""},
        ]},
      ]},
      {num:3,titre:"LEGS + CORE",sous:"Jambes lourdes + Gainage avancé",badge:"legs",sections:[
        {label:"SALLE (60%)",tag:"salle",exos:[
          {nom:"Squat barre libre",sets:"4 × 8–10",quand:"+2.5kg/sem",note:"50–70 kg · progression linéaire",prog:""},
          {nom:"Leg press",sets:"3 × 10–12",quand:"+10kg à 3×12",note:"80–120 kg · pied haut pour fessiers",prog:""},
          {nom:"Romanian deadlift barre",sets:"4 × 8–10",quand:"+5kg",note:"50–65 kg · dos droit",prog:""},
          {nom:"Leg curl couché",sets:"3 × 12",quand:"+5kg",note:"Antagoniste quadriceps",prog:""},
          {nom:"Hip thrust barre",sets:"4 × 12–15",quand:"+5–10kg",note:"40–60 kg · fessiers + lombaire",prog:""},
        ]},
        {label:"CORE CALISTHÉNIE (40%)",tag:"core",exos:[
          {nom:"L-sit tuck parallèles",sets:"5 × max (obj. 10–15s)",quand:"→ L-sit complet",note:"Bras tendus, omoplates déprimées",prog:"→ Jambes tendues"},
          {nom:"Dragon flag négatif",sets:"4 × 3–5 lents",quand:"4×5 → concentriques",note:"Descente 4–5 sec. Gainage total.",prog:"→ Concentrique"},
          {nom:"Ab wheel (depuis genoux)",sets:"4 × 8–12",quand:"4×12 → depuis pieds",note:"Expiration en rentrant, dos plat",prog:"→ Depuis pieds"},
          {nom:"Hanging knee raises",sets:"4 × 12–15",quand:"4×15 → toes to bar",note:"Contrôle le balancement",prog:"→ Toes to bar"},
          {nom:"Crunch inversé (reverse crunch)",sets:"3 × 15",quand:"3×20 → lest",note:"Bas du dos plaqué, hanches se soulèvent",prog:"→ Avec lest"},
        ]},
      ]},
      {num:4,titre:"REPOS ACTIF",sous:"Mobilité + Skills légers",badge:"rest",sections:[
        {label:"RÉCUPÉRATION",tag:"core",exos:[
          {nom:"Mobilité épaules + hanches",sets:"20 min",quand:"—",note:"Thread needle, world's greatest stretch",prog:""},
          {nom:"Skills légers (50% intensité)",sets:"10 min",quand:"—",note:"Handstand hold ou L-sit seulement",prog:""},
        ]},
      ]},
      {num:5,titre:"PUSH + SKILLS",sous:"Push hypertrophie + Planche/HSPU",badge:"skills",sections:[
        {label:"SKILLS PRIORITY (25 min)",tag:"skills",exos:[
          {nom:"Planche tuck → frog stand",sets:"6 × 15–20 sec",quand:"Frog stand 20s = objectif",note:"Lean avant progressif, bras tendus",prog:"→ Tuck barre"},
          {nom:"Handstand contre mur + sorties",sets:"5 × 20–30 sec",quand:"30 sec sans aide mur",note:"Oreilles entre les bras",prog:"→ 30s stable"},
          {nom:"High pull explosif + bar dip",sets:"5 × 3–5 + 5 × 5",quand:"Barre jusqu'au nombril",note:"Prépare la transition muscle-up",prog:"→ Muscle-up"},
        ]},
        {label:"PUSH VARIANTE",tag:"cali",exos:[
          {nom:"Pompes archer",sets:"4 × 6–8 chaque",quand:"4×8 → 1 bras",note:"Un bras large, l'autre plie",prog:"→ Pompe 1 bras"},
          {nom:"HSPU négatif mur (5 sec)",sets:"4 × 3–5",quand:"4×5 → positifs",note:"Tête touche sol, corps droit",prog:"→ HSPU positif"},
          {nom:"Cable flyes ou pec deck",sets:"3 × 15",quand:"+charge",note:"Finisseur pectoraux",prog:""},
        ]},
      ]},
      {num:6,titre:"PULL + SKILLS",sous:"Pull volume + Front lever / L-sit",badge:"skills",sections:[
        {label:"SKILLS PRIORITY (20 min)",tag:"skills",exos:[
          {nom:"Front lever tuck",sets:"6 × 10–15 sec",quand:"→ advanced tuck",note:"Corps horizontal, bras tendus",prog:"→ Advanced tuck"},
          {nom:"L-sit jambes tendues",sets:"5 × max",quand:"→ V-sit angle",note:"Compression hanches maximale",prog:"→ V-sit"},
          {nom:"Skin the cat (rotation complète)",sets:"4 × 3–5",quand:"Fluide et contrôlé",note:"Épaules mobiles",prog:"→ 3×8"},
        ]},
        {label:"PULL VARIANTE",tag:"cali",exos:[
          {nom:"Tractions lestées (+5 kg)",sets:"5 × 5–6",quand:"+5kg à 5×6",note:"Si 3×8 libres → ajouter lest",prog:""},
          {nom:"Archer pull-ups",sets:"4 × 4–6 chaque",quand:"4×6 → 1-arm négatif",note:"Un bras tendu, l'autre tire",prog:"→ 1-arm négatif"},
          {nom:"Tirage unilatéral haltère",sets:"4 × 10–12 chaque",quand:"+5kg",note:"24–30 kg · coude vers plafond",prog:""},
          {nom:"Curl barre EZ lourd",sets:"3 × 8",quand:"+2.5kg",note:"35–40 kg total · force biceps",prog:""},
        ]},
      ]},
    ],
    skills:[
      {nom:"Planche",exo:"Tuck sol → frog stand → tuck barre",vol:"6 × 15–20 sec",cible:"Frog stand 20s + tuck barre 10s"},
      {nom:"Handstand",exo:"Contre mur + sorties progressives",vol:"5 × 20–30 sec",cible:"Handstand mur 30 sec"},
      {nom:"Muscle-up (prép)",exo:"High pull explosif + bar dip",vol:"5 × 3–5",cible:"Barre au nombril"},
      {nom:"Front Lever",exo:"Tuck FL horizontal bras tendus",vol:"6 × 10–15 sec",cible:"Tuck FL bras tendus"},
      {nom:"L-sit → V-sit",exo:"L-sit jambes tendues parallèles",vol:"5 × max",cible:"L-sit 20s → V-sit 5s"},
    ],
    criteres:["10 tractions strictes pronation full ROM","15 dips profonds descente 90°+","20 pompes déclinées parfaites","Handstand mur 30 sec stable","Frog stand 20s / Tuck barre 10s","L-sit jambes tendues 10s","Squat barre 1×5 = 80% poids corps","Physique visible : dos en V, abdos apparents"]
  },
  p3:{label:"Phase 3 — Élite",semaines:"S25–S52",
    split:"5 séances/semaine — Push Heavy / Pull Heavy / Legs / Skills Day / Volume",
    objectif:"Transformation complète. Hypertrophie maximale. Muscle-up, planche avancée, HSPU, front lever straddle.",
    jours:[
      {num:1,titre:"PUSH HEAVY",sous:"Force + Hypertrophie pec/épaules/triceps",badge:"push",sections:[
        {label:"CALISTHÉNIE FORCE (60%)",tag:"cali",exos:[
          {nom:"Pompes lestées (+10–20 kg)",sets:"5 × 5–8",quand:"+5kg à 5×8",note:"Sac à dos ou ceinture lestée",prog:"→ Pompe 1 bras"},
          {nom:"HSPU mur complet",sets:"5 × 5–8",quand:"+1 rep à 5×8",note:"Tête touche sol, extension complète",prog:"→ Freestanding S40+"},
          {nom:"Dips lestés (+10–20 kg)",sets:"5 × 6–8",quand:"+5kg à 5×8",note:"Descente lente 3 sec",prog:"→ Dips anneaux fin P3"},
          {nom:"Pseudo planche push-up (lean avancé)",sets:"4 × 5–8",quand:"→ planche push-up",note:"Mains niveau hanches, horizontal",prog:"→ Planche push-up"},
        ]},
        {label:"SALLE (40%)",tag:"salle",exos:[
          {nom:"Développé couché barre",sets:"4 × 5–6 (force)",quand:"+2.5kg à 4×6",note:"70–90 kg · force pure",prog:""},
          {nom:"Développé incliné haltères",sets:"4 × 8–10",quand:"+2kg",note:"24–30 kg · haut pec",prog:""},
          {nom:"Overhead press barre",sets:"3 × 6–8",quand:"+2.5kg",note:"40–55 kg · épaules force",prog:""},
        ]},
      ]},
      {num:2,titre:"PULL HEAVY",sous:"Force + Hypertrophie dos/biceps",badge:"pull",sections:[
        {label:"CALISTHÉNIE FORCE (60%)",tag:"cali",exos:[
          {nom:"Tractions lestées (+10–15 kg)",sets:"5 × 4–6",quand:"+5kg à 5×6",note:"Force maximale dos",prog:""},
          {nom:"Muscle-up (S25: prép / S33: strict)",sets:"5 × max",quand:"5 reps → explosif",note:"L'exercice roi. Pull + transition + dip",prog:"→ Explosif"},
          {nom:"Front lever tuck → straddle",sets:"5 × 10–15 sec",quand:"15s → level suivant",note:"Corps horizontal, bras tendus",prog:"→ Straddle S40+"},
          {nom:"Archer pull-up / 1-arm négatif",sets:"4 × 3–5 chaque",quand:"→ négatif complet",note:"Vers traction 1 bras",prog:"→ 1-arm complet"},
        ]},
        {label:"SALLE (40%)",tag:"salle",exos:[
          {nom:"Rowing barre penché",sets:"4 × 6–8",quand:"+5kg",note:"60–80 kg · barre touche poitrine",prog:""},
          {nom:"Pull-over haltère",sets:"3 × 10–12",quand:"+2kg",note:"28–35 kg · grand dorsal + dentelé",prog:""},
          {nom:"Curl barre EZ lourd",sets:"4 × 6–8 (force)",quand:"+2.5kg",note:"40–50 kg total",prog:""},
          {nom:"Tirage nuque prise large",sets:"3 × 10",quand:"+5kg",note:"50–60 kg · largeur dos",prog:""},
        ]},
      ]},
      {num:3,titre:"LEGS + CORE AVANCÉ",sous:"Legs lourds + Dragon flag + Core",badge:"legs",sections:[
        {label:"LEGS SALLE (60%)",tag:"salle",exos:[
          {nom:"Squat barre (back squat)",sets:"5 × 5 (force)",quand:"+2.5kg",note:"80–100 kg · progression linéaire",prog:""},
          {nom:"Bulgarian split squat haltères",sets:"4 × 8–10 chaque",quand:"+2kg",note:"24–28 kg · hypertrophie + équilibre",prog:""},
          {nom:"Romanian deadlift barre",sets:"4 × 8",quand:"+5kg",note:"80–95 kg · chaîne postérieure",prog:""},
          {nom:"Nordic hamstring curl",sets:"3 × 5–8 négatifs",quand:"→ concentriques",note:"Poids du corps · prévention blessures",prog:""},
          {nom:"Hip thrust barre",sets:"4 × 10–12",quand:"+5–10kg",note:"80–100 kg · ALL skills",prog:""},
        ]},
        {label:"CORE AVANCÉ (40%)",tag:"core",exos:[
          {nom:"Dragon flag",sets:"4 × 5–8",quand:"+1 rep",note:"Concentrique + excentrique",prog:"→ Full ROM"},
          {nom:"L-sit → V-sit progression",sets:"5 × max",quand:"→ V-sit +",note:"Compression maximale hanches",prog:""},
          {nom:"Hanging toes to bar",sets:"4 × 10–15",quand:"+2 reps",note:"Jambes tendues, touche barre",prog:""},
          {nom:"Ab wheel depuis pieds",sets:"4 × 10",quand:"+2 reps",note:"Extension complète, dos plat",prog:""},
          {nom:"Windshield wipers (barre)",sets:"3 × 10 chaque",quand:"→ jambes tendues",note:"Obliques + fléchisseurs profonds",prog:"→ Jambes tendues"},
        ]},
      ]},
      {num:4,titre:"⭐ SKILLS DAY",sous:"LA séance la plus importante du programme",badge:"skills",sections:[
        {label:"6 BLOCS SKILLS — repos 2–3 min",tag:"skills",exos:[
          {nom:"PLANCHE : Tuck → Adv. tuck → Straddle",sets:"6 × 15–25 sec",quand:"+2s/sem sur niveau actuel",note:"S36: 20s adv tuck | S44: straddle",prog:"→ Full planche S52"},
          {nom:"MUSCLE-UP : propres → explosifs",sets:"5 × max",quand:"+1 rep/2 sem",note:"S33: 1 rep | S40: 5 reps",prog:"→ 5 explosifs S48"},
          {nom:"HANDSTAND : mur → freestanding",sets:"8 × 15–30 sec",quand:"+5s/mois",note:"S40: 5s free | S52: 15s free",prog:"→ Freestanding"},
          {nom:"FRONT LEVER : tuck → straddle",sets:"5 × 10–20 sec",quand:"+2s/sem",note:"S36: adv tuck | S48: straddle",prog:"→ Straddle"},
          {nom:"BACK LEVER (intro S32)",sets:"4 × 10–15 sec",quand:"+2s/sem",note:"Skin the cat obligatoire avant",prog:"→ Straddle S40"},
          {nom:"HSPU : mur → déficit → freestanding",sets:"5 × 3–8",quand:"+1 rep",note:"S40: déficit 10cm | S52: 1–3 free",prog:"→ Freestanding"},
        ]},
      ]},
      {num:5,titre:"PUSH VOLUME",sous:"Hypertrophie + Explosivité",badge:"push",sections:[
        {label:"PUSH VOLUME (cali + salle)",tag:"cali",exos:[
          {nom:"Pompes explosives (clap)",sets:"4 × 8–10",quand:"+2 reps",note:"Puissance pectoraux",prog:""},
          {nom:"Ring push-ups (si anneaux)",sets:"4 × 10–12",quand:"+2 reps",note:"Activation maximale stabilisateurs",prog:""},
          {nom:"Dips anneaux ou lestés",sets:"4 × 8–10",quand:"+2 reps ou +2.5kg",note:"Anneaux si disponibles",prog:""},
          {nom:"Cable flyes haut → bas",sets:"4 × 15",quand:"+charge",note:"Étirement pectoral complet",prog:""},
          {nom:"Élévations latérales haltères",sets:"4 × 15",quand:"+2kg",note:"14–18 kg · finisseur épaules",prog:""},
        ]},
      ]},
      {num:6,titre:"PULL VOLUME",sous:"Volume + Définition + Isolation",badge:"pull",sections:[
        {label:"PULL VOLUME",tag:"cali",exos:[
          {nom:"Tractions pronation volume",sets:"5 × max",quand:"Obj S52: 5×15–20",note:"Volume pur. Repos 90s.",prog:""},
          {nom:"Rowing haltère unilatéral lourd",sets:"4 × 8–10 chaque",quand:"+5kg",note:"35–45 kg · épaisseur dos",prog:""},
          {nom:"Face pulls câble",sets:"4 × 20",quand:"+charge",note:"Santé épaules P3 — NE PAS SUPPRIMER",prog:""},
          {nom:"Curl concentré",sets:"3 × 12",quand:"+2kg",note:"Pic biceps, définition",prog:""},
          {nom:"Curl reverse (pronation)",sets:"3 × 12",quand:"+2kg",note:"Avant-bras + brachioradial",prog:""},
        ]},
      ]},
    ],
    skills:[
      {nom:"Planche",exo:"Tuck → Adv. tuck → Straddle → Full",vol:"6 × 15–25 sec",cible:"S52: Straddle 15s / Full 5s"},
      {nom:"Muscle-up",exo:"1 → 5 propres → 5 explosifs",vol:"5 × max",cible:"S52: 5 explosifs"},
      {nom:"Handstand",exo:"Mur 30s → sorties → freestanding",vol:"8 × 15–30 sec",cible:"S52: Freestanding 10–15s"},
      {nom:"Front Lever",exo:"Tuck → Adv. tuck → Straddle",vol:"5 × 10–20 sec",cible:"S52: Straddle 10s"},
      {nom:"Back Lever",exo:"Tuck → Straddle (intro S32)",vol:"4 × 10–15 sec",cible:"S52: Straddle back lever"},
      {nom:"HSPU",exo:"Mur strict → déficit → freestanding",vol:"5 × 3–8",cible:"S52: Freestanding 1–3 reps"},
    ],
    criteres:[]
  }
};

// ─── EXERCICES DB (45+) ───
const EXERCICES_DB = [
  // ABDOS
  {nom:"Planche avant (plank)",cat:"Abdos",type:"cali",depart:"En appui avant-bras et orteils, corps en ligne droite tête-talons.",exec:["Contracte abdos, fessiers, quadriceps simultanément","Pousse coudes vers pieds (tension active)","Tête neutre, regard vers le sol","Respire normalement"],cles:["Bassin parfaitement aligné — ni trop haut ni trop bas","Le bas du dos NE doit PAS s'affaisser","RKC plank = coudes vers pieds + serrer les fesses fort = 40% tension en plus"],prog:"Genoux → Standard → RKC plank → Dragon flag",tip:"Le RKC plank (pousser coudes vers pieds, serrer fesses fort) active 40% de tension en plus."},
  {nom:"Hollow body hold",cat:"Abdos",type:"cali",depart:"Allongé dos, bras tendus au-dessus de la tête, jambes tendues à 45°.",exec:["Presse le bas du dos contre le sol — règle absolue","Contracte abdos comme pour rentrer le nombril","Jambes et bras aussi bas que possible","Maintiens en respirant normalement"],cles:["Si dos décolle = monte les jambes","Base de toute la calisthénie (planche, muscle-up)","Genoux pliés pour débuter"],prog:"Genoux pliés → 60° → 45° → 30° → Hollow rock",tip:"Maîtriser le hollow body = maîtriser la moitié de la calisthénie. Fondation absolue."},
  {nom:"Crunch bicycle lent",cat:"Abdos",type:"cali",depart:"Allongé dos, mains derrière nuque, genoux à 90°.",exec:["Coude droit vers genou gauche en ROTATION du torse","Jambe gauche s'allonge simultanément","Retour centre, répète autre côté","Mouvement lent — 2 sec par rep"],cles:["Rotation du torse, PAS du cou","Ne tire pas sur la tête","Lent = efficace. Rapide = triche."],prog:"Genoux → Jambe étendue → Avec lest",tip:"Exercice abdo le plus complet selon EMG : grands droits + obliques + transverse."},
  {nom:"Leg raises au sol",cat:"Abdos",type:"cali",depart:"Allongé dos, bras le long corps ou sous les fesses, jambes tendues.",exec:["Inspire, presse dos au sol","Soulève jambes tendues à 90°","Descend LENTEMENT sans poser","Expire à la descente"],cles:["Bas du dos RESTE au sol toute la durée","Si jambes pas tendues → plie légèrement","Descente = phase difficile, ne la bâcle pas"],prog:"Genoux pliés → Tendues sol → Hanging knee raises → Toes to bar",tip:"La descente lente est 3× plus efficace que la montée. Concentre-toi sur l'excentrique."},
  {nom:"Dragon flag",cat:"Abdos",type:"cali",depart:"Allongé sur banc, mains agrippent les montants derrière la tête.",exec:["Soulève hanches pour amener corps vertical","Descend lentement (5 sec) corps RIGIDE","Ne laisse JAMAIS les hanches fléchir","Monte ou négatifs seulement au début"],cles:["Corps = planche rigide — aucune flexion à la hanche","Commence par négatifs seuls 4–6 semaines","Signature de Bruce Lee"],prog:"Négatifs tuck → Négatifs tendus → Concentrique + excentrique",tip:"Ne passe au concentrique que quand le négatif complet est maîtrisé (4×5 lents). 3–6 mois min."},
  {nom:"L-sit (parallèles)",cat:"Abdos / Skills",type:"cali",depart:"Sur barres parallèles, bras tendus, épaules déprimées, jambes tendues.",exec:["Déprime épaules fort (loin des oreilles)","Contracte abdos ET fléchisseurs hanches","Jambes complètement tendues parallèles sol","Maintiens en respirant"],cles:["Combine force abdominale + compression hanches","Fléchisseurs souvent la limite, pas les abdos","Douleur à l'aine = normal au début"],prog:"Tuck L-sit → 1 jambe tendue → L-sit complet → V-sit",tip:"Fais des étirements fléchisseurs de hanche quotidiens. C'est la limite de 90% des pratiquants."},
  {nom:"Ab wheel rollout",cat:"Abdos",type:"cali",depart:"À genoux, mains sur roue ab wheel, bras tendus.",exec:["Roule en gardant dos DROIT","Va aussi loin que possible sans baisser hanches","Contracte abdos pour revenir","Ne laisse pas hanches toucher sol"],cles:["Exercice abdo le plus difficile","Erreur = dos qui s'arque en avant","Expire vers l'avant, inspire en revenant"],prog:"Genoux court → Genoux complet → Pieds debout → Pieds avec pause",tip:"4×10 depuis les pieds = abdos dans le top 1%. Objectif Phase 3."},
  {nom:"Hanging knee raises",cat:"Abdos",type:"cali",depart:"Suspendu barre en dead hang actif, épaules déprimées.",exec:["Contracte abdos, ramène genoux vers poitrine","Pause 1 sec en haut","Descend LENTEMENT — pas de balancement","Corps aussi immobile que possible"],cles:["Contrôle du balancement = progression neurologique","Ne se balance pas pour aller plus haut","Expir en montant, inspir en descendant"],prog:"Knee raises → Jambes 45° → Jambes 90° → Toes to bar → Windshield wipers",tip:"En suspension tu renforces aussi grip et avant-bras. Double bénéfice."},
  {nom:"Side plank",cat:"Abdos",type:"cali",depart:"Appui sur un avant-bras, corps de côté. Pieds empilés.",exec:["Soulève hanches — corps en ligne droite","Contracte obliques et fessiers","Maintiens sans laisser hanches tomber","Respire normalement"],cles:["Hanches ne tombent pas vers le sol","Ne compense pas avec le bas du dos","Progression : genou → pieds empilés → avec rotation"],prog:"Genoux → Pieds empilés → Rotation bras → Avec poids",tip:"Prévient douleurs lombaires et renforce obliques — la ceinture naturelle du corps."},
  {nom:"Windshield wipers (barre)",cat:"Abdos",type:"cali",depart:"Suspendu barre, jambes à 90° (L-position). Prise pronation.",exec:["Maintiens jambes à 90°, tourne bassin vers droite","Pieds vers la main droite","Retour centre puis vers gauche","Lent et contrôlé"],cles:["Exercice Phase 3 avancé","Bras ne s'écartent pas — grip serré","Commence jambes pliées avant tendues"],prog:"Jambes pliées → Tendues 45° → Tendues 90° → Full ROM",tip:"Combine avec hanging leg raises pour programme core complet en suspension."},
  // PECTORAUX / PUSH
  {nom:"Pompes standard",cat:"Pectoraux",type:"cali",depart:"Position planche, mains largeur épaules, coudes à 45°.",exec:["Inspire en descendant lentement 2–3 sec","Poitrine effleure presque le sol","Expire en poussant explosif","Corps rigide de tête aux pieds"],cles:["Coudes à 45° — jamais à 90°","Corps = planche rigide","Full ROM : poitrine au sol, bras tendus"],prog:"Inclinées → Standard → Déclinées → Diamant → Archer → 1 bras",tip:"Si les hanches ne restent pas droites, fais les genoux au sol. Technique prime sur reps."},
  {nom:"Pompes déclinées",cat:"Pectoraux",type:"cali",depart:"Pieds sur banc (30–60 cm), mains au sol. Corps incliné tête vers bas.",exec:["Descente lente 3 sec","Poitrine touche presque sol","Pousse explosif","Corps rigide"],cles:["Plus pieds sont hauts, plus haut pectoraux + épaules travaillent","Prépare directement le handstand push-up"],prog:"Pieds bas → Banc normal → Très haut → HSPU",tip:"Idéal pour haut pectoraux et préparer le handstand push-up."},
  {nom:"Pompes diamant",cat:"Triceps",type:"cali",depart:"Mains jointives sous sternum, triangle. Bras serrés.",exec:["Descente coudes parallèles au corps","Poitrine descend entre les mains","Pousse en contractant triceps","Extension complète"],cles:["Coudes pointent vers l'arrière","Poids légèrement en avant sur phalanges","Isole les triceps sans matériel"],prog:"Standard → Diamant → Pike → HSPU",tip:"Indispensable pour progresser vers le muscle-up."},
  {nom:"Pike push-up",cat:"Épaules",type:"cali",depart:"V inversé (hanches hautes, triangle). Mains largeur épaules.",exec:["Plie coudes en amenant tête entre mains","Tête effleure le sol","Pousse pour revenir","Hanches restent hautes"],cles:["Plus hanches hautes = plus difficile","Tête passe entre les bras — pas devant","Progression directe vers HSPU"],prog:"Pieds sol → Pieds surélevés → HSPU mur → HSPU freestanding",tip:"Maîtrise pike push-up pieds sur banc = mi-chemin du handstand push-up."},
  {nom:"Dips parallèles (profonds)",cat:"Pectoraux / Triceps",type:"cali",depart:"Sur barres parallèles, bras tendus, épaules déprimées.",exec:["Descend jusqu'à 90° MINIMUM","Extension complète en haut","Lean avant = pec / Droit = triceps"],cles:["Descente insuffisante = exercice inefficace","Omoplates déprimées en haut","90%+ des douleurs d'épaule débutants = descente trop rapide"],prog:"Assistés → Libres → Lestés → Anneaux",tip:"Les dips profonds : descends progressivement sur 4–6 semaines pour habituer les épaules."},
  {nom:"Pompes archer",cat:"Pectoraux",type:"cali",depart:"Position pompe, un bras très écarté tendu, l'autre sous l'épaule.",exec:["Le bras écarté reste tendu","Descends sur le bras qui plie","Pousse pour revenir","Alterne les côtés"],cles:["C'est la progression vers pompe 1 bras","Le bras tendu aide l'équilibre mais ne pousse pas","Rapproche progressivement le bras tendu"],prog:"Pompes déclinées → Archer → Pompes 1 bras",tip:"Chaque côté = exercice indépendant. Révèle exactement l'asymétrie gauche/droite."},
  {nom:"HSPU contre mur",cat:"Épaules / Skills",type:"cali",depart:"Handstand contre mur, mains à 15–20 cm du mur, doigts écartés.",exec:["Plie coudes en amenant tête vers sol","Tête effleure le sol","Pousse pour revenir en extension complète","Corps droit tout au long"],cles:["Coudes à 45° — pas perpendiculaires","Corps aligné (pas de banana back)","Commence par les négatifs (5 sec)"],prog:"Pike push-up → HSPU négatif → HSPU complet → Déficit → Freestanding",tip:"3 mois de négatifs quotidiens avant de faire un HSPU complet. La patience paie."},
  {nom:"Pseudo planche push-up",cat:"Pectoraux / Planche",type:"cali",depart:"Position pompe, mains en avant des épaules (niveau bassin), protraction max.",exec:["Lean encore vers l'avant","Pompe complète avec ce placement de mains","Corps reste le plus horizontal possible"],cles:["Exercice roi pour apprendre la planche","Le lean progressif = principe fondamental","Douleurs poignets = normal, travaille wrist exercises"],prog:"Lean léger → Mains au bassin → Planche push-up complet",tip:"Commence avec juste le lean statique avant de faire des pompes."},
  // DOS / TRACTIONS
  {nom:"Dead hang actif",cat:"Dos / Santé épaules",type:"cali",depart:"Suspendu barre, bras complètement tendus.",exec:["Engage omoplates vers le bas","Corps légèrement creux (hollow)","Maintiens la tension","Ne te balance pas"],cles:["Actif = épaules ne remontent pas","30–60 sec par hold = objectif P1","Fondamental santé épaules et coudes"],prog:"Passif → Actif → Scapular pull-ups → Tractions",tip:"Dead hang quotidien décompresse la colonne vertébrale et renforce le grip."},
  {nom:"Scapular pull-ups",cat:"Dos / Préhabilitation",type:"cali",depart:"Suspendu barre, bras COMPLÈTEMENT tendus. Jamais plier.",exec:["Abaisse omoplates (vers poches arrière)","Corps monte légèrement 5–10 cm","Remonte épaules","Répète sans jamais plier coudes"],cles:["Exercice le plus important avant les tractions","Active trapèzes inférieurs + grand dentelé","Protège épaules à long terme"],prog:"Dead hang → Scapular → Tractions assistées → Tractions libres",tip:"3×10 par jour pendant 2 semaines = base solide pour les vraies tractions."},
  {nom:"Tractions supination (chin-ups)",cat:"Dos / Biceps",type:"cali",depart:"Suspendu barre, prise supination largeur épaules, bras tendus.",exec:["Dépression scapulaire pour amorcer","Tire coudes vers les hanches","Monte menton au-dessus barre","Descends COMPLÈTEMENT bras tendus"],cles:["Full ROM obligatoire","Pas de balancement","Biceps + dos en synergie"],prog:"Assistées → 1 rep → 5 reps → 10 reps → Lestées",tip:"5 reps propres = milestone majeur Phase 1."},
  {nom:"Tractions pronation (pull-ups)",cat:"Dos",type:"cali",depart:"Suspendu barre, prise pronation légèrement plus large que épaules.",exec:["Dépression scapulaire pour amorcer","Tire coudes vers hanches et arrière","Monte menton ou poitrine à la barre","Descend complètement"],cles:["Plus difficile que chin-up","Omoplates se rapprochent au sommet","Prise large = plus dos / serrée = plus biceps"],prog:"Chin-up 5 reps → Pull-up 1 → 5 → 10 → Lestées",tip:"10 chin-ups = probablement 3–5 pull-ups. Commence par là."},
  {nom:"Inverted rows",cat:"Dos / Arrière épaule",type:"cali",depart:"Allongé sous barre basse, mains pronation plus larges que épaules.",exec:["Tire coudes vers hanches","Poitrine touche la barre","Descend complètement","Corps rigide"],cles:["Plus horizontal = plus difficile","Omoplates rejoignent au sommet","Parfait avant les vraies tractions"],prog:"45° → Plus horizontal → Pieds surélevés → Chest to bar",tip:"4×12 inverted rows construisent rapidement la base dorsale."},
  {nom:"Tractions lestées",cat:"Dos / Force",type:"cali",depart:"Ceinture lestée ou sac à dos. Même position que pull-ups.",exec:["Technique identique aux tractions normales","Contrôle la descente — ne chute pas","Plein ROM obligatoire"],cles:["Seulement si 10 reps propres maîtrisées","Commence par +5 kg","Excentrique lent = progrès neuraux"],prog:"Pull-ups 10 reps → +5 kg 5 reps → +10 kg → +20 kg",tip:"Force traction lestée = clé du muscle-up."},
  {nom:"Archer pull-ups",cat:"Dos / Force",type:"cali",depart:"Suspendu barre, une main normale, l'autre bras tendu sur le côté.",exec:["Tire avec le bras normal","Bras tendu aide l'équilibre mais ne tire pas","Alterne les côtés"],cles:["Progression directe vers 1-arm pull-up","Révèle déséquilibres gauche/droite"],prog:"Pull-up × 10 → Archer → 1-arm négatif → 1-arm complet",tip:"L'un des exercices les plus honnêtes sur les déséquilibres."},
  {nom:"Muscle-up (barre)",cat:"Skills / Avancé",type:"cali",depart:"Suspendu barre, prise pronation légèrement plus large.",exec:["PULL : pull explosif barre au nombril","TRANSITION : hanches vers la barre, torse passe au-dessus","DIP : pousse en extension complète","Descend avec contrôle"],cles:["= high pull-up + bar dip combinés","Transition = partie la plus difficile","Kip excessif = pas un muscle-up propre"],prog:"High pull (nombril) → Transition assist. → Complet → Strict",tip:"90% échouent sur la transition, pas sur le pull ou le dip."},
  {nom:"Front lever tuck",cat:"Skills / Avancé",type:"cali",depart:"Suspendu barre, bras tendus, genoux contre poitrine.",exec:["Tire épaules vers bas et arrière","Corps monte jusqu'à horizontal","Genoux contre poitrine","Maintiens"],cles:["Corps HORIZONTAL — pas en diagonale","Bras complètement tendus","Force vient du dos pas des bras"],prog:"Dead hang → Tuck FL → Advanced tuck → Straddle → Full",tip:"Progression non-linéaire. Normal — la densité tendineuse s'adapte aussi."},
  {nom:"Skin the cat",cat:"Mobilité / Épaules",type:"cali",depart:"Suspendu barre, prise pronation, dead hang actif.",exec:["Amène genoux vers poitrine","Continue la rotation pour passer jambes derrière la barre","Corps se retrouve dos en bas (German hang)","Retour dans l'autre sens"],cles:["Shoulder prep OBLIGATOIRE avant","Commence genoux pliés","Mobilité d'épaule maximale requise — base back lever"],prog:"Rotation partielle → Complète genoux → Complète tendus",tip:"Si tu peux faire skin the cat 5× propres, tes épaules sont prêtes pour le back lever."},
  // SALLE
  {nom:"Développé couché haltères",cat:"Pectoraux / Salle",type:"salle",depart:"Allongé banc plat, haltères niveau épaules, coudes à 75°.",exec:["Descente contrôlée 2–3 sec","Haltères descendent jusqu'à hauteur épaules (full ROM)","Pousse en trajectoire légèrement courbe","Extension complète sans verrouiller"],cles:["Coudes à 75° = optimal biomécanique","Haltères > barre pour ROM + stabilisation","Contrôle l'excentrique"],prog:"12–14 kg → 16 → 18–20 → 22–24 kg",tip:"Rotation naturelle des poignets avec haltères = plus bas possible."},
  {nom:"Développé incliné haltères",cat:"Pectoraux / Salle",type:"salle",depart:"Banc incliné 30–45°, haltères au niveau des épaules.",exec:["Même technique que couché","Cible le haut des pectoraux","Plus d'implication des épaules"],cles:["Inclinaison 30° = optimal haut pec","Ne pas dépasser 45° (trop d'épaules)"],prog:"14–16 kg → 18–20 → 22–26 kg",tip:"Le haut des pectoraux = la partie qui donne le 'shelf' au torse."},
  {nom:"Overhead press haltères / barre",cat:"Épaules / Salle",type:"salle",depart:"Debout ou assis, haltères ou barre au niveau des oreilles, coudes à 90°.",exec:["Pousse vers le haut en ligne droite","Extension complète sans verrouiller","Descend contrôlé aux oreilles","Dos droit, abdos contractés"],cles:["Pas d'hyperextension lombaire","Extension complète = activation totale","Moins de charge = meilleure technique"],prog:"12–16 kg → 18–20 → 22–28 kg haltères",tip:"L'overhead press est l'indicateur de force épaules. Si tu stagnes, ajoute du travail mobilité."},
  {nom:"Squat barre",cat:"Jambes / Salle",type:"salle",depart:"Barre sur haut trapèze. Pieds largeur épaules, légèrement tournés.",exec:["Inspire profond, bracing abdominal","Descend en poussant genoux vers l'extérieur","Cuisses parallèles minimum","Remonte dos droit"],cles:["Genoux suivent direction des pieds","Respire en bas, expire en montant","Chute en avant = mobilité cheville limitée"],prog:"Barre seule → 40 kg → 60 → 80 → 100 kg",tip:"1 séance de squat lourd par semaine change tout."},
  {nom:"Romanian deadlift",cat:"Ischio-jambiers / Salle",type:"salle",depart:"Debout, barre ou haltères devant cuisses, prise pronation.",exec:["Pousse hanches vers l'arrière (charnière)","Barre descend le long des jambes","Dos DROIT tout au long","Descends jusqu'à étirement ischio"],cles:["Charnière des hanches, PAS un squat","Dos droit = non-négociable","Barre reste proche du corps"],prog:"Halt. 16 kg → Barre 40 → 60 → 80–95 kg",tip:"Meilleur exercice pour prévenir blessures ischio-jambiers (essentiel ex-footballeur)."},
  {nom:"Leg press",cat:"Jambes / Salle",type:"salle",depart:"Assis machine leg press, pieds sur plateforme à largeur épaules.",exec:["Descend jusqu'à 90° minimum","Pousse en extension complète","Contrôle la descente","Ne verrouille pas les genoux en haut"],cles:["Pied haut sur plateforme = plus de fessiers","Pied bas = plus de quadriceps","Ne jamais laisser genoux s'effondrer"],prog:"80 kg → 100 → 120 → 150–200 kg",tip:"Utilise la leg press pour volume supplémentaire après le squat, pas en remplacement."},
  {nom:"Bulgarian split squat haltères",cat:"Jambes / Salle",type:"salle",depart:"Pied arrière sur banc, pied avant 60–70 cm devant. Haltères dans les mains.",exec:["Descend le genou arrière vers le sol","Cuisse avant parallèle au sol","Pousse sur le talon avant","Corps reste droit"],cles:["Genou avant ne dépasse pas le bout des orteils","Excellent pour détecter déséquilibres jambes","Plus difficile que le squat standard"],prog:"Poids corps → 8 kg → 14 → 20–28 kg haltères",tip:"Le Bulgarian split squat construit la force fonctionnelle et prévient les déséquilibres."},
  {nom:"Hip thrust barre",cat:"Fessiers / Salle",type:"salle",depart:"Dos appuyé banc, barre sur hanches (avec pad), pieds à plat.",exec:["Pousse hanches vers le ciel","Contracte fessiers au maximum","Genou aligné, pause 1 sec en haut","Descend jusqu'à presque toucher sol"],cles:["Fessiers = base stabilité TOUS les skills","Contracte vraiment au sommet","Ne creuse pas le bas du dos"],prog:"Poids corps → 20 → 60 → 80–100 kg",tip:"Fessiers les plus puissants = tous tes skills progressent. Ne sous-estime pas cet exercice."},
  {nom:"Nordic hamstring curl",cat:"Ischio-jambiers / Salle",type:"salle",depart:"Genoux au sol, pieds bloqués sous un banc ou par un partenaire.",exec:["Descend lentement (excentrique) en contrôlant","Corps droit de genoux aux épaules","Aussi loin que possible avant de tomber","Remonte en aidant avec les mains (ou purement excentrique)"],cles:["Exercice de prévention blessures ischio-jambiers n°1","Commence par négatifs seulement","Douleur = normal les 2 premières semaines"],prog:"Négatifs partiels → Négatifs complets → Concentriques partiels → Complet",tip:"Réduit les risques de claquage ischio-jambiers de 50%. Obligatoire pour tout ex-footballeur."},
  {nom:"Rowing barre penché",cat:"Dos / Salle",type:"salle",depart:"Debout penché à 45°, barre en prise pronation, bras tendus.",exec:["Tire les coudes vers le haut","Barre touche le bas de la poitrine","Contracte le dos au sommet","Descend en contrôlant"],cles:["Dos plat — pas d'arrondi","Tête dans le prolongement du dos","Coudes vers le haut, pas vers les côtés"],prog:"40 kg → 50 → 60 → 70–80 kg",tip:"Rowing lourd = dos épais. C'est lui qui donne l'impression de volume au dos."},
  {nom:"Tirage nuque prise large",cat:"Dos / Salle",type:"salle",depart:"Machine lat pulldown, prise très large en pronation.",exec:["Tire vers la nuque ou derrière la tête","Coudes pointent vers le sol","Retour contrôlé","Protraction des omoplates en haut"],cles:["Largeur dos maximale","Attention aux cervicales — ne tire pas trop derrière","Peut aussi se faire devant (plus sécurisé)"],prog:"30 kg → 40 → 50 → 60–70 kg",tip:"Complément parfait aux tractions pour cibler les fibres supérieures du grand dorsal."},
  {nom:"Curl barre EZ",cat:"Biceps / Salle",type:"salle",depart:"Debout, barre EZ, bras tendus, coudes collés aux côtés.",exec:["Flexion stricte coudes uniquement","Supination complète au sommet","Descente contrôlée 3 sec","Extension complète en bas"],cles:["Corps ne se balance pas","Full ROM indispensable","Coudes restent fixes"],prog:"30 kg → 35 → 40 → 45–50 kg total",tip:"Force biceps directement corrélée à performance en tractions."},
  {nom:"Shrugs haltères",cat:"Trapèzes / Salle",type:"salle",depart:"Debout, haltères dans les mains, bras tendus le long du corps.",exec:["Monte les épaules vers les oreilles","Pause 1 sec en haut","Descend contrôlé","Pas de rotation"],cles:["Mouvement vertical uniquement — pas de rotation","Trapèzes supérieurs = épaisseur visuelle du dos"],prog:"20 kg → 24 → 28 → 32 kg haltères",tip:"Trapèzes développés donnent le look 'athlète' que peu obtiennent avec seulement des tractions."},
  {nom:"Face pulls câble",cat:"Arrière épaule / Santé",type:"salle",depart:"Poulie haute avec corde, coudes à hauteur épaules.",exec:["Tire la corde vers le visage en l'écartant","Pouces vers les oreilles en fin","Pause 1 sec","Retour contrôlé"],cles:["Prévention TOUTES blessures d'épaule","Ne jamais sauter même en fin de programme","Rotation externe = santé à long terme"],prog:"Léger → Moyen — priorité technique",tip:"3× par semaine les face pulls transforment la santé des épaules sur le long terme."},
  {nom:"Pull-over haltère",cat:"Dos / Salle",type:"salle",depart:"Allongé transversalement sur banc, haltère tenu à deux mains au-dessus de la poitrine.",exec:["Descend haltère derrière la tête en arc","Étirement du grand dorsal et dentelé","Remonte en arc vers poitrine","Bras légèrement fléchis"],cles:["Grand dorsal + dentelé antérieur","Excellent pour la largeur du dos","Ne descend pas trop bas si épaules sensibles"],prog:"18 kg → 22 → 26 → 30–35 kg",tip:"Pull-over = un des rares exercices qui travaille grand dorsal ET dentelé simultanément."},
  {nom:"Overhead press barre",cat:"Épaules / Salle",type:"salle",depart:"Debout, barre en avant des épaules niveau clavicules, prise légèrement plus large.",exec:["Pousse barre verticalement en passant devant le visage","Extension complète bras tendus","Descend contrôlé","Gainage abdominal permanent"],cles:["Corps droit — pas d'hyperextension lombaire","Barre passe devant le visage (pas derrière)","Force épaule brute"],prog:"Barre seule → 30 → 40 → 50–60 kg",tip:"Overhead press barre strict = indicateur de force totale du haut du corps."},
  {nom:"Planche tuck sol",cat:"Skills / Planche",type:"cali",depart:"À genoux, mains au sol légèrement en avant de la ligne des hanches.",exec:["Lean vers l'avant, poids sur les mains","Genoux près des coudes","Protraction MAXIMALE des omoplates (dos arrondi vers le ciel)","Soulève les pieds"],cles:["Protraction scapulaire CRUCIALE","Hanches à hauteur des épaules ou plus haut","Douleurs poignets = normal, travaille wrist exercises"],prog:"Lean statique → Tuck sol 5s → Tuck barre → Adv. tuck → Straddle → Full",tip:"La planche prend 6–18 mois. C'est normal et c'est physiologique."},

  // ─── BRAS — BICEPS ───
  {nom:"Curl biceps haltères",cat:"Bras / Biceps",type:"salle",depart:"Debout, haltères dans les mains, bras tendus le long du corps, paumes face à face.",exec:["Supine les poignets (paumes vers le ciel) en montant","Flexion stricte des coudes — corps immobile","Contracte le biceps fort au sommet","Descente lente et contrôlée 3 sec"],cles:["Le corps ne se balance JAMAIS — si oui, trop lourd","Full ROM : extension complète en bas + supination complète en haut","Coudes restent fixes le long du corps"],prog:"8 kg → 10 → 12 → 14–16 kg haltères",tip:"La supination complète en haut du mouvement cible le pic du biceps. Ne l'oublie pas."},
  {nom:"Curl marteau",cat:"Bras / Biceps / Avant-bras",type:"salle",depart:"Debout, haltères dans les mains, prise neutre (paumes face à face).",exec:["Monte les haltères sans tourner les poignets","Coudes fixes le long du corps","Contracte en haut","Descente contrôlée"],cles:["Cible le brachial ET le brachioradial (avant-bras)","Renforce la base des tractions et du muscle-up","Moins spectaculaire que le curl classique mais plus fonctionnel"],prog:"10 kg → 12 → 14 → 16–18 kg",tip:"Brachial développé = tractions plus puissantes. Indispensable pour le programme."},
  {nom:"Curl incliné haltères",cat:"Bras / Biceps",type:"salle",depart:"Assis sur banc incliné 45°, haltères bras tendus vers le bas.",exec:["Bras pend librement — c'est l'étirement maximal","Flexion des coudes vers les épaules","Supination complète au sommet","Retour lent en extension totale"],cles:["L'inclinaison crée l'étirement maximal du biceps — meilleur stimulus","Ne pas cambrer le dos pour aider","Excellent pour le développement du pic"],prog:"8 kg → 10 → 12 → 14 kg",tip:"L'étirement des muscles sous tension est le stimulus de croissance n°1. Le curl incliné l'exploit parfaitement."},
  {nom:"Curl barre EZ supination (pronation)",cat:"Bras / Biceps",type:"salle",depart:"Debout, barre EZ en prise pronation (dos des mains vers le haut).",exec:["Flexion des coudes avec prise pronation","Moins de biceps, plus de brachioradial","Descente contrôlée 3 sec","Extension complète"],cles:["Variation qui cible l'avant-bras plus que le curl classique","Renforce grip et poignets","Complémentaire du curl supination"],prog:"20 kg → 25 → 30 → 35 kg total",tip:"Les avant-bras puissants = grip puissant = toutes les tractions facilitées."},
  {nom:"Curl concentré",cat:"Bras / Biceps",type:"salle",depart:"Assis, coude appuyé contre la cuisse intérieure, haltère dans la main.",exec:["Flexion pure du coude","Coude reste fixe sur la cuisse — isolation maximale","Contracte fort au sommet","Retour lent"],cles:["L'exercice d'isolation biceps par excellence","Le coude sur la cuisse empêche tout balancement","Cible le pic du biceps"],prog:"10 kg → 12 → 14 → 16 kg",tip:"Arnold le faisait pour sculpter le pic. L'isolation totale crée le détail musculaire."},

  // ─── BRAS — TRICEPS ───
  {nom:"Triceps overhead extension (haltère ou câble)",cat:"Bras / Triceps",type:"salle",depart:"Debout ou assis, haltère tenu à deux mains au-dessus de la tête, bras tendus.",exec:["Plie les coudes en amenant le haltère derrière la tête","Coudes pointent vers le plafond et restent fixes","Extension complète des bras","Descente contrôlée"],cles:["Cible le long chef du triceps — souvent négligé","Étirement maximal du triceps en bas = stimulus fort","Coudes ne s'écartent pas sur les côtés"],prog:"10 kg → 12 → 14 → 16–18 kg haltère",tip:"Le long chef du triceps = 2/3 du volume du bras. L'overhead extension est son exercice roi."},
  {nom:"Triceps câble poulie haute (pushdown)",cat:"Bras / Triceps",type:"salle",depart:"Face à la poulie haute, prise de la corde ou barre, coudes collés au corps.",exec:["Pousse vers le bas en extension complète","Coudes restent FIXES — ne bougent pas","Contracte les triceps fort en bas","Retour lent contrôlé"],cles:["Coudes collés au corps = isolation stricte du triceps","Extension complète en bas = plein ROM","Prise corde = permet d'écarter en fin pour plus de contraction"],prog:"15 kg → 20 → 25 → 30–35 kg",tip:"Meilleur exercice d'isolation triceps car la résistance est constante tout au long du mouvement."},
  {nom:"Triceps dips (parallèles strict)",cat:"Bras / Triceps / Pectoraux",type:"cali",depart:"Sur barres parallèles, bras tendus. Corps DROIT — pas de lean avant.",exec:["Corps strictement vertical (pour cibler triceps pas pec)","Descend jusqu'à 90° minimum","Pousse en extension complète","Répète sans lean avant"],cles:["Lean avant = pectoraux / Corps droit = triceps","Le seul vrai exercice de dips pour les triceps","Amplitude complète indispensable"],prog:"Assistés → Corps droit libres → Lestés",tip:"En gardant le corps parfaitement droit, 80% du travail va aux triceps. C'est la version bras du dip."},
  {nom:"Triceps barre au front (skull crusher)",cat:"Bras / Triceps",type:"salle",depart:"Allongé sur banc, barre EZ ou haltères au-dessus du front, coudes à 90°.",exec:["Plie les coudes en amenant la barre vers le front","Coudes restent fixes pointés vers le plafond","Extension explosive des bras","Retour contrôlé"],cles:["Coudes ne s'écartent pas pendant le mouvement","Nom correct : skullcrusher — ne touche pas vraiment le front","Attention aux coudes si douleur — arrête"],prog:"15 kg → 20 → 25 → 30–35 kg total",tip:"Skull crusher = masse brute pour les triceps. Associé au curl biceps = bras complets."},

  // ─── ABDOS — COMPLÉMENTAIRES ───
  {nom:"Crunch inversé (reverse crunch)",cat:"Abdos",type:"cali",depart:"Allongé sur le dos, jambes à 90° (genoux au-dessus des hanches). Bras le long du corps.",exec:["Contracte les abdos et soulève le bassin du sol","Les genoux vont vers la poitrine","Pause 1 sec en haut en contractant fort","Descend lentement — jambes ne posent jamais"],cles:["C'est le BASSIN qui monte, pas les jambes","Pas d'élan — mouvement 100% contrôlé","Expiration en montant, inspiration en descendant","Cible les abdominaux inférieurs — rarement travaillés"],prog:"Genoux pliés → Jambes tendues → Avec lest cheville",tip:"Combine avec les leg raises : ensemble ils ciblent les 4 quadrants des abdominaux."},
  {nom:"Pallof press (élastique / câble)",cat:"Abdos / Anti-rotation",type:"cali",depart:"Debout de côté par rapport à l'ancrage, élastique à hauteur de poitrine.",exec:["Tend les bras devant toi — résiste à la rotation","L'élastique cherche à te faire tourner — NE TOURNE PAS","Maintiens 2 sec bras tendus","Reviens les mains à la poitrine"],cles:["But = NE PAS tourner — c'est de la stabilisation","Active les abdos comme si tu allais recevoir un coup","Anti-rotation = protection du dos bien supérieure aux crunches"],prog:"Élastique léger → Résistance forte → Pallof press en squat",tip:"L'anti-rotation est la qualité abdo la plus négligée. Elle protège ton dos mieux que 100 crunches."},
  {nom:"Superman hold",cat:"Abdos / Dos postérieur",type:"cali",depart:"Allongé face au sol, bras tendus devant la tête.",exec:["Lève simultanément bras et jambes du sol","Corps forme un arc léger — regard vers le sol","Maintiens en contractant érecteurs et fessiers","Respire normalement"],cles:["Gainage POSTÉRIEUR — la face cachée des abdos","Indispensable pour l'équilibre musculaire et prévenir les douleurs lombaires","Pour chaque plank, fais un superman — équilibre"],prog:"Hold 5 sec → 20 sec → Rocking → Avec lest",tip:"Pour chaque série de plank, fais un superman. Équilibre antérieur/postérieur = prévention n°1."},
];

// ─── TIPS ───
const TIPS = [
  {cat:"💪 Entraînement",text:"La technique est ton investissement à long terme. Une rep parfaite vaut 10 reps bâclées pour construire le muscle ET éviter les blessures.",source:"Principe fondamental calisthénie"},
  {cat:"😴 Sommeil",text:"Entre 22h et 2h du matin, l'hormone de croissance est libérée à 70% de sa production quotidienne. Dors tôt pour maximiser ta récupération musculaire.",source:"Science de la récupération"},
  {cat:"🥗 Nutrition",text:"Mange ta portion de protéines dans les 30–60 min après l'entraînement. C'est la fenêtre anabolique où ton muscle absorbe le mieux les acides aminés.",source:"Nutriperf"},
  {cat:"💪 Entraînement",text:"+1 rep cette semaine = progression réelle. Tu n'as pas besoin de te détruire — la surcharge progressive est la seule loi qui compte.",source:"Principe surcharge progressive"},
  {cat:"🧠 Mindset",text:"Compare-toi à toi d'il y a 4 semaines, pas à quelqu'un d'autre. Ton seul concurrent, c'est ta version du mois dernier.",source:"Psychologie de la performance"},
  {cat:"🔄 Récupération",text:"Le muscle ne pousse pas pendant l'entraînement — il pousse pendant la récupération. Sans repos = sans résultats.",source:"Physiologie musculaire"},
  {cat:"😴 Sommeil",text:"Une seule nuit courte réduit ta force maximale de 30% le lendemain et diminue la synthèse protéique. 7–9h minimum.",source:"Walker, Why We Sleep"},
  {cat:"💪 Skills",text:"Pour la planche : 5–10 min de travail dédié par jour, 6 jours sur 7. La fréquence bat l'intensité pour les skills neurologiques.",source:"Méthode Greasing the Groove"},
  {cat:"🥗 Nutrition",text:"La déshydratation à seulement 2% diminue les performances de 10–20%. 2.5–3L d'eau par jour minimum.",source:"Physiologie de l'hydratation"},
  {cat:"🧠 Mindset",text:"La discipline est ce que tu fais quand tu n'as pas envie. La motivation dure 3 jours — la discipline dure 12 mois.",source:"Jocko Willink"},
  {cat:"🔄 Récupération",text:"30 min de marche quotidienne active la circulation, réduit le cortisol et accélère l'élimination des déchets métaboliques.",source:"Science de la récupération active"},
  {cat:"💪 Entraînement",text:"Sur les skills avancés, travaille en début de séance. Après la fatigue musculaire, impossible d'apprendre neurologiquement.",source:"Neuroscience de l'apprentissage moteur"},
  {cat:"😴 Sommeil",text:"L'écran bleu supprime la mélatonine pendant 3h. Éteins les écrans 1h avant de dormir — ou active le mode nuit.",source:"Chronobiologie"},
  {cat:"🥗 Nutrition",text:"Mange des glucides autour de l'entraînement (30–60 min avant + 1h après). Rechargent le glycogène et soutiennent la synthèse protéique.",source:"Nutriperf"},
  {cat:"🔄 Prévention",text:"Douleur aiguë = stop IMMÉDIAT. Gêne = continue avec attention. Douleur nette = stop, glace, repos 48h.",source:"Médecine sportive"},
  {cat:"🧠 Mindset",text:"Tu construis un physique pour 20+ ans, pas pour le week-end. Chaque rep est un investissement à long terme.",source:"Psychologie de la performance"},
  {cat:"💪 Entraînement",text:"L'équilibre push/pull est non-négociable. Pour chaque série de push, fais une série de pull. Sinon : posture avachie garantie.",source:"Physiothérapie & Biomécanique"},
  {cat:"🥗 Nutrition",text:"Créatine : 3–5g par jour, tous les jours. Le seul supplément prouvé scientifiquement pour force ET hypertrophie.",source:"Meta-analyse ISSN 2023"},
  {cat:"😴 Sommeil",text:"La sieste de 20 min (pas plus) entre 13h et 15h améliore les performances de l'après-midi de 15–20%. La NASA l'utilise.",source:"Neurosciences NASA"},
  {cat:"🔄 Récupération",text:"Le foam rolling post-séance (5–10 min) réduit les courbatures de 30% en augmentant la circulation locale.",source:"Physiothérapie sportive"},
];

const FOOD_CATEGORIES = {
  "🥩 Protéines animales":[
    {nom:"Blanc de poulet",prot:"31g/100g",kcal:"165 kcal",portion:"150g = 46g prot"},
    {nom:"Thon en boîte (eau)",prot:"26g/100g",kcal:"116 kcal",portion:"1 boîte = 40g prot"},
    {nom:"Œufs entiers",prot:"13g/100g",kcal:"155 kcal",portion:"3 œufs = 19g prot"},
    {nom:"Blancs d'œufs",prot:"11g/100g",kcal:"52 kcal",portion:"4 blancs = 14g prot"},
    {nom:"Saumon atlantique",prot:"25g/100g",kcal:"208 kcal",portion:"150g = 37g prot"},
    {nom:"Steak bœuf 5%",prot:"26g/100g",kcal:"175 kcal",portion:"150g = 39g prot"},
    {nom:"Dinde hachée",prot:"29g/100g",kcal:"190 kcal",portion:"150g = 43g prot"},
    {nom:"Crevettes",prot:"24g/100g",kcal:"99 kcal",portion:"100g = 24g prot"},
  ],
  "🥛 Protéines laitières":[
    {nom:"Fromage blanc 0%",prot:"8g/100g",kcal:"45 kcal",portion:"200g = 16g prot"},
    {nom:"Skyr nature",prot:"11g/100g",kcal:"66 kcal",portion:"150g = 16g prot"},
    {nom:"Yaourt grec 0%",prot:"10g/100g",kcal:"57 kcal",portion:"200g = 20g prot"},
    {nom:"Cottage cheese",prot:"12g/100g",kcal:"92 kcal",portion:"200g = 24g prot"},
    {nom:"Whey protéine",prot:"80g/100g",kcal:"380 kcal",portion:"30g = 24g prot"},
  ],
  "🌾 Glucides complexes":[
    {nom:"Riz basmati cuit",prot:"2.5g/100g",kcal:"130 kcal",portion:"200g = 50g glucides"},
    {nom:"Flocons d'avoine",prot:"13g/100g",kcal:"379 kcal",portion:"80g sec = 50g glucides"},
    {nom:"Patate douce cuite",prot:"2g/100g",kcal:"90 kcal",portion:"200g = 40g glucides"},
    {nom:"Quinoa cuit",prot:"4.5g/100g",kcal:"120 kcal",portion:"200g = 34g glucides"},
    {nom:"Pain complet",prot:"9g/100g",kcal:"247 kcal",portion:"2 tranches = 30g glucides"},
    {nom:"Pâtes complètes cuites",prot:"5g/100g",kcal:"157 kcal",portion:"200g = 40g glucides"},
    {nom:"Lentilles cuites",prot:"9g/100g",kcal:"116 kcal",portion:"150g = 22g prot + 25g glucides"},
  ],
  "🥑 Lipides de qualité":[
    {nom:"Avocat",prot:"2g/100g",kcal:"160 kcal",portion:"1/2 = 12g lipides"},
    {nom:"Huile d'olive vierge",prot:"0g",kcal:"884 kcal/100g",portion:"1 CS = 14g lipides"},
    {nom:"Amandes nature",prot:"21g/100g",kcal:"579 kcal",portion:"30g = 14g lipides"},
    {nom:"Beurre de cacahuète",prot:"25g/100g",kcal:"598 kcal",portion:"2 CS = 16g lip + 8g prot"},
    {nom:"Graines de chia",prot:"17g/100g",kcal:"486 kcal",portion:"2 CS = 9g lip + oméga-3"},
  ],
  "🍌 Fruits & Énergie":[
    {nom:"Banane",prot:"1.1g/100g",kcal:"89 kcal",portion:"1 grande = 30g glucides"},
    {nom:"Dattes Medjool",prot:"1.8g/100g",kcal:"277 kcal",portion:"2 dattes = 30g glucides rapides"},
    {nom:"Myrtilles",prot:"0.7g/100g",kcal:"57 kcal",portion:"100g = antioxydants"},
    {nom:"Orange",prot:"0.9g/100g",kcal:"47 kcal",portion:"1 grande = vit. C"},
  ],
  "🫙 Légumes & Fibres":[
    {nom:"Brocoli",prot:"2.8g/100g",kcal:"34 kcal",portion:"200g = fibres + vitamines"},
    {nom:"Épinards",prot:"2.9g/100g",kcal:"23 kcal",portion:"Illimité — fer + magnésium"},
    {nom:"Poivron rouge",prot:"1g/100g",kcal:"31 kcal",portion:"1 = 200% VQ vit. C"},
    {nom:"Asperges",prot:"2.2g/100g",kcal:"20 kcal",portion:"Diurétique naturel"},
  ],
};

// Timing nutritionnel par horaire + phase
const TIMING = {
  surplus:{
    A:[
      {time:"06:45",text:"Réveil · 500ml eau · protéines 25–30g + glucides 50–60g",train:false},
      {time:"09:00",text:"Arrivée bureau · café ou thé vert",train:false},
      {time:"12:00",text:"Déjeuner : 150g viande/poisson + 200g riz ou patate douce + légumes + huile olive",train:false},
      {time:"15:30",text:"Collation pré-training : banane + yaourt grec ou whey 20g · départ salle ~17h30",train:false},
      {time:"17:00",text:"Fin travail · direction salle",train:false},
      {time:"17:30",text:"ENTRAÎNEMENT",train:true},
      {time:"19:30",text:"Post-training (dans l'heure) : whey 30g + riz 200g + poulet 150g · PRIORITÉ",train:false},
      {time:"21:30",text:"Dîner léger si macros atteints · ou repas complet si besoin",train:false},
      {time:"22:30",text:"Casein shake : 200g fromage blanc 0% · anabolisme nocturne",train:false},
    ],
    B:[
      {time:"09:00",text:"Réveil · 500ml eau · protéines 25g + glucides 40g",train:false},
      {time:"11:30",text:"Début travail · déjeuner pris avant ou apporté",train:false},
      {time:"12:00",text:"Déjeuner : 150g viande/poisson + 200g féculents + légumes",train:false},
      {time:"15:00",text:"Collation mid-shift : fromage blanc 150g + amandes · soutient l'énergie",train:false},
      {time:"19:30",text:"Fin travail · 30 min post-travail = pré-training",train:false},
      {time:"20:00",text:"Pré-training : banane + café ou whey léger · séance ~20h15",train:false},
      {time:"20:15",text:"ENTRAÎNEMENT",train:true},
      {time:"22:00",text:"Post-training (dans l'heure) : whey 30g + riz 200g + protéines · PRIORITÉ",train:false},
      {time:"23:00",text:"200g fromage blanc 0% + cannelle · récupération nocturne",train:false},
    ]
  },
  cut:{
    A:[
      {time:"06:45",text:"Réveil · eau + café noir · protéines 30g + peu de glucides",train:false},
      {time:"09:00",text:"Arrivée bureau · café ou thé",train:false},
      {time:"12:00",text:"Déjeuner : 180g viande maigre/poisson + légumes à volonté + 100g riz",train:false},
      {time:"15:30",text:"Collation légère : 150g fromage blanc 0% + 10 amandes",train:false},
      {time:"17:30",text:"ENTRAÎNEMENT",train:true},
      {time:"19:30",text:"Post-training : 40g whey ou 180g poulet + légumes + 50–80g glucides",train:false},
      {time:"22:00",text:"200g fromage blanc 0% + cannelle si faim",train:false},
    ],
    B:[
      {time:"09:00",text:"Réveil · eau + café noir · protéines 30g + minimum glucides",train:false},
      {time:"12:30",text:"Déjeuner : 180g viande maigre/poisson + légumes + 100g riz ou patate douce",train:false},
      {time:"15:30",text:"Collation : 150g skyr + 10 amandes",train:false},
      {time:"19:30",text:"Fin travail · pré-training : banane uniquement",train:false},
      {time:"20:15",text:"ENTRAÎNEMENT",train:true},
      {time:"22:15",text:"Post-training : 40g whey + poulet + légumes · AUCUN glucide lourd",train:false},
      {time:"23:00",text:"200g fromage blanc 0% + cannelle",train:false},
    ]
  }
};

const RECORDS_DATA = [
  {nom:"Tractions pronation (max reps)",current:0,s12:8,s24:14,s52:20,unit:"reps"},
  {nom:"Dips profonds (max reps)",current:5,s12:15,s24:22,s52:30,unit:"reps"},
  {nom:"Pompes (max reps)",current:12,s12:30,s24:40,s52:60,unit:"reps"},
  {nom:"Planche tuck (secondes)",current:0,s12:20,s24:30,s52:15,unit:"sec",note:"Obj S52 = straddle 15s"},
  {nom:"Handstand mur (sec)",current:0,s12:25,s24:40,s52:10,unit:"sec",note:"Obj S52 = freestanding 10s"},
  {nom:"L-sit (sec)",current:0,s12:10,s24:20,s52:15,unit:"sec",note:"Obj S52 = V-sit 15s"},
  {nom:"Muscle-up (reps)",current:0,s12:0,s24:1,s52:5,unit:"reps"},
  {nom:"Squat barre (kg)",current:20,s12:70,s24:85,s52:115,unit:"kg"},
  {nom:"Poids de corps (kg)",current:75,s12:76,s24:78,s52:77,unit:"kg",note:"+muscle -gras"},
];

const MENSURATIONS_FIELDS = [
  {key:"poids",label:"Poids",unit:"kg"},
  {key:"tour_poitrine",label:"Tour poitrine",unit:"cm"},
  {key:"tour_taille",label:"Tour taille",unit:"cm"},
  {key:"tour_hanches",label:"Tour hanches",unit:"cm"},
  {key:"tour_bras_g",label:"Bras gauche",unit:"cm"},
  {key:"tour_bras_d",label:"Bras droit",unit:"cm"},
  {key:"tour_cuisse",label:"Tour cuisse",unit:"cm"},
  {key:"tour_mollet",label:"Tour mollet",unit:"cm"},
  {key:"graisse",label:"% Graisse (estimé)",unit:"%"},
];

// ═══════════════════════════════════════════════════
// STATE
// ═══════════════════════════════════════════════════
let ST = {
  startDate:null, prenom:"", records:{}, photos:[], doneCriteria:{p1:[],p2:[]},
  streak:0, lastTrainDate:null, tipIdx:0, nutrMode:'surplus', horaire:'A',
  mensurations:[], doneExos:{}, currentPhase:'p1', currentDayIdx:null,
};
function loadST(){try{const s=localStorage.getItem('cali-v3');if(s)Object.assign(ST,JSON.parse(s));}catch(e){}}
function saveST(){try{localStorage.setItem('cali-v3',JSON.stringify(ST));}catch(e){}}

// ─── TIMER ───
let TMR = {total:90,remaining:90,running:false,iv:null,activePreset:90};
function setTimer(s,btn){
  clearInterval(TMR.iv); TMR.total=s; TMR.remaining=s; TMR.running=false; TMR.activePreset=s;
  document.querySelectorAll('.ts-preset').forEach(b=>b.classList.remove('ts-active'));
  if(btn) btn.classList.add('ts-active');
  updateTimerDisplay(); updateTimerBtn();
}
function toggleTimer(){
  if(TMR.running){clearInterval(TMR.iv);TMR.running=false;}
  else{
    if(TMR.remaining<=0){TMR.remaining=TMR.total;}
    TMR.running=true;
    TMR.iv=setInterval(()=>{
      TMR.remaining--;
      updateTimerDisplay();
      if(TMR.remaining<=0){clearInterval(TMR.iv);TMR.running=false;updateTimerBtn();showToast('⏰ Repos terminé — c\'est reparti !');}
    },1000);
  }
  updateTimerBtn();
}
function resetTimer(){clearInterval(TMR.iv);TMR.remaining=TMR.total;TMR.running=false;updateTimerDisplay();updateTimerBtn();}
function updateTimerDisplay(){
  const m=Math.floor(TMR.remaining/60),s=TMR.remaining%60;
  const pct=TMR.total>0?(TMR.remaining/TMR.total*100):100;
  const disp=document.getElementById('timer-disp');
  const bar=document.getElementById('timer-bar');
  if(disp){
    disp.textContent=`${String(m).padStart(2,'0')}:${String(s).padStart(2,'0')}`;
    disp.className='timer-sticky-display'+(TMR.running&&TMR.remaining>15?' ts-running':TMR.remaining<=15&&TMR.remaining>0?' ts-warning':TMR.remaining===0?' ts-done':'');
  }
  if(bar) bar.style.width=pct+'%';
}
function updateTimerBtn(){
  const btn=document.getElementById('timer-go-btn');
  if(!btn)return;
  if(TMR.running){btn.textContent='⏸ Pause';btn.className='ts-btn ts-btn-pause';}
  else{btn.textContent='▶ Go';btn.className='ts-btn ts-btn-go';}
}

// ═══════════════════════════════════════════════════
// HELPERS
// ═══════════════════════════════════════════════════
function getDayNum(){if(!ST.startDate)return 1;return Math.max(1,Math.floor((new Date()-new Date(ST.startDate))/86400000)+1);}
function getWeekNum(){return Math.ceil(getDayNum()/7);}
function getPhaseKey(){const w=getWeekNum();return w<=8?'p1':w<=24?'p2':'p3';}
function isDeload(){return[8,16,24,32,40,48].includes(getWeekNum());}
function getTodayKey(){return'done_'+new Date().toISOString().split('T')[0];}
function getDow(){const d=new Date().getDay();return d===0?6:d-1;} // 0=Lun..6=Dim

function switchTab(n){
  document.querySelectorAll('.tab').forEach(t=>t.classList.remove('active'));
  document.querySelectorAll('.nav-btn').forEach(b=>b.classList.remove('active'));
  document.getElementById('tab-'+n).classList.add('active');
  document.querySelector(`[data-tab="${n}"]`).classList.add('active');
}

// ═══════════════════════════════════════════════════
// Legacy stubs — plus utilisés
function checkOnboard(){}
function validateOnboard(){}
function checkPin(){}

// ═══════════════════════════════════════════════════
// ACCUEIL
// ═══════════════════════════════════════════════════
function buildAccueil(){
  const now=new Date();
  const dayNum=getDayNum();
  const week=getWeekNum();
  const phKey=getPhaseKey();
  const ph=PROGRAMME[phKey];
  const dow=getDow();
  const todayJour=ph.jours[dow%ph.jours.length];
  const isDeloadW=isDeload();
  const prenom=ST.prenom||'Champion';

  // Message motivationnel dynamique
  const lastTrain=ST.lastTrainDate;
  const today=now.toISOString().split('T')[0];
  const yesterday=new Date(Date.now()-86400000).toISOString().split('T')[0];
  const twoDaysAgo=new Date(Date.now()-172800000).toISOString().split('T')[0];
  const streak=ST.streak||0;
  const totalDone=countTotalSessions();

  let greeting='', msg='', submsg='', badges='';
  const phIcon={p1:'⚡',p2:'🔥',p3:'💎'}[phKey];

  document.getElementById('home-greeting').textContent=now.toLocaleDateString('fr-FR',{weekday:'long',day:'numeric',month:'long'}).toUpperCase();

  if(isDeloadW){
    msg=`${prenom}, c'est ta semaine de récupération.`;
    submsg="Réduis le volume de 50%. Ton corps reconstruit en ce moment même. Profite, dors et mange bien.";
  } else if(todayJour.badge==='rest'){
    msg=`Repos actif aujourd'hui, ${prenom}.`;
    submsg="30 min de marche, 15 min de mobilité. Le repos fait partie du programme — respecte-le.";
  } else if(!lastTrain || lastTrain < twoDaysAgo){
    const daysMissed=lastTrain?Math.floor((new Date(today)-new Date(lastTrain))/86400000):dayNum;
    msg=`${daysMissed > 3 ? `${daysMissed} jours sans séance, ${prenom}` : `Manque à l'appel, ${prenom}`}. Reprends les rênes.`;
    submsg="Le physique ne se construit pas dans ta tête. Chaque jour raté est un jour donné à ceux qui sont là.";
  } else if(streak>=7){
    msg=`${streak} jours de suite. ${prenom}, un vrai champion est en train de naître. 🏆`;
    submsg=`Semaine ${week} — ${ph.label}. Tu construis quelque chose de solide.`;
  } else if(streak>=3){
    msg=`${streak} séances sur ${streak} — tu es dans la zone, ${prenom}.`;
    submsg="La consistance est le seul secret qui n'en est pas un. Continue exactement comme ça.";
  } else if(totalDone===0){
    msg=`Prêt à démarrer, ${prenom} ?`;
    submsg="Semaine 1. Phase 1. Jour 1. C'est ici que tout commence. La fondation se pose maintenant.";
  } else {
    msg=`Semaine ${week}, ${phIcon} ${ph.label}.`;
    submsg=`${totalDone} séance${totalDone>1?'s':''} réalisée${totalDone>1?'s':''} depuis le début. Chaque rep compte.`;
  }

  document.getElementById('home-msg').textContent=msg;
  document.getElementById('home-submsg').textContent=submsg;
  badges+=`<span class="home-badge home-badge-phase">${phIcon} ${ph.label}</span>`;
  if(isDeloadW) badges+=`<span class="home-badge home-badge-deload">🟠 Semaine déload S${week}</span>`;
  if(streak>0) badges+=`<span class="home-badge home-badge-rest">${streak}🔥 streak</span>`;
  document.getElementById('home-badges').innerHTML=badges;

  // Stats
  document.getElementById('home-stats').innerHTML=`
    <div class="home-stat"><div class="home-stat-val gold">S${week}</div><div class="home-stat-label">Semaine</div></div>
    <div class="home-stat"><div class="home-stat-val">${dayNum}</div><div class="home-stat-label">Jour du programme</div></div>
    <div class="home-stat"><div class="home-stat-val green">${totalDone}</div><div class="home-stat-label">Séances réalisées</div></div>
    <div class="home-stat"><div class="home-stat-val">${streak}🔥</div><div class="home-stat-label">Streak actuel</div></div>
  `;

  // Shortcuts
  document.getElementById('shortcut-seance-sub').textContent=todayJour.badge==='rest'?'Repos actif aujourd\'hui':`${todayJour.titre} — ${todayJour.sous.substring(0,30)}...`;
  document.getElementById('shortcut-photos-sub').textContent=(ST.photos?.length||0)+' photo'+ ((ST.photos?.length||0)!==1?'s':'') +' uploadée'+ ((ST.photos?.length||0)!==1?'s':'');

  // Tip du jour
  ST.tipIdx = dayNum % TIPS.length;
  renderTip();

  // Prochaines séances
  const upList=document.getElementById('upcoming-list');
  upList.innerHTML='';
  const badgeStyles={push:'background:#EBF2F8;color:#2A5F8A',pull:'background:#FBEAEA;color:#8A2A2A',legs:'background:#EAF3EC;color:#2A6B3A',skills:'background:#FDF3E7;color:#C4622D',rest:'background:var(--pearl);color:var(--mid)',core:'background:#EAF3EC;color:#2A6B3A'};
  for(let i=0;i<5;i++){
    const d=(dow+i)%7;
    const j=ph.jours[d%ph.jours.length];
    const dayName=i===0?'Aujourd\'hui':i===1?'Demain':JOURS_SEMAINE[(dow+i)%7];
    upList.innerHTML+=`<div class="upcoming-item">
      <div class="upcoming-day">${dayName}</div>
      <div class="upcoming-name">${j.titre}</div>
      <span class="upcoming-badge" style="${badgeStyles[j.badge]||''};padding:2px 8px;border-radius:10px;">${j.badge.toUpperCase()}</span>
    </div>`;
  }
}

function countTotalSessions(){
  if(ST.completedSessions && ST.completedSessions.length) return ST.completedSessions.length;
  let count=0;
  for(const k in ST){if(k.startsWith('done_')&&Array.isArray(ST[k])&&ST[k].length>0)count++;}
  return count;
}

function goToProgramme(){
  switchTab('programme');
  // Active le bon jour
  const dow=getDow();
  setTimeout(()=>{
    const btns=document.querySelectorAll('.week-day-btn');
    if(btns[dow]) btns[dow].click();
  },100);
}

// ═══════════════════════════════════════════════════
// TIPS
// ═══════════════════════════════════════════════════
function renderTip(){
  const t=TIPS[ST.tipIdx%TIPS.length];
  document.getElementById('tip-daily-cat').textContent=t.cat;
  document.getElementById('tip-daily-text').textContent=t.text;
  document.getElementById('tip-daily-src').textContent=t.source;
}
function nextTip(){ST.tipIdx=(ST.tipIdx+1)%TIPS.length;renderTip();}
function prevTip(){ST.tipIdx=(ST.tipIdx-1+TIPS.length)%TIPS.length;renderTip();}
function randomTip(){ST.tipIdx=Math.floor(Math.random()*TIPS.length);renderTip();}

// ═══════════════════════════════════════════════════
// PROGRAMME
// ═══════════════════════════════════════════════════
let activeProgramPhase='p1';

function buildProgramme(){
  // Bannière déload
  const db=document.getElementById('deload-banner-wrap');
  if(isDeload()){
    db.innerHTML=`<div class="deload-banner">🟠 Semaine ${getWeekNum()} — DÉLOAD : -50% volume, -40% intensité. Même exercices, moitié des séries.</div>`;
  } else db.innerHTML='';

  // Phase auto-select selon semaine
  const phKey=getPhaseKey();
  activeProgramPhase=phKey;
  document.querySelectorAll('.phase-tab').forEach(b=>b.classList.remove('active'));
  const phIdx={p1:0,p2:1,p3:2}[phKey];
  document.querySelectorAll('.phase-tab')[phIdx]?.classList.add('active');
  document.querySelectorAll('.phase-content').forEach(c=>c.classList.remove('active'));
  document.getElementById('pc-'+phKey).classList.add('active');

  buildDayBar();
  buildProgrammePhases();
}

function buildDayBar(){
  const bar=document.getElementById('week-day-bar');
  bar.innerHTML='';
  const ph=PROGRAMME[activeProgramPhase];
  const dow=getDow();
  const activeIdx=ST.currentDayIdx!==null?ST.currentDayIdx:dow;

  JOURS_SEMAINE.forEach((dayName,i)=>{
    const jIdx=i%ph.jours.length;
    const jour=ph.jours[jIdx];
    const isToday=i===dow;
    const isActive=i===activeIdx;
    const btn=document.createElement('div');
    btn.className='week-day-btn'+(isToday?' today-day':'')+(isActive?' active':'');
    btn.innerHTML=`
      <div class="week-day-name">${dayName}</div>
      <div class="week-day-session">${jour.titre.split(' ')[0]}</div>
      <div class="week-day-dot" style="background:${BADGE_COLORS[jour.badge]||'#999'}"></div>
    `;
    btn.onclick=()=>selectDay(i);
    bar.appendChild(btn);
  });

  renderSeanceView(activeIdx);
}

function selectDay(idx){
  ST.currentDayIdx=idx;
  document.querySelectorAll('.week-day-btn').forEach((b,i)=>{
    b.classList.toggle('active',i===idx);
  });
  renderSeanceView(idx);
}

function renderSeanceView(dayIdx){
  const ph=PROGRAMME[activeProgramPhase];
  const jIdx=dayIdx%ph.jours.length;
  const jour=ph.jours[jIdx];
  const dow=getDow();
  const isToday=dayIdx===dow;

  // Clé de stockage correcte pour ce jour
  const dateKey=getKeyForDayIdx(dayIdx);
  if(!ST[dateKey]) ST[dateKey]=[];

  // Compter exercices déjà faits
  const allExos=[];
  jour.sections.forEach(s=>s.exos.forEach(e=>allExos.push(e.nom)));
  const doneCount=(ST[dateKey]||[]).filter(n=>allExos.includes(n)).length;
  const pct=allExos.length>0?Math.round(doneCount/allExos.length*100):0;

  const bCss=BADGE_CSS[jour.badge]||'sv-badge-rest';
  let html=`<div class="seance-view">
    <div class="seance-view-header">
      <div style="display:flex;align-items:flex-start;justify-content:space-between;gap:12px;">
        <div>
          <div class="seance-view-title">${jour.titre}${isToday?'<span style="font-size:13px;background:var(--gold);color:white;padding:3px 10px;border-radius:10px;margin-left:10px;vertical-align:middle;">Aujourd\'hui</span>':''}</div>
          <div class="seance-view-sub">${jour.sous}</div>
        </div>
        <span class="sv-badge ${bCss}" style="flex-shrink:0;margin-top:4px;">${jour.badge.toUpperCase()}</span>
      </div>
      <div class="seance-view-badges" style="margin-top:10px;">
        <span style="font-size:12px;color:rgba(255,255,255,.5);">${ph.split}</span>
        ${allExos.length>0?`<span id="seance-counter" style="font-size:12px;color:rgba(255,255,255,.7);">${doneCount}/${allExos.length} exercices</span>`:''}
      </div>
    </div>
    <div class="seance-progress-bar"><div class="seance-progress-fill" id="seance-prog-fill" style="width:${pct}%"></div></div>`;

  jour.sections.forEach(sec=>{
    const tagClass={cali:'tag-cali',salle:'tag-salle',skills:'tag-skills',core:'tag-core'}[sec.tag]||'tag-cali';
    const tagLabel={cali:'Calisthénie',salle:'Salle Basic Fit',skills:'⭐ Skills',core:'Core'}[sec.tag]||'';
    html+=`<div class="seance-section-label">
      <span class="seance-section-tag ${tagClass}">${tagLabel}</span>
      <span class="seance-section-name">${sec.label}</span>
    </div>`;
    sec.exos.forEach(ex=>{
      const done=(ST[dateKey]||[]).includes(ex.nom);
      const safeNom=ex.nom.replace(/'/g,"\\'").replace(/\\/g,'\\\\');
      html+=`<div class="exo-row${done?' done-row':''}" id="exo-r-${ex.nom.replace(/\W/g,'_')}" onclick="toggleExoRow('${safeNom}',${dayIdx})">
        <div class="exo-row-check">${done?'✓':''}</div>
        <div class="exo-row-info">
          <div class="exo-row-name">${ex.nom}</div>
          <div class="exo-row-meta">
            <span class="exo-row-sets">${ex.sets}</span>
            ${ex.note?`<span>${ex.note}</span>`:''}
            ${ex.prog?`<span class="exo-row-prog">${ex.prog}</span>`:''}
          </div>
          ${ex.quand?`<div style="font-size:11px;color:var(--gold);margin-top:2px;">🎯 ${ex.quand}</div>`:''}
        </div>
        <button class="exo-timer-btn" onclick="event.stopPropagation();setTimer(90,null);showToast('⏱ Timer 1:30');" title="Timer repos">⏱</button>
      </div>`;
    });
  });

  // Timer sticky
  html+=`<div class="timer-sticky">
    <div class="timer-sticky-display ts-running" id="timer-disp">01:30</div>
    <div class="timer-sticky-progress" style="position:absolute;bottom:0;left:0;right:0;"><div class="timer-sticky-bar" id="timer-bar" style="width:100%"></div></div>
    <div class="timer-sticky-presets">
      <button class="ts-preset" onclick="setTimer(60,this)">1:00</button>
      <button class="ts-preset ts-active" onclick="setTimer(90,this)">1:30</button>
      <button class="ts-preset" onclick="setTimer(120,this)">2:00</button>
      <button class="ts-preset" onclick="setTimer(180,this)">3:00</button>
    </div>
    <div class="timer-sticky-controls">
      <button class="ts-btn ts-btn-go" id="timer-go-btn" onclick="toggleTimer()">▶ Go</button>
      <button class="ts-btn ts-btn-reset" onclick="resetTimer()">↺</button>
    </div>
  </div></div>`;

  document.getElementById('seance-view-wrap').innerHTML=html;
  updateTimerDisplay();
}

function toggleExoRow(exoNom, dayIdx){
  // Clé unique par jour sélectionné — permet de cocher n'importe quel jour
  const dateKey = getKeyForDayIdx(parseInt(dayIdx));
  if(!ST[dateKey]) ST[dateKey]=[];
  const idx=ST[dateKey].indexOf(exoNom);
  const el=document.getElementById('exo-r-'+exoNom.replace(/\W/g,'_'));
  if(idx===-1){
    ST[dateKey].push(exoNom);
    if(el){el.classList.add('done-row');el.querySelector('.exo-row-check').textContent='✓';}
  } else {
    ST[dateKey].splice(idx,1);
    if(el){el.classList.remove('done-row');el.querySelector('.exo-row-check').textContent='';}
  }

  // Recalcule progression
  const ph=PROGRAMME[activeProgramPhase];
  const jIdx=parseInt(dayIdx)%ph.jours.length;
  const jour=ph.jours[jIdx];
  const allExos=[];
  jour.sections.forEach(s=>s.exos.forEach(e=>allExos.push(e.nom)));
  const done=ST[dateKey].filter(n=>allExos.includes(n)).length;
  const pct=allExos.length>0?Math.round(done/allExos.length*100):0;
  const fill=document.getElementById('seance-prog-fill');
  if(fill) fill.style.width=pct+'%';
  // Mise à jour compteur dans le header séance
  const counter=document.getElementById('seance-counter');
  if(counter) counter.textContent=`${done}/${allExos.length} exercices`;

  // Séance complète → streak + félicitations + semaine avance
  if(done>=allExos.length && allExos.length>0){
    const todayStr=new Date().toISOString().split('T')[0];
    // On incrémente le streak seulement si c'est la séance du jour réel
    if(parseInt(dayIdx)===getDow() && ST.lastTrainDate!==todayStr){
      const yesterday=new Date(Date.now()-86400000).toISOString().split('T')[0];
      ST.streak=ST.lastTrainDate===yesterday?(ST.streak||0)+1:1;
      ST.lastTrainDate=todayStr;
      // Incrémente le compteur de séances total
      if(!ST.completedSessions) ST.completedSessions=[];
      if(!ST.completedSessions.includes(todayStr)) ST.completedSessions.push(todayStr);
      saveST();
      buildAccueil();
      showCongrats(done);
    } else if(parseInt(dayIdx)!==getDow()){
      // Séance passée ou future cochée manuellement — on sauvegarde sans streak
      saveST();
      showToast('✅ Séance enregistrée !');
    }
  }
  saveST();
}

// Retourne une clé de stockage pour un dayIdx donné (basée sur la vraie date du jour correspondant)
function getKeyForDayIdx(dayIdx){
  const dow=getDow();
  const diff=dayIdx-dow;
  const d=new Date();
  d.setDate(d.getDate()+diff);
  return 'done_'+d.toISOString().split('T')[0];
}

function showCongrats(total){
  const msgs=[
    `${total} exercices. Streak : ${ST.streak} jour${ST.streak>1?'s':''} consécutif${ST.streak>1?'s':''} 🔥`,
    `Séance 100% terminée. Ton corps progresse en ce moment même. Récupère bien.`,
    `Impeccable. Semaine ${getWeekNum()} avance. Chaque séance forge le physique.`,
  ];
  document.getElementById('congrats-msg').textContent=msgs[Math.floor(Math.random()*msgs.length)];
  document.getElementById('congrats-overlay').classList.add('show');
}

function switchPhase(pk, btn){
  activeProgramPhase=pk;
  ST.currentDayIdx=null;
  document.querySelectorAll('.phase-tab').forEach(t=>t.classList.remove('active'));
  if(btn) btn.classList.add('active');
  document.querySelectorAll('.phase-content').forEach(c=>c.classList.remove('active'));
  document.getElementById('pc-'+pk).classList.add('active');
  buildDayBar();
}

function buildProgrammePhases(){
  ['p1','p2','p3'].forEach(pk=>{
    const ph=PROGRAMME[pk];
    const cont=document.getElementById('pc-'+pk);
    if(!cont) return;
    let html=`<div class="card" style="margin-bottom:20px;background:var(--cream);">
      <div style="font-family:'Playfair Display',serif;font-size:15px;font-weight:700;margin-bottom:6px;">${ph.label} — ${ph.semaines}</div>
      <p style="font-size:13px;color:var(--mid);margin-bottom:6px;">${ph.objectif}</p>
      <p style="font-size:12px;font-weight:600;">🗓 ${ph.split}</p>
    </div>`;

    if(ph.skills?.length){
      html+=`<div class="card" style="margin-bottom:20px;">
        <div class="card-title">⭐ Skills Focus</div>
        <div class="skills-grid">${ph.skills.map(sk=>`
          <div class="skill-card">
            <div style="font-weight:700;font-size:13px;margin-bottom:4px;">${sk.nom}</div>
            <div style="font-size:11px;color:var(--mid);">${sk.exo} · ${sk.vol}</div>
            <div class="skill-target">Objectif : ${sk.cible}</div>
          </div>`).join('')}
        </div>
      </div>`;
    }

    if(ph.criteres?.length){
      html+=`<div style="background:#EAF3EC;border:1.5px solid #90C6A0;border-radius:var(--radius);padding:20px;margin-bottom:16px;">
        <div style="font-family:'Playfair Display',serif;font-size:14px;font-weight:700;color:var(--green);margin-bottom:12px;">✅ Critères de passage phase suivante</div>
        ${ph.criteres.map(c=>`<div style="display:flex;gap:8px;padding:5px 0;font-size:13px;border-bottom:1px dashed #cde4d4;"><span style="color:var(--green);">✓</span><span>${c}</span></div>`).join('')}
      </div>`;
    }

    cont.innerHTML=html;
  });
}

// ═══════════════════════════════════════════════════
// EXERCICES
// ═══════════════════════════════════════════════════
// Mapping filtre → fonction de test sur chaque exercice
const FILTER_MAP = {
  'Tout':      ()=>true,
  'Abdos':     e=>{ const c=e.cat.toLowerCase(); return c.includes('abdo')||c.includes('gainage')||c.includes('anti-rotation')||c.includes('oblique')||c.includes('postérieur');},
  'Pectoraux': e=>e.cat.toLowerCase().includes('pectoral'),
  'Dos':       e=>{ const c=e.cat.toLowerCase(); return c.includes('dos')||c.includes('trapèze')||c.includes('trapeze')||c.includes('traction')||c.includes('préhab');},
  'Épaules':   e=>{ const c=e.cat.toLowerCase(); return c.includes('épaule')||c.includes('epaule')||c.includes('deltoïde');},
  'Bras':      e=>{ const c=e.cat.toLowerCase(); return c.includes('bras')||c.includes('bicep')||c.includes('tricep')||c.includes('avant-bras');},
  'Jambes':    e=>{ const c=e.cat.toLowerCase(); return c.includes('jambe')||c.includes('ischio')||c.includes('fessier')||c.includes('quadri')||c.includes('mollet')||c.includes('nordic');},
  'Skills':    e=>{ const c=e.cat.toLowerCase(); return c.includes('skill')||c.includes('planche')||c.includes('mobilité')||c.includes('mobilite');},
  'Salle':     e=>e.type==='salle',
};

let exoFilterCat='Tout';
function buildExos(){
  const cats=['Tout','Abdos','Pectoraux','Dos','Épaules','Bras','Jambes','Skills','Salle'];
  const pills=document.getElementById('filter-pills');
  pills.innerHTML='';
  cats.forEach(cat=>{
    const b=document.createElement('button');
    b.className='pill'+(cat==='Tout'?' active':'');
    b.textContent=cat;
    b.onclick=()=>{
      exoFilterCat=cat;
      document.querySelectorAll('#filter-pills .pill').forEach(p=>p.classList.remove('active'));
      b.classList.add('active');
      filterExos();
    };
    pills.appendChild(b);
  });
  filterExos();
}
function filterExos(){
  const search=document.getElementById('exo-search').value.toLowerCase().trim();
  const filterFn = FILTER_MAP[exoFilterCat] || (()=>true);
  const filtered=EXERCICES_DB.filter(e=>{
    const matchCat = filterFn(e);
    const matchSearch = !search || e.nom.toLowerCase().includes(search) || e.cat.toLowerCase().includes(search);
    return matchCat && matchSearch;
  });
  const grid=document.getElementById('exo-lib-grid');
  grid.innerHTML='';
  filtered.forEach(exo=>{
    const div=document.createElement('div');
    div.className='exo-lib-card';
    div.innerHTML=`<div class="exo-lib-name">${exo.nom}</div>
      <div class="exo-lib-cat">${exo.cat} · ${exo.type==='cali'?'🏋️ Calisthénie':'🏟️ Salle'}</div>
      <div class="exo-lib-desc">${exo.depart.substring(0,100)}...</div>`;
    div.onclick=()=>openModal(exo);
    grid.appendChild(div);
  });
  if(!filtered.length) grid.innerHTML=`<div class="empty-state" style="grid-column:1/-1"><div class="empty-icon">🔍</div><div>Aucun exercice trouvé pour ce filtre</div></div>`;
}
function openModal(exo){
  document.getElementById('modal-content').innerHTML=`
    <button class="modal-close" onclick="document.getElementById('modal-overlay').classList.remove('open')">✕</button>
    <div class="modal-title">${exo.nom}</div>
    <div class="modal-cat">${exo.cat} · ${exo.type==='cali'?'🏋️ Calisthénie':'🏟️ Salle'}</div>
    <div class="modal-sec">📍 Position de départ</div>
    <p style="font-size:13px;line-height:1.6;">${exo.depart}</p>
    <div class="modal-sec">▶ Exécution</div>
    <ul class="modal-list">${exo.exec.map(e=>`<li>${e}</li>`).join('')}</ul>
    <div class="modal-sec">⚡ Points clés</div>
    <ul class="modal-list">${exo.cles.map(c=>`<li>${c}</li>`).join('')}</ul>
    <div class="modal-sec">📈 Progression</div>
    <p style="font-size:12px;color:var(--mid);line-height:1.6;">${exo.prog}</p>
    <div class="modal-tip">💡 <strong>Coach tip :</strong> ${exo.tip}</div>`;
  document.getElementById('modal-overlay').classList.add('open');
}
function closeModal(e){if(!e||e.target===document.getElementById('modal-overlay'))document.getElementById('modal-overlay').classList.remove('open');}

// ═══════════════════════════════════════════════════
// NUTRITION
// ═══════════════════════════════════════════════════
function buildNutrition(){renderNutrition();}
function setNutrMode(m,btn){ST.nutrMode=m;document.querySelectorAll('#tab-nutrition .filter-pills:first-of-type .pill').forEach(p=>p.classList.remove('active'));btn.classList.add('active');renderNutrition();}
function setHoraire(h,btn){ST.horaire=h;document.querySelectorAll('#tab-nutrition .filter-pills:last-of-type .pill').forEach(p=>p.classList.remove('active'));btn.classList.add('active');renderNutrition();}
function renderNutrition(){
  const macros=ST.nutrMode==='surplus'
    ?[{v:'2 900',l:'CALORIES/JOUR',c:'macro-kcal'},{v:'175g',l:'PROTÉINES',c:'macro-prot'},{v:'380g',l:'GLUCIDES',c:'macro-carb'},{v:'80g',l:'LIPIDES',c:'macro-fat'}]
    :[{v:'2 600',l:'CALORIES/JOUR',c:'macro-kcal'},{v:'180g',l:'PROTÉINES',c:'macro-prot'},{v:'280g',l:'GLUCIDES',c:'macro-carb'},{v:'75g',l:'LIPIDES',c:'macro-fat'}];
  document.getElementById('nutr-macros').innerHTML=macros.map(m=>`<div class="macro-card ${m.c}"><div class="macro-val">${m.v}</div><div class="macro-label">${m.l}</div></div>`).join('');

  const timingData=TIMING[ST.nutrMode][ST.horaire];
  document.getElementById('timing-list').innerHTML=timingData.map(t=>
    `<div class="timing-row${t.train?' timing-train':''}"><div class="timing-time">${t.time}</div><div>${t.text}</div></div>`
  ).join('');

  document.getElementById('supps-list').innerHTML=`
    <strong>💧 Eau :</strong> 2.5–3L minimum par jour<br><br>
    <strong>🧂 Créatine :</strong> 3–5g/jour · prouvée force + hypertrophie<br><br>
    <strong>🐟 Oméga-3 :</strong> 2–3g EPA+DHA · anti-inflammatoire, articulaire<br><br>
    <strong>☀️ Vitamine D3 :</strong> 2 000–4 000 UI/jour surtout en hiver<br><br>
    <strong>💤 Magnésium bisglycinate :</strong> 300–400mg le soir · sommeil + récup<br><br>
    <strong>☕ Caféine :</strong> 200mg 30 min pré-training · +10–15% performance`;

  const fc=document.getElementById('food-cats');
  fc.innerHTML='';
  Object.entries(FOOD_CATEGORIES).forEach(([cat,foods])=>{
    fc.innerHTML+=`<div class="food-cat-title">${cat}</div><div class="food-grid">${foods.map(f=>`
      <div class="food-item"><div class="food-name">${f.nom}</div><div class="food-macro">Prot: ${f.prot} · ${f.kcal}</div><div class="food-portion">${f.portion}</div></div>`).join('')}</div>`;
  });
}

// ═══════════════════════════════════════════════════
// PHOTOS
// ═══════════════════════════════════════════════════
let pendingPhotos=[];
function buildPhotos(){
  const sel=document.getElementById('photo-semaine');
  for(let i=1;i<=52;i++){const o=document.createElement('option');o.value=i;o.textContent=`Semaine ${i}`;sel.appendChild(o);}
  sel.value=getWeekNum();
  document.getElementById('photo-date').value=new Date().toISOString().split('T')[0];
  renderGallery();buildAA();
}
function toggleAA(){const s=document.getElementById('aa-section');s.style.display=s.style.display==='none'?'block':'none';}
function handlePhotoUpload(e){
  const files=Array.from(e.target.files);if(!files.length)return;
  pendingPhotos=[];const zone=document.getElementById('photo-preview-zone');zone.innerHTML='';
  let loaded=0;
  files.forEach(file=>{
    const r=new FileReader();
    r.onload=ev=>{pendingPhotos.push({src:ev.target.result});zone.innerHTML+=`<img src="${ev.target.result}" style="width:90px;height:75px;object-fit:cover;border-radius:8px;border:1px solid var(--border);margin-right:6px;">`;loaded++;if(loaded===files.length)document.getElementById('photo-form').classList.add('visible');};
    r.readAsDataURL(file);
  });
  e.target.value='';
}
function savePhoto(){
  const date=document.getElementById('photo-date').value;
  const sem=document.getElementById('photo-semaine').value;
  if(!date||!pendingPhotos.length){showToast('⚠️ Sélectionne une photo et une date');return;}
  pendingPhotos.forEach(ph=>{
    ST.photos.push({src:ph.src,date,semaine:parseInt(sem),type:document.getElementById('photo-type').value,poids:document.getElementById('photo-poids').value,note:document.getElementById('photo-note').value,id:Date.now()+Math.random()});
  });
  ST.photos.sort((a,b)=>new Date(b.date)-new Date(a.date));
  saveST();pendingPhotos=[];
  document.getElementById('photo-form').classList.remove('visible');
  document.getElementById('photo-preview-zone').innerHTML='';
  document.getElementById('photo-note').value='';
  document.getElementById('photo-poids').value='';
  renderGallery();buildAA();showToast('📸 Photo(s) sauvegardée(s) !');
}
function cancelPhoto(){document.getElementById('photo-form').classList.remove('visible');pendingPhotos=[];}
function renderGallery(){
  const g=document.getElementById('photo-gallery');
  if(!ST.photos?.length){g.innerHTML=`<div class="empty-state"><div class="empty-icon">📸</div><div>Aucune photo — upload ta première photo d'évolution !</div></div>`;return;}
  const byWeek={};
  ST.photos.forEach(ph=>{const k=`Semaine ${ph.semaine}`;if(!byWeek[k])byWeek[k]=[];byWeek[k].push(ph);});
  g.innerHTML='';
  Object.entries(byWeek).sort((a,b)=>parseInt(b[0].split(' ')[1])-parseInt(a[0].split(' ')[1])).forEach(([week,photos])=>{
    g.innerHTML+=`<div class="timeline-week"><div class="timeline-week-title">📅 ${week} — ${photos.length} photo${photos.length>1?'s':''}</div>
      <div class="photos-row">${photos.map(ph=>`
        <div class="photo-thumb"><div style="position:relative;"><img src="${ph.src}" alt="${ph.type}">
          <button class="photo-delete" onclick="deletePhoto(${ph.id},event)">✕</button></div>
          <div class="photo-thumb-info"><div class="photo-thumb-type">${ph.type}</div>
          <div class="photo-thumb-date">${new Date(ph.date).toLocaleDateString('fr-FR')}${ph.poids?' · '+ph.poids+'kg':''}</div>
          ${ph.note?`<div style="font-size:10px;color:var(--mid);">${ph.note}</div>`:''}</div>
        </div>`).join('')}
      </div></div>`;
  });
}
function deletePhoto(id,e){e.stopPropagation();ST.photos=ST.photos.filter(p=>p.id!==id);saveST();renderGallery();buildAA();}
function buildAA(){
  const b=document.getElementById('aa-before'),a=document.getElementById('aa-after');
  if(!b||!a)return;
  b.innerHTML='<option value="">Choisir...</option>';
  a.innerHTML='<option value="">Choisir...</option>';
  (ST.photos||[]).forEach((ph,i)=>{
    const l=`S${ph.semaine} · ${ph.type} · ${new Date(ph.date).toLocaleDateString('fr-FR')}`;
    b.innerHTML+=`<option value="${i}">${l}</option>`;
    a.innerHTML+=`<option value="${i}">${l}</option>`;
  });
}
function renderAA(){
  const bi=document.getElementById('aa-before').value,ai=document.getElementById('aa-after').value;
  const ph=ST.photos||[];
  document.getElementById('aa-before-img').innerHTML=bi!==''&&ph[bi]?`<img src="${ph[bi].src}" style="width:100%;max-height:220px;object-fit:cover;border-radius:8px;">`:'';
  document.getElementById('aa-after-img').innerHTML=ai!==''&&ph[ai]?`<img src="${ph[ai].src}" style="width:100%;max-height:220px;object-fit:cover;border-radius:8px;">`:'';
}

// ═══════════════════════════════════════════════════
// PROGRESSION
// ═══════════════════════════════════════════════════
function buildProgression(){
  // Paramètres
  document.getElementById('start-date-input').value=ST.startDate||'';
  document.getElementById('prenom-input').value=ST.prenom||'';

  // Formulaire mensurations
  const formGrid=document.getElementById('mensuration-form-grid');
  formGrid.innerHTML=MENSURATIONS_FIELDS.map(f=>`
    <div><label>${f.label} (${f.unit})</label><input type="number" id="mens-${f.key}" step="0.1" placeholder="${f.unit}" value="${getLastMensuration(f.key)||''}"></div>`).join('');

  // Historique mensurations
  renderMensurationHistory();

  // Records
  const el=document.getElementById('records-list');
  el.innerHTML='';
  RECORDS_DATA.forEach(rec=>{
    const saved=ST.records[rec.nom]!==undefined?ST.records[rec.nom]:rec.current;
    const pct=Math.min(100,Math.round(saved/rec.s52*100));
    const sid=rec.nom.replace(/[^a-zA-Z0-9]/g,'_');
    el.innerHTML+=`<div class="prog-item">
      <div class="prog-row">
        <div class="prog-name">${rec.nom}</div>
        <div id="rd-${sid}" style="display:flex;align-items:center;gap:8px;">
          <span class="prog-current">${saved} ${rec.unit}</span>
          <button class="record-edit-btn" onclick="editRec('${rec.nom}','${rec.unit}','${sid}')">✏️</button>
        </div>
        <div id="re-${sid}" style="display:none;align-items:center;gap:6px;">
          <input class="record-input-inline" type="number" id="ri-${sid}" value="${saved}" step="0.5">
          <span style="font-size:12px;color:var(--mid);">${rec.unit}</span>
          <button class="record-save-btn" onclick="saveRec('${rec.nom}','${rec.unit}','${sid}')">✓</button>
        </div>
      </div>
      ${rec.note?`<div style="font-size:11px;color:var(--gold);margin-bottom:6px;">${rec.note}</div>`:''}
      <div class="prog-bar-wrap"><div class="prog-bar" style="width:${pct}%"></div></div>
      <div style="display:flex;justify-content:space-between;font-size:11px;color:var(--mid);margin-top:4px;">
        <span>Actuel : <b>${saved}${rec.unit}</b></span>
        <span>S12: ${rec.s12} · S24: ${rec.s24}</span>
        <span>Obj S52 : <b>${rec.s52}${rec.unit}</b></span>
      </div>
    </div>`;
  });

  // Critères
  ['p1','p2'].forEach(pk=>{
    const el=document.getElementById(`criteria-${pk}`);if(!el)return;
    const ph=PROGRAMME[pk];
    if(!ph.criteres?.length){el.innerHTML='<p style="font-size:13px;color:var(--mid);">Phase 3 — tu es au sommet !</p>';return;}
    el.innerHTML='';
    if(!ST.doneCriteria[pk]) ST.doneCriteria[pk]=[];
    ph.criteres.forEach((c,i)=>{
      const done=ST.doneCriteria[pk].includes(i);
      const div=document.createElement('div');
      div.className='crit-item'+(done?' done':'');
      div.innerHTML=`<span style="font-size:16px;">${done?'✅':'⬜'}</span><span>${c}</span>`;
      div.onclick=()=>{
        const idx=ST.doneCriteria[pk].indexOf(i);
        if(idx===-1){ST.doneCriteria[pk].push(i);div.classList.add('done');div.querySelector('span').textContent='✅';showToast('🏆 Critère validé !');}
        else{ST.doneCriteria[pk].splice(idx,1);div.classList.remove('done');div.querySelector('span').textContent='⬜';}
        saveST();
      };
      el.appendChild(div);
    });
  });
}

function editRec(nom,unit,sid){
  document.getElementById(`rd-${sid}`).style.display='none';
  document.getElementById(`re-${sid}`).style.display='flex';
  document.getElementById(`ri-${sid}`).focus();
}
function saveRec(nom,unit,sid){
  const v=parseFloat(document.getElementById(`ri-${sid}`).value);
  if(!isNaN(v)){ST.records[nom]=v;saveST();buildProgression();showToast(`🏆 ${v} ${unit} enregistré !`);}
}
function updateParams(){
  const d=document.getElementById('start-date-input').value;
  const p=document.getElementById('prenom-input').value.trim();
  if(d) ST.startDate=d;
  if(p) ST.prenom=p;
  saveST();buildAccueil();showToast('✅ Paramètres mis à jour !');
}

// Mensurations
function getLastMensuration(key){
  if(!ST.mensurations?.length) return '';
  const last=ST.mensurations[ST.mensurations.length-1];
  return last[key]||'';
}
function saveMensurations(){
  const phase=document.getElementById('mensuration-phase').value;
  const entry={date:new Date().toISOString().split('T')[0],phase};
  let hasData=false;
  MENSURATIONS_FIELDS.forEach(f=>{
    const v=parseFloat(document.getElementById('mens-'+f.key).value);
    if(!isNaN(v)&&v>0){entry[f.key]=v;hasData=true;}
  });
  if(!hasData){showToast('⚠️ Remplis au moins une mesure');return;}
  if(!ST.mensurations) ST.mensurations=[];
  ST.mensurations.push(entry);
  saveST();renderMensurationHistory();showToast('📏 Mensurations enregistrées !');
}
function renderMensurationHistory(){
  const el=document.getElementById('mensuration-history');
  if(!ST.mensurations?.length){el.innerHTML='<p style="font-size:13px;color:var(--mid);">Aucune mesure enregistrée. Remplis ton premier bilan !</p>';return;}
  // Grouper par phase
  const phases=['debut','p1-fin','p2-fin','p3-fin','actuel'];
  const phaseLabels={debut:'Début',  'p1-fin':'Fin Phase 1 (S8)','p2-fin':'Fin Phase 2 (S24)','p3-fin':'Fin Phase 3 (S52)','actuel':'Actuel'};
  const byPhase={};
  ST.mensurations.forEach(m=>{if(!byPhase[m.phase])byPhase[m.phase]=[];byPhase[m.phase].push(m);});
  const debut=ST.mensurations.find(m=>m.phase==='debut');

  el.innerHTML='<div class="phase-history">';
  const toShow=Object.entries(byPhase).slice(-3);
  toShow.forEach(([ph,entries])=>{
    const last=entries[entries.length-1];
    let html=`<div class="phase-hist-card"><div class="phase-hist-title">${phaseLabels[ph]||ph}</div>`;
    html+=`<div style="font-size:11px;color:var(--mid);margin-bottom:8px;">${new Date(last.date).toLocaleDateString('fr-FR')}</div>`;
    MENSURATIONS_FIELDS.slice(0,5).forEach(f=>{
      if(!last[f.key]) return;
      const diff=debut&&debut[f.key]?((last[f.key]-debut[f.key])>=0?'+':'')+((last[f.key]-debut[f.key]).toFixed(1)):'';
      const diffColor=f.key==='tour_taille'||f.key==='graisse'?(parseFloat(diff)<=0?'pos':'neg'):(parseFloat(diff)>=0?'pos':'neg');
      html+=`<div style="display:flex;justify-content:space-between;font-size:12px;padding:4px 0;border-bottom:1px dashed var(--border);">
        <span style="color:var(--mid);">${f.label}</span>
        <span style="font-weight:700;">${last[f.key]}${f.unit} ${diff?`<span class="mensuration-diff ${diffColor}">(${diff})</span>`:''}</span>
      </div>`;
    });
    html+='</div>';
    el.innerHTML+=html;
  });
  el.innerHTML+='</div>';
}

// ═══════════════════════════════════════════════════
// EXPORT / IMPORT
// ═══════════════════════════════════════════════════
function exportData(){
  const data = JSON.stringify(ST, null, 2);
  const blob = new Blob([data], {type:'application/json'});
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  const date = new Date().toISOString().split('T')[0];
  a.href = url;
  a.download = `cali-elite-sauvegarde-${date}.json`;
  a.click();
  URL.revokeObjectURL(url);
  showToast('✅ Données exportées ! Garde ce fichier précieusement.');
}
function importData(event){
  const file = event.target.files[0];
  if(!file) return;
  const reader = new FileReader();
  reader.onload = (e) => {
    try {
      const imported = JSON.parse(e.target.result);
      // Vérification minimale
      if(!imported.startDate && !imported.records && !imported.streak && !imported.prenom){
        showToast('⚠️ Fichier invalide — ce n\'est pas un fichier CALI ÉLITE');
        return;
      }
      Object.assign(ST, imported);
      saveST();
      buildAll();
      const status = document.getElementById('import-status');
      status.style.display = 'block';
      status.textContent = `✅ Import réussi ! ${Object.keys(imported.records||{}).length} records, ${(imported.photos||[]).length} photos, ${(imported.mensurations||[]).length} mesures restaurées.`;
      showToast('🎉 Données importées avec succès !');
    } catch(err) {
      showToast('❌ Erreur de lecture du fichier JSON');
    }
  };
  reader.readAsText(file);
  event.target.value = '';
}

function changePinPrompt(){
  const current=prompt('Entre ton PIN actuel :');
  if(current===null) return;
  if(current!==getStoredPin()){showToast('❌ PIN incorrect');return;}
  const newPin=prompt('Nouveau PIN (4 chiffres) :');
  if(!newPin||newPin.length!==4||isNaN(newPin)){showToast('⚠️ PIN invalide — 4 chiffres requis');return;}
  const confirm=prompt('Confirme le nouveau PIN :');
  if(newPin!==confirm){showToast('❌ Les codes ne correspondent pas');return;}
  setStoredPin(newPin);
  showToast('✅ PIN mis à jour !');
}

// ═══════════════════════════════════════════════════
// TOAST
// ═══════════════════════════════════════════════════
function showToast(msg){
  const t=document.getElementById('toast');t.textContent=msg;t.classList.add('show');
  setTimeout(()=>t.classList.remove('show'),2800);
}

// ═══════════════════════════════════════════════════
// INIT
// ═══════════════════════════════════════════════════
function buildAll(){
  document.getElementById('header-date').textContent=new Date().toLocaleDateString('fr-FR',{weekday:'short',day:'numeric',month:'long',year:'numeric'}).toUpperCase();
  buildAccueil();
  buildProgramme();
  buildExos();
  buildNutrition();
  buildPhotos();
  buildProgression();
}

loadST();
buildAll();
</script>

</body>
</html>
