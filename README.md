<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>FoodWell.sniu | Premium Trading & Investment Platform</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Rajdhani:wght@300;400;600;700&family=Inter:wght@300;400;500;600;700&family=Cinzel:wght@400;600;700;900&family=Great+Vibes&family=Playfair+Display:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet"/>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"/>
<style>
:root{
  --gold:#FFD700;--gold2:#FFA500;--gold3:#B8860B;
  --dark:#020810;--dark2:#080F1E;--dark3:#0D1A30;
  --accent:#00C6FF;--accent2:#00FF88;
  --text:#E8F4FF;--muted:#6B8099;
  --card:rgba(255,255,255,0.03);--border:rgba(0,198,255,0.12);
  --red:#FF3E3E;--green:#00FF88;--purple:#9B59B6;
}
*{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{background:var(--dark);color:var(--text);font-family:'Inter',sans-serif;overflow-x:hidden;}
::-webkit-scrollbar{width:5px;}
::-webkit-scrollbar-track{background:var(--dark);}
::-webkit-scrollbar-thumb{background:linear-gradient(var(--accent),var(--gold));border-radius:3px;}
body::before{content:'';position:fixed;top:0;left:0;width:100%;height:100%;
  background:radial-gradient(ellipse at 10% 10%,rgba(0,198,255,0.06) 0%,transparent 55%),
  radial-gradient(ellipse at 90% 90%,rgba(255,215,0,0.05) 0%,transparent 55%),
  radial-gradient(ellipse at 50% 50%,rgba(0,255,136,0.03) 0%,transparent 65%);
  pointer-events:none;z-index:0;}

/* ===== NAVBAR ===== */
nav{position:fixed;top:0;width:100%;z-index:1000;
  background:rgba(2,8,16,0.97);backdrop-filter:blur(25px);
  border-bottom:1px solid var(--border);padding:0 50px;height:72px;
  display:flex;align-items:center;justify-content:space-between;}
.nav-logo{display:flex;align-items:center;gap:14px;text-decoration:none;}
.logo-box{width:46px;height:46px;background:linear-gradient(135deg,var(--accent),var(--gold));
  border-radius:12px;display:flex;align-items:center;justify-content:center;
  font-size:22px;box-shadow:0 0 25px rgba(0,198,255,0.4);}
.logo-name{font-family:'Orbitron',sans-serif;font-size:20px;font-weight:900;
  background:linear-gradient(135deg,var(--accent),var(--gold));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;}
.logo-sub{font-size:10px;color:var(--muted);letter-spacing:3px;text-transform:uppercase;
  font-family:'Rajdhani',sans-serif;display:block;margin-top:-3px;}
.nav-links{display:flex;gap:30px;list-style:none;}
.nav-links a{color:var(--muted);text-decoration:none;font-size:13px;font-family:'Rajdhani',sans-serif;
  font-weight:600;letter-spacing:1.5px;text-transform:uppercase;transition:color 0.3s;position:relative;}
.nav-links a::after{content:'';position:absolute;bottom:-4px;left:0;width:0;height:2px;background:var(--accent);transition:width 0.3s;}
.nav-links a:hover{color:var(--accent);}
.nav-links a:hover::after{width:100%;}
.nav-cta{background:linear-gradient(135deg,var(--accent),#0088BB)!important;
  color:var(--dark)!important;padding:9px 22px;border-radius:7px;font-weight:700!important;}

/* ===== TICKER ===== */
.ticker-top{margin-top:72px;position:relative;z-index:1;}
.t-label{padding:9px 0;text-align:center;font-family:'Orbitron',sans-serif;font-size:10px;
  font-weight:700;letter-spacing:3px;text-transform:uppercase;border-bottom:1px solid var(--border);}

/* ===== HERO ===== */
.hero{min-height:100vh;display:flex;align-items:center;
  padding:100px 50px 80px;position:relative;z-index:1;}
.hero-grid{max-width:1400px;margin:0 auto;display:grid;
  grid-template-columns:1.1fr 0.9fr;gap:70px;align-items:center;width:100%;}
.hero-badge{display:inline-flex;align-items:center;gap:8px;
  background:rgba(0,198,255,0.08);border:1px solid rgba(0,198,255,0.25);
  padding:7px 18px;border-radius:25px;font-size:11px;color:var(--accent);
  letter-spacing:2.5px;text-transform:uppercase;font-family:'Rajdhani',sans-serif;
  font-weight:700;margin-bottom:22px;}
.bdot{width:8px;height:8px;background:var(--accent2);border-radius:50%;animation:blink 1.5s infinite;}
@keyframes blink{0%,100%{opacity:1;transform:scale(1);}50%{opacity:0.4;transform:scale(0.7);}}
.hero h1{font-family:'Orbitron',sans-serif;font-size:54px;font-weight:900;line-height:1.08;margin-bottom:22px;}
.hero h1 span{background:linear-gradient(135deg,var(--accent),var(--gold));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;}
.hero-sub{font-size:11px;color:var(--gold);letter-spacing:4px;text-transform:uppercase;
  font-family:'Rajdhani',sans-serif;font-weight:700;margin-bottom:10px;}
.hero p{font-size:16px;color:var(--muted);line-height:1.9;margin-bottom:38px;max-width:560px;}
.hero-btns{display:flex;gap:16px;flex-wrap:wrap;}
.btn-p{background:linear-gradient(135deg,var(--accent),#0088BB);color:var(--dark);
  padding:15px 34px;border-radius:9px;font-weight:700;font-family:'Rajdhani',sans-serif;
  font-size:14px;letter-spacing:1.5px;text-transform:uppercase;text-decoration:none;
  display:inline-flex;align-items:center;gap:8px;transition:all 0.3s;
  box-shadow:0 5px 22px rgba(0,198,255,0.3);}
.btn-p:hover{transform:translateY(-3px);box-shadow:0 10px 32px rgba(0,198,255,0.5);}
.btn-s{border:1px solid var(--border);color:var(--text);padding:15px 34px;border-radius:9px;
  font-weight:600;font-family:'Rajdhani',sans-serif;font-size:14px;letter-spacing:1.5px;
  text-transform:uppercase;text-decoration:none;display:inline-flex;align-items:center;
  gap:8px;transition:all 0.3s;background:var(--card);}
.btn-s:hover{border-color:var(--accent);color:var(--accent);}
.hero-stats{display:flex;gap:36px;margin-top:50px;padding-top:36px;border-top:1px solid var(--border);}
.sn{font-family:'Orbitron',sans-serif;font-size:28px;font-weight:700;color:var(--accent);}
.sl{font-size:11px;color:var(--muted);text-transform:uppercase;letter-spacing:1.5px;margin-top:4px;}
.hero-right{display:flex;flex-direction:column;gap:13px;}
.hc{background:var(--card);border:1px solid var(--border);border-radius:14px;
  padding:18px 22px;display:flex;align-items:center;justify-content:space-between;
  backdrop-filter:blur(12px);transition:all 0.3s;}
.hc:hover{border-color:var(--accent);transform:translateX(6px);}
.hc-l{display:flex;align-items:center;gap:14px;}
.hi{width:42px;height:42px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:19px;}
.hn{font-weight:700;font-size:14px;font-family:'Rajdhani',sans-serif;}
.hf{font-size:11px;color:var(--muted);}
.hr{text-align:right;}
.hp{font-family:'Orbitron',sans-serif;font-size:15px;font-weight:700;}
.hch{font-size:11px;font-weight:700;padding:3px 9px;border-radius:5px;margin-top:4px;display:inline-block;}
.up{color:var(--green);background:rgba(0,255,136,0.1);}
.dn{color:var(--red);background:rgba(255,62,62,0.1);}

/* ===== BASE ===== */
section{position:relative;z-index:1;}
.container{max-width:1400px;margin:0 auto;padding:0 50px;}
.sh{text-align:center;margin-bottom:65px;}
.stag{display:inline-block;background:rgba(255,215,0,0.08);border:1px solid rgba(255,215,0,0.25);
  color:var(--gold);padding:6px 18px;border-radius:25px;font-size:11px;letter-spacing:2.5px;
  text-transform:uppercase;font-family:'Rajdhani',sans-serif;font-weight:700;margin-bottom:18px;}
.stitle{font-family:'Orbitron',sans-serif;font-size:38px;font-weight:700;margin-bottom:16px;}
.stitle span{background:linear-gradient(135deg,var(--accent),var(--gold));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;}
.ssub{color:var(--muted);font-size:16px;max-width:650px;margin:0 auto;line-height:1.8;}

/* ===== ABOUT ===== */
.about-sec{padding:110px 0;background:linear-gradient(180deg,var(--dark),var(--dark2));}
.ag{display:grid;grid-template-columns:1fr 1fr;gap:70px;align-items:center;}
.ag h2{font-family:'Orbitron',sans-serif;font-size:34px;font-weight:700;margin-bottom:20px;}
.ag h2 span{background:linear-gradient(135deg,var(--accent),var(--gold));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;}
.ag p{color:var(--muted);font-size:15px;line-height:1.9;margin-bottom:16px;}
.atags{display:flex;flex-wrap:wrap;gap:10px;margin-top:26px;}
.atag{background:rgba(0,198,255,0.07);border:1px solid rgba(0,198,255,0.2);color:var(--accent);
  padding:7px 16px;border-radius:7px;font-size:12px;font-family:'Rajdhani',sans-serif;font-weight:700;letter-spacing:1px;}
.aright{display:grid;grid-template-columns:1fr 1fr;gap:18px;}
.asc{background:var(--card);border:1px solid var(--border);border-radius:16px;padding:28px 24px;
  text-align:center;transition:all 0.3s;}
.asc:hover{border-color:var(--gold);transform:translateY(-5px);box-shadow:0 15px 35px rgba(255,215,0,0.08);}
.asn{font-family:'Orbitron',sans-serif;font-size:30px;font-weight:700;
  background:linear-gradient(135deg,var(--accent),var(--gold));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;}
.asl{font-size:12px;color:var(--muted);text-transform:uppercase;letter-spacing:1.5px;
  margin-top:8px;font-family:'Rajdhani',sans-serif;}

/* ===========================
   ✅ CERTIFICATES — REAL LOOK
   =========================== */
.awards-sec{padding:110px 0;
  background:linear-gradient(180deg,var(--dark2) 0%,#0A1020 50%,var(--dark2) 100%);}
.certs-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:36px;}

/* ---- Certificate Card ---- */
.cert-wrap{perspective:1000px;}
.cert{
  position:relative;
  background:linear-gradient(160deg,#FFF8E1 0%,#FFFDE7 30%,#FFF9C4 60%,#FFFDE7 100%);
  border-radius:6px;
  padding:0;
  overflow:hidden;
  transition:transform 0.5s ease,box-shadow 0.5s ease;
  box-shadow:0 10px 40px rgba(0,0,0,0.6),0 2px 8px rgba(255,215,0,0.2);
  cursor:pointer;
}
.cert:hover{
  transform:translateY(-12px) rotateX(3deg);
  box-shadow:0 30px 70px rgba(0,0,0,0.7),0 0 30px rgba(255,215,0,0.25);
}

/* Outer gold border frame */
.cert-frame{
  margin:12px;
  border:3px solid var(--gold3);
  border-radius:3px;
  padding:0;
  position:relative;
}
.cert-frame::before{
  content:'';
  position:absolute;inset:4px;
  border:1px solid rgba(184,134,11,0.4);
  border-radius:2px;
  pointer-events:none;
  z-index:1;
}

/* Corner ornaments */
.cert-corner{position:absolute;width:30px;height:30px;z-index:2;}
.cert-corner.tl{top:-2px;left:-2px;border-top:4px solid var(--gold);border-left:4px solid var(--gold);}
.cert-corner.tr{top:-2px;right:-2px;border-top:4px solid var(--gold);border-right:4px solid var(--gold);}
.cert-corner.bl{bottom:-2px;left:-2px;border-bottom:4px solid var(--gold);border-left:4px solid var(--gold);}
.cert-corner.br{bottom:-2px;right:-2px;border-bottom:4px solid var(--gold);border-right:4px solid var(--gold);}

/* Inner content */
.cert-inner{padding:28px 24px 22px;text-align:center;position:relative;}

/* Top decoration line */
.cert-topline{
  display:flex;align-items:center;gap:8px;justify-content:center;margin-bottom:14px;
}
.cert-topline::before,.cert-topline::after{content:'';flex:1;height:1px;background:linear-gradient(90deg,transparent,var(--gold3));}
.cert-topline::after{background:linear-gradient(90deg,var(--gold3),transparent);}
.cert-topstar{color:var(--gold3);font-size:14px;}

/* Header */
.cert-header-org{
  font-family:'Cinzel',serif;font-size:10px;font-weight:600;
  color:var(--gold3);letter-spacing:3px;text-transform:uppercase;margin-bottom:6px;
}
.cert-of-text{
  font-family:'Cinzel',serif;font-size:18px;font-weight:700;
  color:#4A3000;letter-spacing:2px;margin-bottom:4px;
  text-shadow:0 1px 0 rgba(255,255,255,0.8);
}
.cert-excellence{
  font-family:'Cinzel',serif;font-size:11px;color:var(--gold3);
  letter-spacing:4px;text-transform:uppercase;margin-bottom:16px;
}

/* Divider ornament */
.cert-divider{
  display:flex;align-items:center;gap:6px;justify-content:center;margin:12px 0;
}
.cert-divider-line{flex:1;height:1px;background:linear-gradient(90deg,transparent,rgba(184,134,11,0.5),transparent);}
.cert-divider-diamond{width:8px;height:8px;background:var(--gold3);transform:rotate(45deg);flex-shrink:0;}

/* Seal */
.cert-seal-wrap{margin:14px auto 10px;position:relative;display:inline-block;}
.cert-seal-outer{
  width:80px;height:80px;border-radius:50%;
  background:radial-gradient(circle at 40% 35%,#FFD700,#B8860B 60%,#8B6508 100%);
  display:flex;align-items:center;justify-content:center;
  box-shadow:0 4px 15px rgba(184,134,11,0.5),inset 0 2px 4px rgba(255,255,255,0.3);
  position:relative;
}
.cert-seal-outer::before{
  content:'';position:absolute;inset:4px;border-radius:50%;
  border:2px dashed rgba(255,255,255,0.4);
}
.cert-seal-outer::after{
  content:'★ CERTIFIED ★';
  position:absolute;bottom:-22px;left:50%;transform:translateX(-50%);
  font-family:'Cinzel',serif;font-size:7px;color:var(--gold3);
  white-space:nowrap;letter-spacing:2px;font-weight:700;
}
.cert-seal-icon{font-size:32px;filter:drop-shadow(0 2px 4px rgba(0,0,0,0.3));}

/* Presented to */
.cert-pres{
  font-family:'Playfair Display',serif;font-style:italic;
  font-size:11px;color:#6B5B00;letter-spacing:1px;margin-top:22px;margin-bottom:4px;
}
.cert-name{
  font-family:'Great Vibes',cursive;font-size:32px;
  color:#2C1A00;margin-bottom:4px;
  text-shadow:0 1px 2px rgba(255,255,255,0.6);
}
.cert-company{
  font-family:'Cinzel',serif;font-size:10px;font-weight:600;
  color:var(--gold3);letter-spacing:2px;text-transform:uppercase;margin-bottom:14px;
}

/* Award title */
.cert-award-box{
  background:linear-gradient(135deg,rgba(184,134,11,0.12),rgba(184,134,11,0.06));
  border:1px solid rgba(184,134,11,0.3);
  border-radius:4px;padding:10px 16px;margin:10px 0 16px;
}
.cert-award-label{font-family:'Cinzel',serif;font-size:9px;color:var(--gold3);
  letter-spacing:2px;text-transform:uppercase;margin-bottom:4px;}
.cert-award-title{font-family:'Playfair Display',serif;font-size:13px;font-weight:700;
  color:#3A2500;line-height:1.4;}

/* Footer */
.cert-footer{
  display:flex;justify-content:space-between;align-items:flex-end;
  margin-top:14px;padding-top:12px;
  border-top:1px solid rgba(184,134,11,0.3);
}
.cert-sig{text-align:center;}
.cert-sig-line{width:90px;height:1px;background:rgba(74,48,0,0.4);margin:0 auto 4px;}
.cert-sig-name{font-family:'Great Vibes',cursive;font-size:16px;color:#4A3000;}
.cert-sig-role{font-family:'Cinzel',serif;font-size:8px;color:var(--gold3);
  letter-spacing:1.5px;text-transform:uppercase;}
.cert-id{text-align:right;}
.cert-id-num{font-family:'Orbitron',sans-serif;font-size:9px;color:rgba(74,48,0,0.5);}
.cert-year-badge{
  background:linear-gradient(135deg,var(--gold),var(--gold2));
  color:#2C1A00;font-family:'Cinzel',serif;font-size:11px;font-weight:700;
  padding:4px 12px;border-radius:3px;letter-spacing:2px;display:inline-block;margin-top:8px;
}

/* Bottom gold strip */
.cert-bottom-strip{
  height:8px;
  background:linear-gradient(90deg,var(--gold3),var(--gold),#FFF8E1,var(--gold),var(--gold3));
}

/* Hologram sticker */
.cert-holo{
  position:absolute;top:20px;right:20px;
  width:44px;height:44px;border-radius:50%;
  background:conic-gradient(#FF0000,#FF7700,#FFFF00,#00FF00,#0000FF,#8B00FF,#FF0000);
  opacity:0.6;
  box-shadow:0 0 8px rgba(255,255,255,0.4);
  display:flex;align-items:center;justify-content:center;
  font-size:16px;
}

/* ===== CHARTS ===== */
.charts-sec{padding:110px 0;}
.ctabs{display:flex;gap:10px;flex-wrap:wrap;justify-content:center;margin-bottom:40px;}
.tab-btn{background:var(--card);border:1px solid var(--border);color:var(--muted);
  padding:9px 22px;border-radius:7px;font-family:'Rajdhani',sans-serif;font-weight:700;
  font-size:13px;letter-spacing:1.5px;text-transform:uppercase;cursor:pointer;transition:all 0.3s;}
.tab-btn.active,.tab-btn:hover{background:rgba(0,198,255,0.1);border-color:var(--accent);color:var(--accent);}
.cpanel{display:none;}
.cpanel.active{display:block;animation:fadeUp 0.5s ease;}
@keyframes fadeUp{from{opacity:0;transform:translateY(12px);}to{opacity:1;transform:translateY(0);}}
.cbox{background:var(--card);border:1px solid var(--border);border-radius:18px;overflow:hidden;padding:22px;}
.chd{display:flex;align-items:center;justify-content:space-between;margin-bottom:18px;}
.chl{display:flex;align-items:center;gap:14px;}
.chico{width:38px;height:38px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:20px;}
.chtit{font-family:'Orbitron',sans-serif;font-size:16px;font-weight:700;}
.chsub{font-size:12px;color:var(--muted);}
.lbadge{display:flex;align-items:center;gap:6px;background:rgba(0,255,136,0.1);
  border:1px solid rgba(0,255,136,0.3);padding:5px 14px;border-radius:20px;
  font-size:12px;color:var(--green);font-family:'Rajdhani',sans-serif;font-weight:700;}
.ld{width:8px;height:8px;background:var(--green);border-radius:50%;animation:blink 1.5s infinite;}
.mgrid{display:grid;grid-template-columns:repeat(3,1fr);gap:22px;margin-top:44px;}
.mcard{background:var(--card);border:1px solid var(--border);border-radius:16px;overflow:hidden;transition:all 0.3s;}
.mcard:hover{border-color:var(--accent);box-shadow:0 0 22px rgba(0,198,255,0.1);}
.mhd{padding:16px 20px;display:flex;align-items:center;justify-content:space-between;border-bottom:1px solid var(--border);}
.ml{display:flex;align-items:center;gap:10px;}
.mico{width:34px;height:34px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:17px;}
.mn{font-weight:700;font-size:13px;font-family:'Rajdhani',sans-serif;}
.mf{font-size:11px;color:var(--muted);}

/* ===== MARKET OVERVIEW ===== */
.mkt-sec{padding:110px 0;background:linear-gradient(180deg,var(--dark),var(--dark2));}

/* ===== TEAM ===== */
.team-sec{padding:110px 0;background:linear-gradient(180deg,var(--dark2),var(--dark3));}
.team-top{display:flex;justify-content:center;gap:80px;margin-bottom:50px;flex-wrap:wrap;}
.tc{background:var(--card);border:1px solid var(--border);border-radius:20px;
  padding:32px 28px;text-align:center;transition:all 0.4s;position:relative;
  overflow:hidden;min-width:220px;max-width:260px;}
.tc::before{content:'';position:absolute;top:0;left:50%;transform:translateX(-50%);
  width:60%;height:3px;background:linear-gradient(90deg,transparent,var(--accent),transparent);}
.tc.ceo::before{background:linear-gradient(90deg,transparent,var(--gold),transparent);}
.tc.mod::before{background:linear-gradient(90deg,transparent,var(--purple),transparent);}
.tc:hover{transform:translateY(-8px);}
.tav{width:80px;height:80px;border-radius:50%;display:flex;align-items:center;justify-content:center;
  font-size:30px;margin:0 auto 18px;
  background:linear-gradient(135deg,rgba(0,198,255,0.15),rgba(0,198,255,0.05));
  border:2px solid rgba(0,198,255,0.25);position:relative;}
.ceo .tav{background:linear-gradient(135deg,rgba(255,215,0,0.15),rgba(255,165,0,0.05));border-color:rgba(255,215,0,0.3);}
.mod .tav{background:linear-gradient(135deg,rgba(155,89,182,0.15),rgba(155,89,182,0.05));border-color:rgba(155,89,182,0.3);}
.tav-ring{position:absolute;inset:-5px;border-radius:50%;border:1px solid rgba(0,198,255,0.1);}
.tname{font-family:'Orbitron',sans-serif;font-size:14px;font-weight:700;margin-bottom:6px;}
.trole{font-size:12px;color:var(--accent);font-family:'Rajdhani',sans-serif;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;margin-bottom:8px;}
.ceo .trole{color:var(--gold);}
.mod .trole{color:var(--purple);}
.tbadge{display:inline-block;background:rgba(0,198,255,0.08);border:1px solid rgba(0,198,255,0.2);
  color:var(--muted);padding:4px 12px;border-radius:5px;font-size:11px;
  font-family:'Rajdhani',sans-serif;font-weight:600;letter-spacing:1px;margin-top:6px;}
.ceo .tbadge{background:rgba(255,215,0,0.06);border-color:rgba(255,215,0,0.2);color:var(--gold2);}
.mod .tbadge{background:rgba(155,89,182,0.08);border-color:rgba(155,89,182,0.2);color:var(--purple);}
.tdesc{font-size:12px;color:var(--muted);margin-top:10px;line-height:1.6;}
.tsoc{display:flex;gap:8px;justify-content:center;margin-top:14px;}
.tsoc a{color:var(--muted);font-size:15px;transition:color 0.3s;}
.tsoc a:hover{color:var(--accent);}
.ceo .tsoc a:hover{color:var(--gold);}
.mod .tsoc a:hover{color:var(--purple);}

/* Branch team */
.team-branch{display:flex;justify-content:center;gap:40px;flex-wrap:wrap;}
.branch-group{display:flex;flex-direction:column;align-items:center;}
.branch-title{font-family:'Rajdhani',sans-serif;font-size:12px;color:var(--muted);
  letter-spacing:3px;text-transform:uppercase;margin-bottom:16px;text-align:center;}
.branch-line{width:2px;height:36px;margin:0 auto;background:linear-gradient(var(--border),var(--accent));}
.sub-grid{display:flex;gap:18px;flex-wrap:wrap;justify-content:center;}
.stc{background:var(--card);border:1px solid var(--border);border-radius:16px;
  padding:22px 18px;text-align:center;transition:all 0.3s;max-width:175px;}
.stc:hover{transform:translateY(-6px);border-color:rgba(0,198,255,0.3);}
.stav{width:60px;height:60px;border-radius:50%;display:flex;align-items:center;justify-content:center;
  font-size:26px;margin:0 auto 14px;
  background:linear-gradient(135deg,rgba(0,198,255,0.1),rgba(0,198,255,0.03));
  border:2px solid rgba(0,198,255,0.15);}
.stn{font-family:'Orbitron',sans-serif;font-size:13px;font-weight:700;margin-bottom:5px;}
.str{font-size:11px;color:var(--accent);font-family:'Rajdhani',sans-serif;font-weight:700;letter-spacing:1px;text-transform:uppercase;margin-bottom:6px;}
.stb{display:inline-block;background:rgba(0,198,255,0.06);border:1px solid rgba(0,198,255,0.15);
  color:var(--muted);padding:3px 10px;border-radius:5px;font-size:10px;
  font-family:'Rajdhani',sans-serif;font-weight:600;}
.std{font-size:11px;color:var(--muted);margin-top:8px;line-height:1.6;}

/* Private sec */
.priv-wrap{display:flex;flex-direction:column;align-items:center;margin-top:8px;}
.priv-line{width:2px;height:36px;background:linear-gradient(var(--gold),var(--border));}
.priv-card{background:linear-gradient(135deg,rgba(255,215,0,0.05),rgba(255,165,0,0.02));
  border:1px solid rgba(255,215,0,0.2);border-radius:16px;padding:22px 20px;
  text-align:center;max-width:200px;transition:all 0.3s;}
.priv-card:hover{border-color:rgba(255,215,0,0.4);transform:translateY(-5px);}

/* ===== FEATURES ===== */
.feat-sec{padding:110px 0;background:linear-gradient(180deg,var(--dark3),var(--dark));}
.fgrid{display:grid;grid-template-columns:repeat(3,1fr);gap:26px;}
.fc{background:var(--card);border:1px solid var(--border);border-radius:18px;
  padding:34px;transition:all 0.3s;position:relative;overflow:hidden;}
.fc::after{content:'';position:absolute;bottom:0;left:0;width:100%;height:3px;
  background:linear-gradient(90deg,var(--accent),var(--gold));transform:scaleX(0);transition:transform 0.3s;}
.fc:hover::after{transform:scaleX(1);}
.fc:hover{border-color:rgba(0,198,255,0.3);transform:translateY(-6px);}
.fi{width:58px;height:58px;background:linear-gradient(135deg,rgba(0,198,255,0.12),rgba(0,198,255,0.04));
  border:1px solid rgba(0,198,255,0.18);border-radius:15px;display:flex;align-items:center;
  justify-content:center;font-size:26px;margin-bottom:22px;}
.ft{font-family:'Rajdhani',sans-serif;font-size:18px;font-weight:700;margin-bottom:12px;}
.fd{font-size:14px;color:var(--muted);line-height:1.8;}

/* ===== CONTACT ===== */
.contact-sec{padding:110px 0;background:linear-gradient(180deg,var(--dark),var(--dark2));}
.cgrid{display:grid;grid-template-columns:1fr 1fr;gap:65px;align-items:start;}
.ci h3{font-family:'Orbitron',sans-serif;font-size:28px;font-weight:700;margin-bottom:18px;line-height:1.3;}
.ci p{color:var(--muted);font-size:15px;line-height:1.9;margin-bottom:32px;}
.citem{display:flex;align-items:center;gap:16px;padding:17px 22px;background:var(--card);
  border:1px solid var(--border);border-radius:14px;margin-bottom:12px;text-decoration:none;transition:all 0.3s;}
.citem:hover{border-color:var(--accent);background:rgba(0,198,255,0.04);}
.cico{width:44px;height:44px;background:rgba(0,198,255,0.1);border-radius:11px;
  display:flex;align-items:center;justify-content:center;color:var(--accent);font-size:19px;flex-shrink:0;}
.clabel{font-size:11px;color:var(--muted);text-transform:uppercase;letter-spacing:1.5px;font-family:'Rajdhani',sans-serif;}
.cval{color:var(--text);font-weight:500;font-size:14px;margin-top:2px;}
.cform{background:var(--card);border:1px solid var(--border);border-radius:22px;
  padding:44px;backdrop-filter:blur(12px);}
.cform h4{font-family:'Orbitron',sans-serif;font-size:18px;font-weight:700;margin-bottom:28px;color:var(--accent);}
.frow{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
.fgrp{margin-bottom:18px;}
.fgrp label{display:block;font-size:12px;color:var(--muted);margin-bottom:8px;
  font-family:'Rajdhani',sans-serif;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;}
.fgrp input,.fgrp select,.fgrp textarea{width:100%;background:rgba(255,255,255,0.03);
  border:1px solid var(--border);border-radius:9px;padding:13px 17px;color:var(--text);
  font-size:14px;font-family:'Inter',sans-serif;transition:border-color 0.3s;outline:none;}
.fgrp input:focus,.fgrp select:focus,.fgrp textarea:focus{border-color:var(--accent);}
.fgrp select option{background:var(--dark2);}
.fgrp textarea{resize:vertical;min-height:100px;}
.fsub{width:100%;background:linear-gradient(135deg,var(--accent),#0088BB);color:var(--dark);
  border:none;padding:15px;border-radius:9px;font-weight:700;font-family:'Rajdhani',sans-serif;
  font-size:16px;letter-spacing:2px;text-transform:uppercase;cursor:pointer;transition:all 0.3s;
  display:flex;align-items:center;justify-content:center;gap:8px;}
.fsub:hover{transform:translateY(-2px);box-shadow:0 10px 28px rgba(0,198,255,0.4);}

/* ===== FOOTER ===== */
footer{background:var(--dark2);border-top:1px solid var(--border);padding:65px 50px 30px;}
.fgridf{max-width:1400px;margin:0 auto;display:grid;
  grid-template-columns:2.2fr 1fr 1fr 1fr;gap:44px;margin-bottom:44px;}
.fbrand p{color:var(--muted);font-size:14px;line-height:1.9;margin:18px 0 26px;}
.fsoc{display:flex;gap:10px;}
.sb{width:40px;height:40px;border-radius:9px;border:1px solid var(--border);
  background:var(--card);display:flex;align-items:center;justify-content:center;
  color:var(--muted);font-size:17px;text-decoration:none;transition:all 0.3s;}
.sb:hover{border-color:var(--accent);color:var(--accent);background:rgba(0,198,255,0.08);}
.fcol h5{font-family:'Rajdhani',sans-serif;font-weight:700;font-size:13px;letter-spacing:2.5px;
  text-transform:uppercase;color:var(--text);margin-bottom:22px;}
.fcol ul{list-style:none;}
.fcol ul li{margin-bottom:11px;}
.fcol ul li a{color:var(--muted);text-decoration:none;font-size:14px;transition:color 0.3s;}
.fcol ul li a:hover{color:var(--accent);}
.fbot{max-width:1400px;margin:0 auto;padding-top:30px;border-top:1px solid var(--border);
  display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:16px;}
.fbot p{color:var(--muted);font-size:13px;}
.fblinks{display:flex;gap:22px;}
.fblinks a{color:var(--muted);text-decoration:none;font-size:13px;transition:color 0.3s;}
.fblinks a:hover{color:var(--accent);}
.disc{background:rgba(255,165,0,0.04);border:1px solid rgba(255,165,0,0.18);
  border-radius:12px;padding:16px 22px;max-width:1400px;margin:22px auto;
  font-size:12px;color:var(--muted);display:flex;gap:12px;align-items:flex-start;line-height:1.8;}
.disc i{color:#FFA500;margin-top:3px;flex-shrink:0;}

/* ===== RESPONSIVE ===== */
@media(max-width:1100px){
  .hero-grid{grid-template-columns:1fr;}
  .ag{grid-template-columns:1fr;}
  .cgrid{grid-template-columns:1fr;}
  .certs-grid{grid-template-columns:repeat(2,1fr);}
  .mgrid{grid-template-columns:repeat(2,1fr);}
  .fgrid{grid-template-columns:repeat(2,1fr);}
  .fgridf{grid-template-columns:1fr 1fr;}
}
@media(max-width:768px){
  nav{padding:0 20px;}
  .nav-links{display:none;}
  .hero{padding:90px 20px 60px;}
  .hero h1{font-size:34px;}
  .container{padding:0 20px;}
  .certs-grid{grid-template-columns:1fr;}
  .mgrid{grid-template-columns:1fr;}
  .fgrid{grid-template-columns:1fr;}
  .frow{grid-template-columns:1fr;}
  .fgridf{grid-template-columns:1fr;}
  .team-top{flex-direction:column;align-items:center;}
  .sub-grid{flex-direction:column;align-items:center;}
}
</style>
</head>
<body>

<!-- ===== NAVBAR ===== -->
<nav>
  <a href="#" class="nav-logo">
    <div class="logo-box">🍃</div>
    <div>
      <div class="logo-name">FoodWell.sniu</div>
      <span class="logo-sub">Premium Trading & Investment</span>
    </div>
  </a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#markets">Markets</a></li>
    <li><a href="#charts">Charts</a></li>
    <li><a href="#awards">Awards</a></li>
    <li><a href="#team">Team</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#contact" class="nav-cta">Get Started</a></li>
  </ul>
</nav>

<!-- ===== TICKER SECTION ===== -->
<div class="ticker-top" id="markets">

  <!-- CRYPTO TOP 5 -->
  <div style="background:rgba(247,147,26,0.04);border-bottom:1px solid var(--border);padding:5px 0 2px;">
    <div class="t-label" style="color:#F7931A;border:none;padding:4px 0;">₿ TOP 5 CRYPTO LIVE</div>
    <div class="tradingview-widget-container">
      <div class="tradingview-widget-container__widget"></div>
      <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-ticker-tape.js" async>
      {"symbols":[{"proName":"BINANCE:BTCUSDT","title":"Bitcoin"},{"proName":"BINANCE:ETHUSDT","title":"Ethereum"},{"proName":"BINANCE:BNBUSDT","title":"BNB"},{"proName":"BINANCE:SOLUSDT","title":"Solana"},{"proName":"BINANCE:XRPUSDT","title":"XRP"}],"showSymbolLogo":true,"colorTheme":"dark","isTransparent":true,"displayMode":"adaptive","locale":"en"}
      </script>
    </div>
  </div>

  <!-- FOREX TOP 5 -->
  <div style="background:rgba(0,198,255,0.03);border-bottom:1px solid var(--border);padding:5px 0 2px;">
    <div class="t-label" style="color:#00C6FF;border:none;padding:4px 0;">💱 TOP 5 FOREX LIVE</div>
    <div class="tradingview-widget-container">
      <div class="tradingview-widget-container__widget"></div>
      <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-ticker-tape.js" async>
      {"symbols":[{"proName":"FX:EURUSD","title":"EUR/USD"},{"proName":"FX:GBPUSD","title":"GBP/USD"},{"proName":"FX:USDJPY","title":"USD/JPY"},{"proName":"FX:AUDUSD","title":"AUD/USD"},{"proName":"FX:USDCHF","title":"USD/CHF"}],"showSymbolLogo":true,"colorTheme":"dark","isTransparent":true,"displayMode":"adaptive","locale":"en"}
      </script>
    </div>
  </div>

  <!-- COMMODITY TOP 5 -->
  <div style="background:rgba(255,215,0,0.03);border-bottom:1px solid var(--border);padding:5px 0 2px;">
    <div class="t-label" style="color:#FFD700;border:none;padding:4px 0;">🏅 TOP 5 COMMODITIES LIVE</div>
    <div class="tradingview-widget-container">
      <div class="tradingview-widget-container__widget"></div>
      <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-ticker-tape.js" async>
      {"symbols":[{"proName":"TVC:GOLD","title":"Gold"},{"proName":"TVC:SILVER","title":"Silver"},{"proName":"NYMEX:CL1!","title":"Crude Oil"},{"proName":"NYMEX:NG1!","title":"Natural Gas"},{"proName":"CBOT:ZW1!","title":"Wheat"}],"showSymbolLogo":true,"colorTheme":"dark","isTransparent":true,"displayMode":"adaptive","locale":"en"}
      </script>
    </div>
  </div>

  <!-- INDIA TOP 5 -->
  <div style="background:rgba(255,153,0,0.03);border-bottom:1px solid var(--border);padding:5px 0 2px;">
    <div class="t-label" style="color:#FF9900;border:none;padding:4px 0;">🇮🇳 TOP 5 INDIA MARKETS LIVE</div>
    <div class="tradingview-widget-container">
      <div class="tradingview-widget-container__widget"></div>
      <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-ticker-tape.js" async>
      {"symbols":[{"proName":"NSE:NIFTY","title":"NIFTY 50"},{"proName":"BSE:SENSEX","title":"SENSEX"},{"proName":"NSE:RELIANCE","title":"Reliance"},{"proName":"NSE:TCS","title":"TCS"},{"proName":"NSE:HDFCBANK","title":"HDFC Bank"}],"showSymbolLogo":true,"colorTheme":"dark","isTransparent":true,"displayMode":"adaptive","locale":"en"}
      </script>
    </div>
  </div>

  <!-- GOVT BONDS TOP 5 -->
  <div style="background:rgba(0,255,136,0.03);border-bottom:1px solid var(--border);padding:5px 0 2px;">
    <div class="t-label" style="color:#00FF88;border:none;padding:4px 0;">📜 TOP 5 GOVERNMENT BONDS LIVE</div>
    <div class="tradingview-widget-container">
      <div class="tradingview-widget-container__widget"></div>
      <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-ticker-tape.js" async>
      {"symbols":[{"proName":"TVC:US10Y","title":"US 10Y Bond"},{"proName":"TVC:US02Y","title":"US 2Y Bond"},{"proName":"TVC:US30Y","title":"US 30Y Bond"},{"proName":"TVC:IN10Y","title":"India 10Y Bond"},{"proName":"TVC:DE10Y","title":"Germany 10Y Bond"}],"showSymbolLogo":true,"colorTheme":"dark","isTransparent":true,"displayMode":"adaptive","locale":"en"}
      </script>
    </div>
  </div>
</div>

<!-- ===== HERO ===== -->
<section class="hero">
  <div class="hero-grid">
    <div>
      <div class="hero-badge"><div class="bdot"></div>Live Markets • Real-Time Intelligence</div>
      <div class="hero-sub">FoodWell.sniu — Global Premium Trading Hub</div>
      <h1>Invest Smarter.<br/>Trade <span>With Precision.</span></h1>
      <p>FoodWell.sniu is a next-generation premium trading and investment platform delivering real-time market intelligence across Crypto, Forex, Commodities, Indian Equities, and Government Bonds — powered by AI and institutional-grade analytics.</p>
      <div class="hero-btns">
        <a href="#charts" class="btn-p"><i class="fas fa-chart-line"></i>Live Charts</a>
        <a href="#about" class="btn-s"><i class="fas fa-info-circle"></i>About Us</a>
      </div>
      <div class="hero-stats">
        <div><div class="sn">75K+</div><div class="sl">Active Traders</div></div>
        <div><div class="sn">$5.2B+</div><div class="sl">Volume Traded</div></div>
        <div><div class="sn">98.9%</div><div class="sl">Uptime</div></div>
        <div><div class="sn">9</div><div class="sl">Awards Won</div></div>
      </div>
    </div>
    <div class="hero-right">
      <div class="hc">
        <div class="hc-l"><div class="hi" style="background:rgba(247,147,26,0.15);">₿</div><div><div class="hn">BTC/USDT</div><div class="hf">Bitcoin</div></div></div>
        <div class="hr"><div class="hp" style="color:#F7931A;">$67,420</div><div class="hch up">▲ +2.34%</div></div>
      </div>
      <div class="hc">
        <div class="hc-l"><div class="hi" style="background:rgba(0,198,255,0.15);">💱</div><div><div class="hn">EUR/USD</div><div class="hf">Forex Major</div></div></div>
        <div class="hr"><div class="hp" style="color:var(--accent);">1.0842</div><div class="hch dn">▼ -0.18%</div></div>
      </div>
      <div class="hc">
        <div class="hc-l"><div class="hi" style="background:rgba(255,215,0,0.15);">🥇</div><div><div class="hn">GOLD</div><div class="hf">XAU/USD</div></div></div>
        <div class="hr"><div class="hp" style="color:#FFD700;">$2,341</div><div class="hch up">▲ +0.74%</div></div>
      </div>
      <div class="hc">
        <div class="hc-l"><div class="hi" style="background:rgba(255,153,0,0.15);">🇮🇳</div><div><div class="hn">NIFTY 50</div><div class="hf">NSE India</div></div></div>
        <div class="hr"><div class="hp" style="color:#FF9900;">22,450</div><div class="hch up">▲ +1.02%</div></div>
      </div>
      <div class="hc">
        <div class="hc-l"><div class="hi" style="background:rgba(0,255,136,0.12);">📜</div><div><div class="hn">US 10Y Bond</div><div class="hf">Treasury Yield</div></div></div>
        <div class="hr"><div class="hp" style="color:var(--green);">4.52%</div><div class="hch dn">▼ -0.03%</div></div>
      </div>
    </div>
  </div>
</section>

<!-- ===== ABOUT ===== -->
<section class="about-sec" id="about">
  <div class="container">
    <div class="ag">
      <div>
        <div class="stag">🍃 About FoodWell.sniu</div>
        <h2>Building the Future of <span>Premium Trading</span></h2>
        <p>FoodWell.sniu was founded with a singular vision — to democratize access to professional-grade trading tools and financial intelligence for every investor, from retail traders to institutional participants.</p>
        <p>Our platform integrates real-time data feeds, AI-powered analytics, hedge fund-grade research, and a curated team of market specialists who collectively bring decades of trading experience across all major asset classes.</p>
        <p>Under the strategic leadership of <strong style="color:var(--gold);">Founder & CEO Sumit Mauryan</strong> and <strong style="color:var(--purple);">Co-Founder & MOD Hasnain Ansari</strong>, FoodWell.sniu has grown into a trusted name in global markets — empowering traders with the edge they deserve.</p>
        <div class="atags">
          <span class="atag">Crypto Trading</span><span class="atag">Forex Markets</span>
          <span class="atag">Gold & Silver</span><span class="atag">Hedge Funds</span>
          <span class="atag">Gov Bonds</span><span class="atag">Indian Equities</span>
          <span class="atag">AI Signals</span><span class="atag">Risk Management</span>
        </div>
      </div>
      <div class="aright">
        <div class="asc"><div class="asn">75K+</div><div class="asl">Active Traders</div></div>
        <div class="asc"><div class="asn">$5.2B+</div><div class="asl">Total Volume</div></div>
        <div class="asc"><div class="asn">42+</div><div class="asl">Countries</div></div>
        <div class="asc"><div class="asn">99.1%</div><div class="asl">Satisfaction</div></div>
        <div class="asc"><div class="asn">150+</div><div class="asl">Trading Pairs</div></div>
        <div class="asc"><div class="asn">24/7</div><div class="asl">Live Support</div></div>
      </div>
    </div>
  </div>
</section>

<!-- ===== CERTIFICATES ===== -->
<section class="awards-sec" id="awards">
  <div class="container">
    <div class="sh">
      <div class="stag">🏆 Awards & Recognition</div>
      <h2 class="stitle">Our <span>Certificates of Excellence</span></h2>
      <p class="ssub">FoodWell.sniu has been recognized by the world's leading financial and trading organizations with official certificates of excellence, merit, and achievement.</p>
    </div>

    <div class="certs-grid">

      <!-- CERT 1 -->
      <div class="cert-wrap">
        <div class="cert">
          <div class="cert-frame">
            <div class="cert-corner tl"></div><div class="cert-corner tr"></div>
            <div class="cert-corner bl"></div><div class="cert-corner br"></div>
            <div class="cert-inner">
              <div class="cert-holo">🏅</div>
              <div class="cert-topline"><span class="cert-topstar">✦</span><span style="font-family:'Cinzel',serif;font-size:9px;color:#8B6508;letter-spacing:3px;">GLOBAL FINTECH SUMMIT</span><span class="cert-topstar">✦</span></div>
              <div class="cert-of-text">Certificate</div>
              <div class="cert-excellence">of Excellence</div>
              <div class="cert-divider"><div class="cert-divider-line"></div><div class="cert-divider-diamond"></div><div class="cert-divider-line"></div></div>
              <div class="cert-seal-wrap">
                <div class="cert-seal-outer"><div class="cert-seal-icon">🏆</div></div>
              </div>
              <div class="cert-pres">This certificate is proudly presented to</div>
              <div class="cert-name">FoodWell.sniu</div>
              <div class="cert-company">Founded by Sumit Mauryan</div>
              <div class="cert-award-box">
                <div class="cert-award-label">For Outstanding Achievement In</div>
                <div class="cert-award-title">Best Premium Crypto Trading Platform of the Year</div>
              </div>
              <div class="cert-year-badge">2024</div>
              <div class="cert-footer">
                <div class="cert-sig"><div class="cert-sig-line"></div><div class="cert-sig-name">Sumit Mauryan</div><div class="cert-sig-role">Founder & CEO</div></div>
                <div class="cert-id"><div class="cert-id-num">CERT#GFS-2024-001</div><div style="font-family:'Cinzel',serif;font-size:8px;color:rgba(74,48,0,0.5);margin-top:4px;">Global FinTech Summit</div></div>
              </div>
            </div>
          </div>
          <div class="cert-bottom-strip"></div>
        </div>
      </div>

      <!-- CERT 2 -->
      <div class="cert-wrap">
        <div class="cert">
          <div class="cert-frame">
            <div class="cert-corner tl"></div><div class="cert-corner tr"></div>
            <div class="cert-corner bl"></div><div class="cert-corner br"></div>
            <div class="cert-inner">
              <div class="cert-holo">⭐</div>
              <div class="cert-topline"><span class="cert-topstar">✦</span><span style="font-family:'Cinzel',serif;font-size:9px;color:#8B6508;letter-spacing:3px;">TRADEX INTERNATIONAL</span><span class="cert-topstar">✦</span></div>
              <div class="cert-of-text">Certificate</div>
              <div class="cert-excellence">of Achievement</div>
              <div class="cert-divider"><div class="cert-divider-line"></div><div class="cert-divider-diamond"></div><div class="cert-divider-line"></div></div>
              <div class="cert-seal-wrap">
                <div class="cert-seal-outer"><div class="cert-seal-icon">🥇</div></div>
              </div>
              <div class="cert-pres">This certificate is proudly presented to</div>
              <div class="cert-name">FoodWell.sniu</div>
              <div class="cert-company">Co-Founded by Hasnain Ansari</div>
              <div class="cert-award-box">
                <div class="cert-award-label">For Outstanding Achievement In</div>
                <div class="cert-award-title">Most Innovative Trading Technology of the Year</div>
              </div>
              <div class="cert-year-badge">2024</div>
              <div class="cert-footer">
                <div class="cert-sig"><div class="cert-sig-line"></div><div class="cert-sig-name">Hasnain Ansari</div><div class="cert-sig-role">Co-Founder & MOD</div></div>
                <div class="cert-id"><div class="cert-id-num">CERT#TRX-2024-002</div><div style="font-family:'Cinzel',serif;font-size:8px;color:rgba(74,48,0,0.5);margin-top:4px;">TradEx International</div></div>
              </div>
            </div>
          </div>
          <div class="cert-bottom-strip"></div>
        </div>
      </div>

      <!-- CERT 3 -->
      <div class="cert-wrap">
        <div class="cert">
          <div class="cert-frame">
            <div class="cert-corner tl"></div><div class="cert-corner tr"></div>
            <div class="cert-corner bl"></div><div class="cert-corner br"></div>
            <div class="cert-inner">
              <div class="cert-holo">💎</div>
              <div class="cert-topline"><span class="cert-topstar">✦</span><span style="font-family:'Cinzel',serif;font-size:9px;color:#8B6508;letter-spacing:3px;">BLOOMBERG FINANCE AWARDS</span><span class="cert-topstar">✦</span></div>
              <div class="cert-of-text">Certificate</div>
              <div class="cert-excellence">of Merit</div>
              <div class="cert-divider"><div class="cert-divider-line"></div><div class="cert-divider-diamond"></div><div class="cert-divider-line"></div></div>
              <div class="cert-seal-wrap">
                <div class="cert-seal-outer"><div class="cert-seal-icon">💎</div></div>
              </div>
              <div class="cert-pres">This certificate is proudly presented to</div>
              <div class="cert-name">FoodWell.sniu</div>
              <div class="cert-company">Trading & Analytics Division</div>
              <div class="cert-award-box">
                <div class="cert-award-label">For Outstanding Achievement In</div>
                <div class="cert-award-title">Excellence in Market Analytics & Research</div>
              </div>
              <div class="cert-year-badge">2024</div>
              <div class="cert-footer">
                <div class="cert-sig"><div class="cert-sig-line"></div><div class="cert-sig-name">Sumit Mauryan</div><div class="cert-sig-role">Founder & CEO</div></div>
                <div class="cert-id"><div class="cert-id-num">CERT#BLM-2024-003</div><div style="font-family:'Cinzel',serif;font-size:8px;color:rgba(74,48,0,0.5);margin-top:4px;">Bloomberg Finance</div></div>
              </div>
            </div>
          </div>
          <div class="cert-bottom-strip"></div>
        </div>
      </div>

      <!-- CERT 4 -->
      <div class="cert-wrap">
        <div class="cert">
          <div class="cert-frame">
            <div class="cert-corner tl"></div><div class="cert-corner tr"></div>
            <div class="cert-corner bl"></div><div class="cert-corner br"></div>
            <div class="cert-inner">
              <div class="cert-holo">🔱</div>
              <div class="cert-topline"><span class="cert-topstar">✦</span><span style="font-family:'Cinzel',serif;font-size:9px;color:#8B6508;letter-spacing:3px;">CRYPTO EXCELLENCE AWARDS</span><span class="cert-topstar">✦</span></div>
              <div class="cert-of-text">Certificate</div>
              <div class="cert-excellence">of Excellence</div>
              <div class="cert-divider"><div class="cert-divider-line"></div><div class="cert-divider-diamond"></div><div class="cert-divider-line"></div></div>
              <div class="cert-seal-wrap">
                <div class="cert-seal-outer"><div class="cert-seal-icon">⭐</div></div>
              </div>
              <div class="cert-pres">This certificate is proudly presented to</div>
              <div class="cert-name">FoodWell.sniu</div>
              <div class="cert-company">Hedge Fund & Derivatives Desk</div>
              <div class="cert-award-box">
                <div class="cert-award-label">For Outstanding Achievement In</div>
                <div class="cert-award-title">Top Derivatives & Hedge Fund Platform</div>
              </div>
              <div class="cert-year-badge">2023</div>
              <div class="cert-footer">
                <div class="cert-sig"><div class="cert-sig-line"></div><div class="cert-sig-name">Hasnain Ansari</div><div class="cert-sig-role">Co-Founder & MOD</div></div>
                <div class="cert-id"><div class="cert-id-num">CERT#CEA-2023-004</div><div style="font-family:'Cinzel',serif;font-size:8px;color:rgba(74,48,0,0.5);margin-top:4px;">Crypto Excellence Awards</div></div>
              </div>
            </div>
          </div>
          <div class="cert-bottom-strip"></div>
        </div>
      </div>

      <!-- CERT 5 -->
      <div class="cert-wrap">
        <div class="cert">
          <div class="cert-frame">
            <div class="cert-corner tl"></div><div class="cert-corner tr"></div>
            <div class="cert-corner bl"></div><div class="cert-corner br"></div>
            <div class="cert-inner">
              <div class="cert-holo">🎖️</div>
              <div class="cert-topline"><span class="cert-topstar">✦</span><span style="font-family:'Cinzel',serif;font-size:9px;color:#8B6508;letter-spacing:3px;">FX INTELLIGENCE FORUM</span><span class="cert-topstar">✦</span></div>
              <div class="cert-of-text">Certificate</div>
              <div class="cert-excellence">of Honor</div>
              <div class="cert-divider"><div class="cert-divider-line"></div><div class="cert-divider-diamond"></div><div class="cert-divider-line"></div></div>
              <div class="cert-seal-wrap">
                <div class="cert-seal-outer"><div class="cert-seal-icon">🎖️</div></div>
              </div>
              <div class="cert-pres">This certificate is proudly presented to</div>
              <div class="cert-name">FoodWell.sniu</div>
              <div class="cert-company">Forex & Commodities Division</div>
              <div class="cert-award-box">
                <div class="cert-award-label">For Outstanding Achievement In</div>
                <div class="cert-award-title">Best Forex & Commodity Trading Services</div>
              </div>
              <div class="cert-year-badge">2023</div>
              <div class="cert-footer">
                <div class="cert-sig"><div class="cert-sig-line"></div><div class="cert-sig-name">Sumit Mauryan</div><div class="cert-sig-role">Founder & CEO</div></div>
                <div class="cert-id"><div class="cert-id-num">CERT#FXI-2023-005</div><div style="font-family:'Cinzel',serif;font-size:8px;color:rgba(74,48,0,0.5);margin-top:4px;">FX Intelligence Forum</div></div>
              </div>
            </div>
          </div>
          <div class="cert-bottom-strip"></div>
        </div>
      </div>

      <!-- CERT 6 -->
      <div class="cert-wrap">
        <div class="cert">
          <div class="cert-frame">
            <div class="cert-corner tl"></div><div class="cert-corner tr"></div>
            <div class="cert-corner bl"></div><div class="cert-corner br"></div>
            <div class="cert-inner">
              <div class="cert-holo">🛡️</div>
              <div class="cert-topline"><span class="cert-topstar">✦</span><span style="font-family:'Cinzel',serif;font-size:9px;color:#8B6508;letter-spacing:3px;">INVESTMENT WEEK MAGAZINE</span><span class="cert-topstar">✦</span></div>
              <div class="cert-of-text">Certificate</div>
              <div class="cert-excellence">of Merit</div>
              <div class="cert-divider"><div class="cert-divider-line"></div><div class="cert-divider-diamond"></div><div class="cert-divider-line"></div></div>
              <div class="cert-seal-wrap">
                <div class="cert-seal-outer"><div class="cert-seal-icon">🔰</div></div>
              </div>
              <div class="cert-pres">This certificate is proudly presented to</div>
              <div class="cert-name">FoodWell.sniu</div>
              <div class="cert-company">Risk & Strategy Division</div>
              <div class="cert-award-box">
                <div class="cert-award-label">For Outstanding Achievement In</div>
                <div class="cert-award-title">Outstanding Risk Management & Portfolio Strategy</div>
              </div>
              <div class="cert-year-badge">2023</div>
              <div class="cert-footer">
                <div class="cert-sig"><div class="cert-sig-line"></div><div class="cert-sig-name">Hasnain Ansari</div><div class="cert-sig-role">Co-Founder & MOD</div></div>
                <div class="cert-id"><div class="cert-id-num">CERT#IWM-2023-006</div><div style="font-family:'Cinzel',serif;font-size:8px;color:rgba(74,48,0,0.5);margin-top:4px;">Investment Week Magazine</div></div>
              </div>
            </div>
          </div>
          <div class="cert-bottom-strip"></div>
        </div>
      </div>

      <!-- CERT 7 -->
      <div class="cert-wrap">
        <div class="cert">
          <div class="cert-frame">
            <div class="cert-corner tl"></div><div class="cert-corner tr"></div>
            <div class="cert-corner bl"></div><div class="cert-corner br"></div>
            <div class="cert-inner">
              <div class="cert-holo">🌟</div>
              <div class="cert-topline"><span class="cert-topstar">✦</span><span style="font-family:'Cinzel',serif;font-size:9px;color:#8B6508;letter-spacing:3px;">WEALTHTECH SUMMIT</span><span class="cert-topstar">✦</span></div>
              <div class="cert-of-text">Certificate</div>
              <div class="cert-excellence">of Excellence</div>
              <div class="cert-divider"><div class="cert-divider-line"></div><div class="cert-divider-diamond"></div><div class="cert-divider-line"></div></div>
              <div class="cert-seal-wrap">
                <div class="cert-seal-outer"><div class="cert-seal-icon">🥈</div></div>
              </div>
              <div class="cert-pres">This certificate is proudly presented to</div>
              <div class="cert-name">FoodWell.sniu</div>
              <div class="cert-company">Client Experience Division</div>
              <div class="cert-award-box">
                <div class="cert-award-label">For Outstanding Achievement In</div>
                <div class="cert-award-title">Best Retail Trading Experience Platform</div>
              </div>
              <div class="cert-year-badge">2022</div>
              <div class="cert-footer">
                <div class="cert-sig"><div class="cert-sig-line"></div><div class="cert-sig-name">Sumit Mauryan</div><div class="cert-sig-role">Founder & CEO</div></div>
                <div class="cert-id"><div class="cert-id-num">CERT#WTS-2022-007</div><div style="font-family:'Cinzel',serif;font-size:8px;color:rgba(74,48,0,0.5);margin-top:4px;">WealthTech Summit 2022</div></div>
              </div>
            </div>
          </div>
          <div class="cert-bottom-strip"></div>
        </div>
      </div>

      <!-- CERT 8 -->
      <div class="cert-wrap">
        <div class="cert">
          <div class="cert-frame">
            <div class="cert-corner tl"></div><div class="cert-corner tr"></div>
            <div class="cert-corner bl"></div><div class="cert-corner br"></div>
            <div class="cert-inner">
              <div class="cert-holo">🇮🇳</div>
              <div class="cert-topline"><span class="cert-topstar">✦</span><span style="font-family:'Cinzel',serif;font-size:9px;color:#8B6508;letter-spacing:3px;">NSE EXCELLENCE AWARDS</span><span class="cert-topstar">✦</span></div>
              <div class="cert-of-text">Certificate</div>
              <div class="cert-excellence">of Merit</div>
              <div class="cert-divider"><div class="cert-divider-line"></div><div class="cert-divider-diamond"></div><div class="cert-divider-line"></div></div>
              <div class="cert-seal-wrap">
                <div class="cert-seal-outer"><div class="cert-seal-icon">🌐</div></div>
              </div>
              <div class="cert-pres">This certificate is proudly presented to</div>
              <div class="cert-name">FoodWell.sniu</div>
              <div class="cert-company">India Markets Research Desk</div>
              <div class="cert-award-box">
                <div class="cert-award-label">For Outstanding Achievement In</div>
                <div class="cert-award-title">Excellence in Indian Market Equity Research</div>
              </div>
              <div class="cert-year-badge">2022</div>
              <div class="cert-footer">
                <div class="cert-sig"><div class="cert-sig-line"></div><div class="cert-sig-name">Hasnain Ansari</div><div class="cert-sig-role">Co-Founder & MOD</div></div>
                <div class="cert-id"><div class="cert-id-num">CERT#NSE-2022-008</div><div style="font-family:'Cinzel',serif;font-size:8px;color:rgba(74,48,0,0.5);margin-top:4px;">NSE Excellence Awards</div></div>
              </div>
            </div>
          </div>
          <div class="cert-bottom-strip"></div>
        </div>
      </div>

      <!-- CERT 9 — CEO Personal Award -->
      <div class="cert-wrap">
        <div class="cert">
          <div class="cert-frame">
            <div class="cert-corner tl"></div><div class="cert-corner tr"></div>
            <div class="cert-corner bl"></div><div class="cert-corner br"></div>
            <div class="cert-inner">
              <div class="cert-holo">👑</div>
              <div class="cert-topline"><span class="cert-topstar">✦</span><span style="font-family:'Cinzel',serif;font-size:9px;color:#8B6508;letter-spacing:3px;">DIGITAL FINANCE AWARDS</span><span class="cert-topstar">✦</span></div>
              <div class="cert-of-text">Certificate</div>
              <div class="cert-excellence">of Leadership</div>
              <div class="cert-divider"><div class="cert-divider-line"></div><div class="cert-divider-diamond"></div><div class="cert-divider-line"></div></div>
              <div class="cert-seal-wrap">
                <div class="cert-seal-outer"><div class="cert-seal-icon">👑</div></div>
              </div>
              <div class="cert-pres">This certificate is proudly presented to</div>
              <div class="cert-name">Sumit Mauryan</div>
              <div class="cert-company">Founder & CEO — FoodWell.sniu</div>
              <div class="cert-award-box">
                <div class="cert-award-label">For Outstanding Achievement In</div>
                <div class="cert-award-title">Visionary Leadership in Financial Technology</div>
              </div>
              <div class="cert-year-badge">2022</div>
              <div class="cert-footer">
                <div class="cert-sig"><div class="cert-sig-line"></div><div class="cert-sig-name">Nirupama</div><div class="cert-sig-role">Private Secretary to CEO</div></div>
                <div class="cert-id"><div class="cert-id-num">CERT#DFA-2022-009</div><div style="font-family:'Cinzel',serif;font-size:8px;color:rgba(74,48,0,0.5);margin-top:4px;">Digital Finance Awards</div></div>
              </div>
            </div>
          </div>
          <div class="cert-bottom-strip"></div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- ===== LIVE CHARTS ===== -->
<section class="charts-sec" id="charts">
  <div class="container">
    <div class="sh">
      <div class="stag">📊 Real-Time Data</div>
      <h2 class="stitle"><span>Live Market</span> Charts</h2>
      <p class="ssub">Professional TradingView charts for Crypto, Forex, Gold, Silver, Indian Equities & Government Bonds — updating live every second.</p>
    </div>
    <div class="ctabs">
      <button class="tab-btn active" onclick="showChart('btc',this)">₿ Bitcoin</button>
      <button class="tab-btn" onclick="showChart('eth',this)">Ξ Ethereum</button>
      <button class="tab-btn" onclick="showChart('bnb',this)">🔶 BNB</button>
      <button class="tab-btn" onclick="showChart('gold',this)">🥇 Gold</button>
      <button class="tab-btn" onclick="showChart('silver',this)">🥈 Silver</button>
      <button class="tab-btn" onclick="showChart('eurusd',this)">💱 EUR/USD</button>
      <button class="tab-btn" onclick="showChart('nifty',this)">🇮🇳 NIFTY</button>
      <button class="tab-btn" onclick="showChart('bond',this)">📜 US Bond</button>
    </div>

    <!-- BTC -->
    <div class="cpanel active" id="chart-btc">
      <div class="cbox">
        <div class="chd"><div class="chl"><div class="chico" style="background:rgba(247,147,26,0.15);">₿</div><div><div class="chtit">BTC/USDT</div><div class="chsub">Bitcoin • Binance</div></div></div><div class="lbadge"><div class="ld"></div>LIVE</div></div>
        <div style="height:500px;"><div id="wbtc" style="height:100%;"></div></div>
        <script src="https://s3.tradingview.com/tv.js"></script>
        <script>new TradingView.widget({"width":"100%","height":500,"symbol":"BINANCE:BTCUSDT","interval":"15","timezone":"Asia/Kolkata","theme":"dark","style":"1","locale":"en","toolbar_bg":"#080F1E","enable_publishing":false,"hide_side_toolbar":false,"allow_symbol_change":true,"container_id":"wbtc","backgroundColor":"rgba(2,8,16,1)"});</script>
      </div>
    </div>

    <!-- ETH -->
    <div class="cpanel" id="chart-eth">
      <div class="cbox">
        <div class="chd"><div class="chl"><div class="chico" style="background:rgba(98,126,234,0.15);">Ξ</div><div><div class="chtit">ETH/USDT</div><div class="chsub">Ethereum • Binance</div></div></div><div class="lbadge"><div class="ld"></div>LIVE</div></div>
        <div style="height:500px;"><div id="weth" style="height:100%;"></div></div>
        <script>new TradingView.widget({"width":"100%","height":500,"symbol":"BINANCE:ETHUSDT","interval":"15","timezone":"Asia/Kolkata","theme":"dark","style":"1","locale":"en","toolbar_bg":"#080F1E","enable_publishing":false,"allow_symbol_change":true,"container_id":"weth","backgroundColor":"rgba(2,8,16,1)"});</script>
      </div>
    </div>

    <!-- BNB -->
    <div class="cpanel" id="chart-bnb">
      <div class="cbox">
        <div class="chd"><div class="chl"><div class="chico" style="background:rgba(243,186,47,0.15);">🔶</div><div><div class="chtit">BNB/USDT</div><div class="chsub">Binance Coin</div></div></div><div class="lbadge"><div class="ld"></div>LIVE</div></div>
        <div style="height:500px;"><div id="wbnb" style="height:100%;"></div></div>
        <script>new TradingView.widget({"width":"100%","height":500,"symbol":"BINANCE:BNBUSDT","interval":"15","timezone":"Asia/Kolkata","theme":"dark","style":"1","locale":"en","toolbar_bg":"#080F1E","enable_publishing":false,"allow_symbol_change":true,"container_id":"wbnb","backgroundColor":"rgba(2,8,16,1)"});</script>
      </div>
    </div>

    <!-- GOLD -->
    <div class="cpanel" id="chart-gold">
      <div class="cbox">
        <div class="chd"><div class="chl"><div class="chico" style="background:rgba(255,215,0,0.15);">🥇</div><div><div class="chtit">GOLD — XAU/USD</div><div class="chsub">Spot Gold • TVC</div></div></div><div class="lbadge"><div class="ld"></div>LIVE</div></div>
        <div style="height:500px;"><div id="wgold" style="height:100%;"></div></div>
        <script>new TradingView.widget({"width":"100%","height":500,"symbol":"TVC:GOLD","interval":"60","timezone":"Asia/Kolkata","theme":"dark","style":"1","locale":"en","toolbar_bg":"#080F1E","enable_publishing":false,"allow_symbol_change":true,"container_id":"wgold","backgroundColor":"rgba(2,8,16,1)"});</script>
      </div>
    </div>

    <!-- SILVER -->
    <div class="cpanel" id="chart-silver">
      <div class="cbox">
        <div class="chd"><div class="chl"><div class="chico" style="background:rgba(192,192,192,0.15);">🥈</div><div><div class="chtit">SILVER — XAG/USD</div><div class="chsub">Spot Silver • TVC</div></div></div><div class="lbadge"><div class="ld"></div>LIVE</div></div>
        <div style="height:500px;"><div id="wsilver" style="height:100%;"></div></div>
        <script>new TradingView.widget({"width":"100%","height":500,"symbol":"TVC:SILVER","interval":"60","timezone":"Asia/Kolkata","theme":"dark","style":"1","locale":"en","toolbar_bg":"#080F1E","enable_publishing":false,"allow_symbol_change":true,"container_id":"wsilver","backgroundColor":"rgba(2,8,16,1)"});</script>
      </div>
    </div>

    <!-- EUR/USD -->
    <div class="cpanel" id="chart-eurusd">
      <div class="cbox">
        <div class="chd"><div class="chl"><div class="chico" style="background:rgba(0,198,255,0.15);">💱</div><div><div class="chtit">EUR/USD</div><div class="chsub">Forex Major Pair</div></div></div><div class="lbadge"><div class="ld"></div>LIVE</div></div>
        <div style="height:500px;"><div id="weurusd" style="height:100%;"></div></div>
        <script>new TradingView.widget({"width":"100%","height":500,"symbol":"FX:EURUSD","interval":"60","timezone":"Europe/London","theme":"dark","style":"1","locale":"en","toolbar_bg":"#080F1E","enable_publishing":false,"allow_symbol_change":true,"container_id":"weurusd","backgroundColor":"rgba(2,8,16,1)"});</script>
      </div>
    </div>

    <!-- NIFTY -->
    <div class="cpanel" id="chart-nifty">
      <div class="cbox">
        <div class="chd"><div class="chl"><div class="chico" style="background:rgba(255,153,0,0.15);">🇮🇳</div><div><div class="chtit">NIFTY 50</div><div class="chsub">NSE India</div></div></div><div class="lbadge"><div class="ld"></div>LIVE</div></div>
        <div style="height:500px;"><div id="wnifty" style="height:100%;"></div></div>
        <script>new TradingView.widget({"width":"100%","height":500,"symbol":"NSE:NIFTY","interval":"15","timezone":"Asia/Kolkata","theme":"dark","style":"1","locale":"en","toolbar_bg":"#080F1E","enable_publishing":false,"allow_symbol_change":true,"container_id":"wnifty","backgroundColor":"rgba(2,8,16,1)"});</script>
      </div>
    </div>

    <!-- BOND -->
    <div class="cpanel" id="chart-bond">
      <div class="cbox">
        <div class="chd"><div class="chl"><div class="chico" style="background:rgba(0,255,136,0.12);">📜</div><div><div class="chtit">US 10Y Gov Bond</div><div class="chsub">Treasury Yield • TVC</div></div></div><div class="lbadge"><div class="ld"></div>LIVE</div></div>
        <div style="height:500px;"><div id="wbond" style="height:100%;"></div></div>
        <script>new TradingView.widget({"width":"100%","height":500,"symbol":"TVC:US10Y","interval":"D","timezone":"America/New_York","theme":"dark","style":"1","locale":"en","toolbar_bg":"#080F1E","enable_publishing":false,"allow_symbol_change":true,"container_id":"wbond","backgroundColor":"rgba(2,8,16,1)"});</script>
      </div>
    </div>

    <!-- MINI GRID -->
    <div class="mgrid">
      <div class="mcard">
        <div class="mhd"><div class="ml"><div class="mico" style="background:rgba(247,147,26,0.15);">₿</div><div><div class="mn">BTC/USDT</div><div class="mf">Bitcoin</div></div></div><div class="lbadge" style="font-size:10px;padding:3px 10px;"><div class="ld"></div>LIVE</div></div>
        <div id="mbtc"></div><script>new TradingView.widget({"width":"100%","height":220,"symbol":"BINANCE:BTCUSDT","interval":"5","theme":"dark","style":"3","locale":"en","enable_publishing":false,"hide_top_toolbar":true,"hide_legend":true,"hide_side_toolbar":true,"allow_symbol_change":false,"container_id":"mbtc","backgroundColor":"rgba(2,8,16,1)"});</script>
      </div>
      <div class="mcard">
        <div class="mhd"><div class="ml"><div class="mico" style="background:rgba(255,215,0,0.15);">🥇</div><div><div class="mn">GOLD</div><div class="mf">XAU/USD</div></div></div><div class="lbadge" style="font-size:10px;padding:3px 10px;"><div class="ld"></div>LIVE</div></div>
        <div id="mgold"></div><script>new TradingView.widget({"width":"100%","height":220,"symbol":"TVC:GOLD","interval":"60","theme":"dark","style":"3","locale":"en","enable_publishing":false,"hide_top_toolbar":true,"hide_legend":true,"hide_side_toolbar":true,"allow_symbol_change":false,"container_id":"mgold","backgroundColor":"rgba(2,8,16,1)"});</script>
      </div>
      <div class="mcard">
        <div class="mhd"><div class="ml"><div class="mico" style="background:rgba(0,198,255,0.15);">💱</div><div><div class="mn">EUR/USD</div><div class="mf">Forex</div></div></div><div class="lbadge" style="font-size:10px;padding:3px 10px;"><div class="ld"></div>LIVE</div></div>
        <div id="meurusd"></div><script>new TradingView.widget({"width":"100%","height":220,"symbol":"FX:EURUSD","interval":"60","theme":"dark","style":"3","locale":"en","enable_publishing":false,"hide_top_toolbar":true,"hide_legend":true,"hide_side_toolbar":true,"allow_symbol_change":false,"container_id":"meurusd","backgroundColor":"rgba(2,8,16,1)"});</script>
      </div>
      <div class="mcard">
        <div class="mhd"><div class="ml"><div class="mico" style="background:rgba(192,192,192,0.15);">🥈</div><div><div class="mn">SILVER</div><div class="mf">XAG/USD</div></div></div><div class="lbadge" style="font-size:10px;padding:3px 10px;"><div class="ld"></div>LIVE</div></div>
        <div id="msilver"></div><script>new TradingView.widget({"width":"100%","height":220,"symbol":"TVC:SILVER","interval":"60","theme":"dark","style":"3","locale":"en","enable_publishing":false,"hide_top_toolbar":true,"hide_legend":true,"hide_side_toolbar":true,"allow_symbol_change":false,"container_id":"msilver","backgroundColor":"rgba(2,8,16,1)"});</script>
      </div>
      <div class="mcard">
        <div class="mhd"><div class="ml"><div class="mico" style="background:rgba(255,153,0,0.15);">🇮🇳</div><div><div class="mn">NIFTY 50</div><div class="mf">NSE India</div></div></div><div class="lbadge" style="font-size:10px;padding:3px 10px;"><div class="ld"></div>LIVE</div></div>
        <div id="mnifty"></div><script>new TradingView.widget({"width":"100%","height":220,"symbol":"NSE:NIFTY","interval":"15","theme":"dark","style":"3","locale":"en","enable_publishing":false,"hide_top_toolbar":true,"hide_legend":true,"hide_side_toolbar":true,"allow_symbol_change":false,"container_id":"mnifty","backgroundColor":"rgba(2,8,16,1)"});</script>
      </div>
      <div class="mcard">
        <div class="mhd"><div class="ml"><div class="mico" style="background:rgba(0,255,136,0.12);">📜</div><div><div class="mn">US 10Y Bond</div><div class="mf">Gov Bond</div></div></div><div class="lbadge" style="font-size:10px;padding:3px 10px;"><div class="ld"></div>LIVE</div></div>
        <div id="mbond"></div><script>new TradingView.widget({"width":"100%","height":220,"symbol":"TVC:US10Y","interval":"D","theme":"dark","style":"3","locale":"en","enable_publishing":false,"hide_top_toolbar":true,"hide_legend":true,"hide_side_toolbar":true,"allow_symbol_change":false,"container_id":"mbond","backgroundColor":"rgba(2,8,16,1)"});</script>
      </div>
    </div>
  </div>
</section>

<!-- ===== MARKET OVERVIEW ===== -->
<section class="mkt-sec" id="marketoverview">
  <div class="container">
    <div class="sh">
      <div class="stag">🌍 Global Markets</div>
      <h2 class="stitle">Complete Market <span>Overview</span></h2>
      <p class="ssub">Full global snapshot — Crypto, Commodities, Government Bonds, Indian Markets and Forex all in one premium view.</p>
    </div>
    <div style="border-radius:18px;overflow:hidden;border:1px solid var(--border);">
      <div class="tradingview-widget-container">
        <div class="tradingview-widget-container__widget"></div>
        <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-market-overview.js" async>
        {"colorTheme":"dark","dateRange":"12M","showChart":true,"locale":"en","width":"100%","height":"700","isTransparent":true,"showSymbolLogo":true,"tabs":[
          {"title":"Crypto","symbols":[{"s":"BINANCE:BTCUSDT","d":"Bitcoin"},{"s":"BINANCE:ETHUSDT","d":"Ethereum"},{"s":"BINANCE:BNBUSDT","d":"BNB"},{"s":"BINANCE:SOLUSDT","d":"Solana"},{"s":"BINANCE:XRPUSDT","d":"XRP"}]},
          {"title":"Commodities","symbols":[{"s":"TVC:GOLD","d":"Gold"},{"s":"TVC:SILVER","d":"Silver"},{"s":"NYMEX:CL1!","d":"Crude Oil"},{"s":"NYMEX:NG1!","d":"Natural Gas"},{"s":"CBOT:ZW1!","d":"Wheat"}]},
          {"title":"Gov Bonds","symbols":[{"s":"TVC:US10Y","d":"US 10Y"},{"s":"TVC:US02Y","d":"US 2Y"},{"s":"TVC:US30Y","d":"US 30Y"},{"s":"TVC:IN10Y","d":"India 10Y"},{"s":"TVC:DE10Y","d":"Germany 10Y"}]},
          {"title":"India","symbols":[{"s":"NSE:NIFTY","d":"NIFTY 50"},{"s":"BSE:SENSEX","d":"SENSEX"},{"s":"NSE:RELIANCE","d":"Reliance"},{"s":"NSE:TCS","d":"TCS"},{"s":"NSE:HDFCBANK","d":"HDFC Bank"}]},
          {"title":"Forex","symbols":[{"s":"FX:EURUSD"},{"s":"FX:GBPUSD"},{"s":"FX:USDJPY"},{"s":"FX:USDINR"},{"s":"FX:AUDUSD"}]}
        ]}
        </script>
      </div>
    </div>
  </div>
</section>

<!-- ===== TEAM ===== -->
<section class="team-sec" id="team">
  <div class="container">
    <div class="sh">
      <div class="stag">👥 Our Team</div>
      <h2 class="stitle">Meet the <span>FoodWell.sniu</span> Team</h2>
      <p class="ssub">A world-class team of trading experts, hedge fund managers, quant analysts, and risk specialists — united by one mission.</p>
    </div>

    <!-- TOP 2 LEADERS -->
    <div class="team-top">
      <!-- SUMIT -->
      <div style="display:flex;flex-direction:column;align-items:center;">
        <div class="tc ceo">
          <div style="position:absolute;top:14px;left:14px;background:linear-gradient(135deg,var(--gold),var(--gold2));color:var(--dark);font-size:10px;font-weight:700;padding:3px 10px;border-radius:5px;font-family:'Rajdhani',sans-serif;letter-spacing:1px;">FOUNDER</div>
          <div class="tav"><div>👨‍💼</div><div class="tav-ring"></div></div>
          <div class="tname">Sumit Mauryan</div>
          <div class="trole">Founder & CEO</div>
          <div class="tbadge">Chief Executive Officer</div>
          <div class="tdesc">Visionary leader driving FoodWell.sniu's global trading strategy and market expansion worldwide.</div>
          <div class="tsoc">
            <a href="mailto:sm8880438@gmail.com"><i class="fas fa-envelope"></i></a>
            <a href="#"><i class="fab fa-linkedin"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
          </div>
        </div>
        <!-- Private Secretary below CEO -->
        <div class="priv-wrap">
          <div class="priv-line"></div>
          <div class="priv-card">
            <div style="width:56px;height:56px;border-radius:50%;background:linear-gradient(135deg,rgba(255,215,0,0.12),rgba(255,165,0,0.04));border:2px solid rgba(255,215,0,0.25);display:flex;align-items:center;justify-content:center;font-size:24px;margin:0 auto 12px;">👩‍💼</div>
            <div style="font-family:'Orbitron',sans-serif;font-size:13px;font-weight:700;margin-bottom:5px;">Nirupama</div>
            <div style="font-size:11px;color:var(--gold2);font-family:'Rajdhani',sans-serif;font-weight:700;letter-spacing:1px;text-transform:uppercase;margin-bottom:6px;">Private Secretary</div>
            <div style="display:inline-block;background:rgba(255,215,0,0.06);border:1px solid rgba(255,215,0,0.2);color:var(--gold2);padding:3px 10px;border-radius:5px;font-size:10px;font-family:'Rajdhani',sans-serif;font-weight:600;">CEO Office</div>
            <div style="font-size:11px;color:var(--muted);margin-top:8px;line-height:1.6;">Strategic coordination & executive board operations management.</div>
          </div>
        </div>
      </div>

      <!-- HASNAIN -->
      <div style="display:flex;flex-direction:column;align-items:center;">
        <div class="tc mod">
          <div style="position:absolute;top:14px;left:14px;background:rgba(155,89,182,0.2);border:1px solid rgba(155,89,182,0.4);color:var(--purple);font-size:10px;font-weight:700;padding:3px 10px;border-radius:5px;font-family:'Rajdhani',sans-serif;letter-spacing:1px;">CO-FOUNDER</div>
          <div class="tav" style="background:linear-gradient(135deg,rgba(155,89,182,0.15),rgba(155,89,182,0.05));border-color:rgba(155,89,182,0.3);">
            <div>👨‍💻</div><div class="tav-ring" style="border-color:rgba(155,89,182,0.12);"></div>
          </div>
          <div class="tname">Hasnain Ansari</div>
          <div class="trole" style="color:var(--purple);">Co-Founder & MOD</div>
          <div class="tbadge" style="background:rgba(155,89,182,0.08);border-color:rgba(155,89,182,0.2);color:var(--purple);">Head of Operations</div>
          <div class="tdesc">Leads trading operations, team management, and product development strategy at FoodWell.sniu.</div>
          <div class="tsoc">
            <a href="#"><i class="fas fa-envelope"></i></a>
            <a href="#"><i class="fab fa-linkedin"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
          </div>
        </div>

        <!-- 4 Sub Team Members -->
        <div style="width:2px;height:36px;background:linear-gradient(var(--purple),var(--border));margin:0 auto;"></div>
        <div style="font-family:'Rajdhani',sans-serif;font-size:11px;color:var(--muted);letter-spacing:3px;text-transform:uppercase;margin-bottom:16px;text-align:center;">Operations Team</div>
        <div class="sub-grid">
          <div class="stc">
            <div class="stav" style="background:linear-gradient(135deg,rgba(155,89,182,0.1),rgba(155,89,182,0.03));border-color:rgba(155,89,182,0.18);">👨‍📊</div>
            <div class="stn">Anurag</div>
            <div class="str" style="color:#9B59B6;">Sr. Trading Analyst</div>
            <div class="stb" style="background:rgba(155,89,182,0.06);border-color:rgba(155,89,182,0.15);color:#9B59B6;">Trading Desk</div>
            <div class="std">Technical analysis, chart patterns & trade execution strategies for all asset classes.</div>
          </div>
          <div class="stc">
            <div class="stav" style="background:linear-gradient(135deg,rgba(155,89,182,0.1),rgba(155,89,182,0.03));border-color:rgba(155,89,182,0.18);">👩‍💹</div>
            <div class="stn">Ayushi</div>
            <div class="str" style="color:#9B59B6;">Hedge Fund Manager</div>
            <div class="stb" style="background:rgba(155,89,182,0.06);border-color:rgba(155,89,182,0.15);color:#9B59B6;">Hedge Fund</div>
            <div class="std">Portfolio allocation, long/short strategies & institutional fund management.</div>
          </div>
          <div class="stc">
            <div class="stav" style="background:linear-gradient(135deg,rgba(155,89,182,0.1),rgba(155,89,182,0.03));border-color:rgba(155,89,182,0.18);">👨‍🔬</div>
            <div class="stn">Abhay</div>
            <div class="str" style="color:#9B59B6;">Quantitative Analyst</div>
            <div class="stb" style="background:rgba(155,89,182,0.06);border-color:rgba(155,89,182,0.15);color:#9B59B6;">Quant Desk</div>
            <div class="std">Algorithmic models, quantitative research & AI-driven trading signals.</div>
          </div>
          <div class="stc">
            <div class="stav" style="background:linear-gradient(135deg,rgba(155,89,182,0.1),rgba(155,89,182,0.03));border-color:rgba(155,89,182,0.18);">👨‍⚖️</div>
            <div class="stn">Vinay</div>
            <div class="str" style="color:#9B59B6;">Risk Management Head</div>
            <div class="stb" style="background:rgba(155,89,182,0.06);border-color:rgba(155,89,182,0.15);color:#9B59B6;">Risk Desk</div>
            <div class="std">Market risk control, VaR calculations & portfolio stress testing frameworks.</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== FEATURES ===== -->
<section class="feat-sec" id="features">
  <div class="container">
    <div class="sh">
      <div class="stag">⚡ Platform Features</div>
      <h2 class="stitle">Why Trade With <span>FoodWell.sniu?</span></h2>
      <p class="ssub">Institutional-grade tools combined with a retail-friendly interface — giving every trader the professional edge they deserve.</p>
    </div>
    <div class="fgrid">
      <div class="fc"><div class="fi">📊</div><div class="ft">Real-Time Live Charts</div><div class="fd">Professional TradingView charts for Crypto, Gold, Silver, Bonds, Forex & Indian Equities — every tick updated live in real time.</div></div>
      <div class="fc"><div class="fi">🤖</div><div class="ft">AI Trading Signals</div><div class="fd">Anurag & Abhay's proprietary AI analyzes 600+ market indicators to deliver high-probability institutional-grade trading signals.</div></div>
      <div class="fc"><div class="fi">🏦</div><div class="ft">Hedge Fund Strategies</div><div class="fd">Access Ayushi's institutional hedge fund frameworks — long/short equity, macro trading, and arbitrage strategies for maximum alpha.</div></div>
      <div class="fc"><div class="fi">🛡️</div><div class="ft">Advanced Risk Management</div><div class="fd">Vinay's risk desk provides real-time monitoring, stop-loss automation, VaR calculations, and portfolio stress testing tools.</div></div>
      <div class="fc"><div class="fi">🌐</div><div class="ft">Multi-Asset Trading</div><div class="fd">Trade Crypto, Gold, Silver, Forex, NSE/BSE Equities, Government Bonds, and Commodities — all from one premium dashboard.</div></div>
      <div class="fc"><div class="fi">🔒</div><div class="ft">Bank-Grade Security</div><div class="fd">256-bit SSL, 2FA, cold wallet storage, multi-sig authorization, and biometric verification across all FoodWell.sniu accounts.</div></div>
      <div class="fc"><div class="fi">📰</div><div class="ft">Market Research</div><div class="fd">Live breaking news, fundamental analysis, economic calendar, earnings reports and FoodWell.sniu's exclusive daily market briefings.</div></div>
      <div class="fc"><div class="fi">⚡</div><div class="ft">Ultra-Low Latency</div><div class="fd">Sub-millisecond order execution across 14 global data centers — zero slippage guaranteed from scalping to institutional blocks.</div></div>
      <div class="fc"><div class="fi">📱</div><div class="ft">Mobile Trading App</div><div class="fd">Full-featured iOS & Android apps. Trade, analyze, manage portfolio, get AI alerts — all coordinated by Nirupama's executive briefings.</div></div>
    </div>
  </div>
</section>

<!-- ===== CONTACT ===== -->
<section class="contact-sec" id="contact">
  <div class="container">
    <div class="sh">
      <div class="stag">📬 Contact Us</div>
      <h2 class="stitle">Get In Touch With <span>Our Team</span></h2>
      <p class="ssub">Our expert team is available 24/7 to assist you with trading queries, account setup, partnerships, and investment guidance.</p>
    </div>
    <div class="cgrid">
      <div class="ci">
        <h3>We're Here<br/><span style="background:linear-gradient(135deg,var(--accent),var(--gold));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;">To Help You Trade Better</span></h3>
        <p>Reach out to our team of trading professionals at FoodWell.sniu. Whether you need trading support, hedge fund consultations, or platform guidance — we're always here.</p>
        <a href="mailto:sm8880438@gmail.com" class="citem">
          <div class="cico"><i class="fas fa-envelope"></i></div>
          <div><div class="clabel">CEO Email</div><div class="cval">sm8880438@gmail.com</div></div>
          <i class="fas fa-arrow-right" style="color:var(--muted);margin-left:auto;"></i>
        </a>
        <a href="#" class="citem">
          <div class="cico"><i class="fab fa-telegram"></i></div>
          <div><div class="clabel">Telegram</div><div class="cval">@FoodWellSniu</div></div>
          <i class="fas fa-arrow-right" style="color:var(--muted);margin-left:auto;"></i>
        </a>
        <a href="#" class="citem">
          <div class="cico"><i class="fab fa-whatsapp"></i></div>
          <div><div class="clabel">WhatsApp</div><div class="cval">Available for Premium Members</div></div>
          <i class="fas fa-arrow-right" style="color:var(--muted);margin-left:auto;"></i>
        </a>
        <a href="#" class="citem">
          <div class="cico"><i class="fas fa-headset"></i></div>
          <div><div class="clabel">Live Support</div><div class="cval">24/7 — Avg. Response: Under 2 Minutes</div></div>
          <i class="fas fa-arrow-right" style="color:var(--muted);margin-left:auto;"></i>
        </a>
        <div style="margin-top:28px;padding:22px;background:rgba(255,215,0,0.04);border:1px solid rgba(255,215,0,0.18);border-radius:14px;">
          <div style="font-size:11px;color:var(--gold);font-family:'Rajdhani',sans-serif;font-weight:700;letter-spacing:2.5px;text-transform:uppercase;margin-bottom:12px;">⏰ Market Hours</div>
          <div style="font-size:13px;color:var(--muted);line-height:2.2;">
            Crypto: <span style="color:var(--green);font-weight:600;">24/7/365</span><br/>
            Gold & Silver: <span style="color:var(--text);">Mon–Fri  9AM–5PM EST</span><br/>
            NSE/BSE India: <span style="color:var(--text);">Mon–Fri  9:15AM–3:30PM IST</span><br/>
            Forex: <span style="color:var(--text);">Mon–Fri  24 Hours</span><br/>
            Gov Bonds: <span style="color:var(--text);">Mon–Fri  8AM–8PM EST</span>
          </div>
        </div>
      </div>
      <div class="cform">
        <h4>📩 Send Us a Message</h4>
        <div class="frow">
          <div class="fgrp"><label>First Name</label><input type="text" placeholder="Your Name"/></div>
          <div class="fgrp"><label>Last Name</label><input type="text" placeholder="Last Name"/></div>
        </div>
        <div class="fgrp"><label>Email Address</label><input type="email" placeholder="your@email.com"/></div>
        <div class="fgrp"><label>Phone Number</label><input type="tel" placeholder="+91 XXXXX XXXXX"/></div>
        <div class="fgrp">
          <label>Interested In</label>
          <select>
            <option>Bitcoin / Crypto Trading</option>
            <option>Gold & Silver Trading</option>
            <option>Forex Trading</option>
            <option>Indian Equities (NSE/BSE)</option>
            <option>Government Bonds</option>
            <option>Hedge Fund Services</option>
            <option>AI Trading Signals</option>
            <option>Portfolio Management</option>
            <option>Risk Management</option>
            <option>Partnership / Business</option>
          </select>
        </div>
        <div class="fgrp"><label>Message</label><textarea placeholder="Tell us about your trading goals..."></textarea></div>
        <button class="fsub" onclick="handleForm(this)"><i class="fas fa-paper-plane"></i>Send Message</button>
      </div>
    </div>
  </div>
</section>

<!-- ===== FOOTER ===== -->
<footer>
  <div class="fgridf">
    <div class="fbrand">
      <div class="nav-logo">
        <div class="logo-box">🍃</div>
        <div><div class="logo-name">FoodWell.sniu</div><span class="logo-sub">Premium Trading & Investment</span></div>
      </div>
      <p>FoodWell.sniu is a premium trading and investment platform offering real-time charts, AI signals, hedge fund strategies, and institutional-grade analytics. Founded by Sumit Mauryan & Hasnain Ansari.</p>
      <div class="fsoc">
        <a href="#" class="sb"><i class="fab fa-twitter"></i></a>
        <a href="#" class="sb"><i class="fab fa-telegram"></i></a>
        <a href="#" class="sb"><i class="fab fa-discord"></i></a>
        <a href="#" class="sb"><i class="fab fa-linkedin"></i></a>
        <a href="#" class="sb"><i class="fab fa-youtube"></i></a>
        <a href="mailto:sm8880438@gmail.com" class="sb"><i class="fas fa-envelope"></i></a>
        <a href="#" class="sb"><i class="fab fa-instagram"></i></a>
      </div>
    </div>
    <div class="fcol">
      <h5>Markets</h5>
      <ul>
        <li><a href="#">Bitcoin (BTC)</a></li><li><a href="#">Ethereum (ETH)</a></li>
        <li><a href="#">Gold (XAU/USD)</a></li><li><a href="#">Silver (XAG/USD)</a></li>
        <li><a href="#">NIFTY 50</a></li><li><a href="#">SENSEX</a></li>
        <li><a href="#">Gov Bonds</a></li><li><a href="#">Forex Pairs</a></li>
      </ul>
    </div>
    <div class="fcol">
      <h5>Services</h5>
      <ul>
        <li><a href="#">Live Charts</a></li><li><a href="#">AI Signals</a></li>
        <li><a href="#">Hedge Fund</a></li><li><a href="#">Risk Management</a></li>
        <li><a href="#">Portfolio Tracker</a></li><li><a href="#">Market Research</a></li>
        <li><a href="#">Trading Academy</a></li><li><a href="#">Mobile App</a></li>
      </ul>
    </div>
    <div class="fcol">
      <h5>Company</h5>
      <ul>
        <li><a href="#about">About Us</a></li><li><a href="#team">Our Team</a></li>
        <li><a href="#awards">Awards</a></li><li><a href="#">Careers</a></li>
        <li><a href="#">Press Room</a></li><li><a href="#">Partners</a></li>
        <li><a href="#contact">Contact</a></li><li><a href="mailto:sm8880438@gmail.com">Email CEO</a></li>
      </ul>
    </div>
  </div>

  <div class="disc">
    <i class="fas fa-exclamation-triangle"></i>
    <div><strong style="color:#FFA500;">⚠️ Risk Disclaimer:</strong> Trading in financial instruments including cryptocurrencies, commodities, forex, equities, and government bonds involves substantial risk. Past performance is not indicative of future results. Never invest money you cannot afford to lose. FoodWell.sniu provides information for educational purposes only and does not constitute financial advice. FoodWell.sniu and its team — Sumit Mauryan, Hasnain Ansari, Anurag, Ayushi, Abhay, Vinay, and Nirupama — are not liable for any trading losses.</div>
  </div>

  <div class="fbot">
    <p>© 2024 <strong style="color:var(--accent);">FoodWell.sniu</strong> — All Rights Reserved | CEO: <strong style="color:var(--gold);">Sumit Mauryan</strong> | <a href="mailto:sm8880438@gmail.com" style="color:var(--accent);text-decoration:none;">sm8880438@gmail.com</a></p>
    <div class="fblinks">
      <a href="#">Privacy Policy</a><a href="#">Terms of Service</a>
      <a href="#">Cookie Policy</a><a href="#">Regulatory Info</a>
    </div>
  </div>
</footer>

<!-- ===== JS ===== -->
<script>
function showChart(id,btn){
  document.querySelectorAll('.cpanel').forEach(p=>p.classList.remove('active'));
  document.querySelectorAll('.tab-btn').forEach(b=>b.classList.remove('active'));
  document.getElementById('chart-'+id).classList.add('active');
  btn.classList.add('active');
}
function handleForm(btn){
  btn.innerHTML='<i class="fas fa-check-circle"></i> Message Sent!';
  btn.style.background='linear-gradient(135deg,#00FF88,#00BB66)';
  setTimeout(()=>{btn.innerHTML='<i class="fas fa-paper-plane"></i> Send Message';btn.style.background='';},3500);
}
document.querySelectorAll('a[href^="#"]').forEach(a=>{
  a.addEventListener('click',e=>{
    const t=document.querySelector(a.getAttribute('href'));
    if(t){e.preventDefault();t.scrollIntoView({behavior:'smooth',block:'start'});}
  });
});
window.addEventListener('scroll',()=>{
  document.querySelector('nav').style.boxShadow=
    window.scrollY>60?'0 4px 30px rgba(0,198,255,0.12)':'none';
});
const obs=new IntersectionObserver(entries=>{
  entries.forEach(e=>{
    if(e.isIntersecting){e.target.style.opacity='1';e.target.style.transform='translateY(0)';}
  });
},{threshold:0.08});
document.querySelectorAll('.cert,.fc,.stc,.asc,.mcard').forEach(el=>{
  el.style.opacity='0';el.style.transform='translateY(28px)';
  el.style.transition='opacity 0.65s ease,transform 0.65s ease';
  obs.observe(el);
});
</script>
</body>
</html>
