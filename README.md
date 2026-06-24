<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Maa Nirmala Business Consulting Pvt. Ltd. | Way of Success</title>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;900&family=Open+Sans:wght@300;400;600&display=swap" rel="stylesheet"/>
<style>
  :root{
    --orange:#E85B1E;
    --navy:#1A2240;
    --dark:#0D1320;
    --light:#F5F6FA;
    --white:#FFFFFF;
    --accent:#FF7A2F;
    --gold:#C8960C;
  }
  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{font-family:'Open Sans',sans-serif;background:var(--dark);color:var(--white);overflow-x:hidden;}

  /* SCROLLBAR */
  ::-webkit-scrollbar{width:6px;}
  ::-webkit-scrollbar-track{background:var(--dark);}
  ::-webkit-scrollbar-thumb{background:var(--orange);border-radius:3px;}

  /* NAVBAR */
  nav{
    position:fixed;top:0;left:0;width:100%;z-index:1000;
    background:rgba(13,19,32,0.95);
    backdrop-filter:blur(12px);
    border-bottom:2px solid var(--orange);
    display:flex;align-items:center;justify-content:space-between;
    padding:0 40px;height:72px;
    transition:all 0.3s;
  }
  .nav-logo{display:flex;align-items:center;gap:14px;}
  .logo-svg{width:56px;height:56px;}
  .nav-brand{display:flex;flex-direction:column;}
  .nav-brand h1{font-family:'Montserrat',sans-serif;font-size:14px;font-weight:900;color:var(--white);letter-spacing:1px;line-height:1.1;}
  .nav-brand span{font-size:9px;color:var(--orange);letter-spacing:3px;font-weight:600;}
  .nav-links{display:flex;gap:28px;list-style:none;}
  .nav-links a{color:rgba(255,255,255,0.82);text-decoration:none;font-size:12.5px;font-weight:600;letter-spacing:1.5px;text-transform:uppercase;transition:color 0.3s;position:relative;}
  .nav-links a::after{content:'';position:absolute;bottom:-4px;left:0;width:0;height:2px;background:var(--orange);transition:width 0.3s;}
  .nav-links a:hover{color:var(--orange);}
  .nav-links a:hover::after{width:100%;}
  .nav-cta{background:var(--orange);color:var(--white);padding:9px 22px;border-radius:4px;font-weight:700;font-size:12px;letter-spacing:1px;text-decoration:none;transition:background 0.3s,transform 0.2s;}
  .nav-cta:hover{background:var(--accent);transform:translateY(-2px);}
  .hamburger{display:none;flex-direction:column;gap:5px;cursor:pointer;}
  .hamburger span{display:block;width:24px;height:2px;background:var(--white);transition:all 0.3s;}

  /* HERO */
  .hero{
    position:relative;min-height:100vh;
    display:flex;align-items:center;justify-content:center;
    overflow:hidden;
    background:linear-gradient(135deg,#0D1320 0%,#1A2240 50%,#0D1320 100%);
  }
  #hero-canvas{position:absolute;top:0;left:0;width:100%;height:100%;z-index:0;}
  .hero-diagonal{
    position:absolute;top:0;right:0;width:48%;height:100%;
    background:linear-gradient(180deg,rgba(232,91,30,0.12) 0%,rgba(26,34,64,0.05) 100%);
    clip-path:polygon(15% 0,100% 0,100% 100%,0 100%);
    z-index:1;
  }
  .hero-content{
    position:relative;z-index:2;
    display:grid;grid-template-columns:1fr 1fr;
    gap:60px;align-items:center;
    max-width:1200px;width:100%;padding:0 40px;
  }
  .hero-left{}
  .hero-eyebrow{
    display:inline-flex;align-items:center;gap:8px;
    background:rgba(232,91,30,0.15);border:1px solid rgba(232,91,30,0.4);
    border-radius:50px;padding:6px 18px;margin-bottom:24px;
    font-size:11px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:var(--orange);
    animation:fadeInDown 0.8s ease both;
  }
  .hero-eyebrow::before{content:'';width:6px;height:6px;border-radius:50%;background:var(--orange);animation:pulse-dot 1.5s infinite;}
  .hero-title{
    font-family:'Montserrat',sans-serif;font-size:42px;font-weight:900;
    line-height:1.12;margin-bottom:10px;
    animation:fadeInUp 0.9s ease 0.2s both;
  }
  .hero-title span{color:var(--orange);}
  .hero-subtitle{
    font-size:13px;font-weight:700;color:var(--orange);letter-spacing:4px;
    text-transform:uppercase;margin-bottom:20px;
    animation:fadeInUp 0.9s ease 0.3s both;
  }
  .hero-desc{
    font-size:15px;color:rgba(255,255,255,0.72);line-height:1.75;margin-bottom:36px;
    animation:fadeInUp 0.9s ease 0.4s both;
  }
  .hero-btns{display:flex;gap:16px;flex-wrap:wrap;animation:fadeInUp 0.9s ease 0.5s both;}
  .btn-primary{
    background:var(--orange);color:var(--white);padding:14px 32px;
    border-radius:5px;font-weight:700;font-size:13px;letter-spacing:1px;
    text-decoration:none;transition:all 0.3s;display:inline-block;
    box-shadow:0 4px 20px rgba(232,91,30,0.4);
  }
  .btn-primary:hover{background:var(--accent);transform:translateY(-3px);box-shadow:0 8px 30px rgba(232,91,30,0.5);}
  .btn-outline{
    border:2px solid rgba(255,255,255,0.4);color:var(--white);padding:14px 32px;
    border-radius:5px;font-weight:700;font-size:13px;letter-spacing:1px;
    text-decoration:none;transition:all 0.3s;display:inline-block;
  }
  .btn-outline:hover{border-color:var(--orange);color:var(--orange);transform:translateY(-3px);}
  .hero-stats{
    display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:36px;
    animation:fadeInUp 0.9s ease 0.6s both;
  }
  .stat-item{text-align:center;padding:16px 8px;background:rgba(255,255,255,0.04);border:1px solid rgba(255,255,255,0.08);border-radius:8px;}
  .stat-num{font-family:'Montserrat',sans-serif;font-size:28px;font-weight:900;color:var(--orange);}
  .stat-label{font-size:10px;color:rgba(255,255,255,0.55);letter-spacing:1.5px;text-transform:uppercase;margin-top:4px;}

  /* CMD PHOTO */
  .hero-right{display:flex;flex-direction:column;align-items:center;justify-content:center;animation:fadeInRight 1s ease 0.3s both;}
  .cmd-frame{
    position:relative;width:340px;
    border-radius:16px;overflow:hidden;
    box-shadow:0 20px 60px rgba(0,0,0,0.5);
  }
  .cmd-frame img{width:100%;display:block;object-fit:cover;filter:brightness(0.92);}
  .cmd-overlay{
    position:absolute;bottom:0;left:0;width:100%;
    background:linear-gradient(to top,rgba(13,19,32,0.98) 0%,transparent 60%);
    padding:24px 20px 20px;
  }
  .cmd-name{font-family:'Montserrat',sans-serif;font-size:18px;font-weight:900;margin-bottom:4px;}
  .cmd-title{font-size:11px;color:var(--orange);letter-spacing:2px;font-weight:700;}
  .cmd-frame::before{
    content:'';position:absolute;top:0;left:0;right:0;bottom:0;
    border:2px solid transparent;border-radius:16px;
    background:linear-gradient(135deg,var(--orange),transparent,var(--navy)) border-box;
    -webkit-mask:linear-gradient(#fff 0 0) padding-box,linear-gradient(#fff 0 0);
    -webkit-mask-composite:destination-out;mask-composite:exclude;
    z-index:1;pointer-events:none;
  }

  /* TICKER */
  .ticker{
    background:var(--orange);padding:10px 0;overflow:hidden;
    position:relative;z-index:10;
  }
  .ticker-inner{
    display:flex;white-space:nowrap;
    animation:ticker-scroll 30s linear infinite;
    width:max-content;
  }
  .ticker-item{
    font-size:12px;font-weight:700;letter-spacing:2px;text-transform:uppercase;
    padding:0 40px;color:var(--white);
    display:flex;align-items:center;gap:12px;
  }
  .ticker-item::after{content:'◆';color:rgba(255,255,255,0.5);font-size:8px;}

  /* SECTION BASE */
  section{padding:90px 0;}
  .section-inner{max-width:1200px;margin:0 auto;padding:0 40px;}
  .section-eyebrow{
    font-size:11px;font-weight:700;letter-spacing:4px;text-transform:uppercase;
    color:var(--orange);margin-bottom:12px;
  }
  .section-title{
    font-family:'Montserrat',sans-serif;font-size:36px;font-weight:900;
    line-height:1.15;margin-bottom:16px;
  }
  .section-line{
    width:52px;height:3px;background:var(--orange);
    margin:0 0 40px;border-radius:2px;
  }
  .section-line.center{margin:0 auto 40px;}
  .text-center{text-align:center;}

  /* ABOUT */
  .about{background:var(--dark);}
  .about-grid{display:grid;grid-template-columns:1fr 1fr;gap:70px;align-items:center;}
  .about-visual{position:relative;}
  .about-card{
    background:linear-gradient(135deg,var(--navy),#0f1829);
    border:1px solid rgba(232,91,30,0.2);
    border-radius:16px;padding:36px;
    position:relative;overflow:hidden;
  }
  .about-card::before{
    content:'';position:absolute;top:-40px;right:-40px;
    width:120px;height:120px;border-radius:50%;
    background:rgba(232,91,30,0.08);
  }
  .about-since{
    font-family:'Montserrat',sans-serif;font-size:80px;font-weight:900;
    color:rgba(232,91,30,0.08);position:absolute;bottom:10px;right:20px;
    line-height:1;
  }
  .about-badges{display:flex;flex-direction:column;gap:14px;margin-top:20px;}
  .badge{
    display:flex;align-items:center;gap:12px;
    background:rgba(255,255,255,0.04);border:1px solid rgba(255,255,255,0.08);
    border-radius:8px;padding:12px 16px;
    transition:border-color 0.3s,transform 0.3s;cursor:default;
  }
  .badge:hover{border-color:var(--orange);transform:translateX(6px);}
  .badge-icon{width:36px;height:36px;background:rgba(232,91,30,0.15);border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:18px;flex-shrink:0;}
  .badge-text h4{font-size:13px;font-weight:700;margin-bottom:2px;}
  .badge-text p{font-size:11px;color:rgba(255,255,255,0.5);}
  .about-text p{color:rgba(255,255,255,0.72);line-height:1.8;margin-bottom:20px;font-size:15px;}
  .reg-list{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:24px;}
  .reg-item{
    background:rgba(232,91,30,0.06);border:1px solid rgba(232,91,30,0.15);
    border-radius:6px;padding:10px 14px;
    font-size:11px;color:rgba(255,255,255,0.65);
  }
  .reg-item strong{display:block;color:var(--orange);font-size:10px;letter-spacing:1px;margin-bottom:3px;}

  /* SERVICES */
  .services{background:linear-gradient(180deg,var(--dark) 0%,#0f1829 100%);}
  .services-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:28px;}
  .service-card{
    background:linear-gradient(135deg,rgba(26,34,64,0.8),rgba(13,19,32,0.9));
    border:1px solid rgba(255,255,255,0.08);
    border-radius:14px;padding:36px 28px;
    transition:all 0.4s;position:relative;overflow:hidden;
    cursor:default;
  }
  .service-card::before{
    content:'';position:absolute;top:0;left:0;width:3px;height:0;
    background:linear-gradient(to bottom,var(--orange),var(--accent));
    transition:height 0.4s;border-radius:3px 0 0 3px;
  }
  .service-card:hover::before{height:100%;}
  .service-card:hover{border-color:rgba(232,91,30,0.3);transform:translateY(-6px);box-shadow:0 20px 40px rgba(0,0,0,0.3);}
  .service-icon{
    width:60px;height:60px;background:rgba(232,91,30,0.12);
    border-radius:14px;display:flex;align-items:center;justify-content:center;
    font-size:28px;margin-bottom:20px;transition:background 0.3s;
  }
  .service-card:hover .service-icon{background:rgba(232,91,30,0.22);}
  .service-card h3{font-family:'Montserrat',sans-serif;font-size:17px;font-weight:800;margin-bottom:12px;}
  .service-card p{font-size:13.5px;color:rgba(255,255,255,0.6);line-height:1.7;}

  /* ONGOING PROJECTS */
  .projects{background:var(--navy);}
  .projects-title-area{margin-bottom:50px;}
  .ongoing-grid{display:grid;grid-template-columns:1fr 1fr;gap:30px;margin-bottom:50px;}
  .project-card{
    background:linear-gradient(135deg,rgba(13,19,32,0.9),rgba(26,34,64,0.5));
    border:1px solid rgba(232,91,30,0.25);
    border-radius:16px;padding:36px;position:relative;overflow:hidden;
  }
  .project-card::after{
    content:'';position:absolute;top:0;right:0;width:100px;height:100px;
    background:radial-gradient(circle,rgba(232,91,30,0.12) 0%,transparent 70%);
  }
  .project-badge{
    display:inline-block;background:var(--orange);color:var(--white);
    font-size:9px;font-weight:800;letter-spacing:2px;text-transform:uppercase;
    padding:5px 12px;border-radius:50px;margin-bottom:16px;
    animation:pulse-badge 2s infinite;
  }
  .project-card h3{font-family:'Montserrat',sans-serif;font-size:19px;font-weight:800;margin-bottom:12px;line-height:1.3;}
  .project-card p{font-size:13.5px;color:rgba(255,255,255,0.65);line-height:1.7;}
  .project-meta{
    display:flex;gap:20px;margin-top:20px;flex-wrap:wrap;
  }
  .project-meta-item{
    display:flex;align-items:center;gap:6px;
    font-size:12px;color:var(--orange);font-weight:600;
  }
  .progress-bar-wrap{margin-top:18px;}
  .progress-label{display:flex;justify-content:space-between;font-size:11px;color:rgba(255,255,255,0.5);margin-bottom:6px;}
  .progress-bar{height:4px;background:rgba(255,255,255,0.1);border-radius:2px;overflow:hidden;}
  .progress-fill{height:100%;background:linear-gradient(to right,var(--orange),var(--accent));border-radius:2px;animation:progress-grow 2s ease 0.5s both;}

  /* PAST CLIENTS */
  .clients{background:var(--dark);padding:70px 0;}
  .clients-scroll{display:flex;gap:24px;flex-wrap:wrap;justify-content:center;margin-top:40px;}
  .client-chip{
    background:rgba(255,255,255,0.04);border:1px solid rgba(255,255,255,0.1);
    border-radius:50px;padding:12px 24px;font-size:13px;font-weight:600;
    color:rgba(255,255,255,0.7);transition:all 0.3s;white-space:nowrap;
  }
  .client-chip:hover{background:rgba(232,91,30,0.1);border-color:var(--orange);color:var(--white);}

  /* FEATURED CLIENTS */
  .featured-clients{display:grid;grid-template-columns:repeat(2,1fr);gap:24px;margin-bottom:0;}
  .featured-client-card{
    display:flex;align-items:center;gap:20px;
    background:linear-gradient(135deg,rgba(26,34,64,0.9),rgba(13,19,32,0.8));
    border:1px solid rgba(255,255,255,0.1);border-radius:14px;padding:22px 24px;
    transition:all 0.35s;cursor:default;
  }
  .featured-client-card:hover{border-color:rgba(232,91,30,0.4);transform:translateY(-4px);box-shadow:0 16px 40px rgba(0,0,0,0.3);}
  .fc-logo-wrap{width:80px;height:60px;flex-shrink:0;display:flex;align-items:center;justify-content:center;background:rgba(255,255,255,0.06);border-radius:10px;overflow:hidden;padding:8px;}
  .fc-logo-img{max-width:100%;max-height:100%;object-fit:contain;filter:brightness(1.1);}
  .fc-logo-fallback{width:100%;height:100%;align-items:center;justify-content:center;border-radius:10px;}
  .fc-abbr{font-family:'Montserrat',sans-serif;font-size:13px;font-weight:900;color:#fff;padding:10px 12px;border-radius:8px;letter-spacing:1px;}
  .fc-info h4{font-family:'Montserrat',sans-serif;font-size:14px;font-weight:800;margin-bottom:5px;line-height:1.3;}
  .fc-info p{font-size:11.5px;color:rgba(255,255,255,0.5);margin-bottom:8px;line-height:1.4;}
  .fc-tag{display:inline-block;background:rgba(232,91,30,0.12);border:1px solid rgba(232,91,30,0.25);color:var(--orange);font-size:9.5px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;padding:3px 10px;border-radius:50px;}
  @media(max-width:700px){.featured-clients{grid-template-columns:1fr;}}

  /* MACHINERY */
  .machinery{background:linear-gradient(180deg,#0f1829 0%,var(--dark) 100%);}
  .machinery-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:16px;}
  .machine-item{
    background:rgba(255,255,255,0.03);border:1px solid rgba(255,255,255,0.07);
    border-radius:10px;padding:18px 14px;text-align:center;
    transition:all 0.3s;
  }
  .machine-item:hover{background:rgba(232,91,30,0.08);border-color:rgba(232,91,30,0.3);transform:translateY(-4px);}
  .machine-icon{font-size:26px;margin-bottom:10px;}
  .machine-item h4{font-size:12px;font-weight:700;margin-bottom:4px;}
  .machine-item p{font-size:11px;color:rgba(255,255,255,0.45);}

  /* CMD SECTION */
  .cmd-section{
    background:linear-gradient(135deg,var(--navy) 0%,var(--dark) 100%);
    position:relative;overflow:hidden;
  }
  .cmd-section::before{
    content:'';position:absolute;top:-100px;left:-100px;
    width:400px;height:400px;border-radius:50%;
    background:radial-gradient(circle,rgba(232,91,30,0.08),transparent 70%);
  }
  .cmd-inner{display:grid;grid-template-columns:1fr 1.4fr;gap:70px;align-items:center;}
  .cmd-photo-wrap{position:relative;}
  .cmd-photo{
    border-radius:20px;overflow:hidden;
    box-shadow:0 30px 70px rgba(0,0,0,0.5);
    position:relative;
  }
  .cmd-photo img{width:100%;display:block;filter:brightness(0.88) contrast(1.05);}
  .cmd-photo::after{
    content:'CMD & FOUNDER';
    position:absolute;bottom:0;left:0;width:100%;
    background:linear-gradient(to top,rgba(13,19,32,0.98),transparent);
    padding:40px 24px 20px;
    font-family:'Montserrat',sans-serif;font-size:11px;font-weight:800;
    letter-spacing:3px;color:var(--orange);
  }
  .cmd-quote{
    border-left:3px solid var(--orange);
    padding-left:24px;margin:24px 0;
    font-size:16px;font-style:italic;color:rgba(255,255,255,0.8);
    line-height:1.7;
  }
  .cmd-text p{color:rgba(255,255,255,0.7);line-height:1.8;font-size:15px;margin-bottom:16px;}
  .cmd-sig{margin-top:28px;}
  .cmd-sig h3{font-family:'Montserrat',sans-serif;font-size:22px;font-weight:900;margin-bottom:4px;}
  .cmd-sig p{color:var(--orange);font-size:12px;letter-spacing:2px;font-weight:700;}

  /* CONTACT */
  .contact{background:var(--dark);}
  .contact-grid{display:grid;grid-template-columns:1fr 1fr;gap:60px;}
  .contact-info{display:flex;flex-direction:column;gap:20px;}
  .contact-item{
    display:flex;align-items:flex-start;gap:16px;
    padding:20px;background:rgba(255,255,255,0.03);
    border:1px solid rgba(255,255,255,0.07);border-radius:10px;
    transition:border-color 0.3s;
  }
  .contact-item:hover{border-color:var(--orange);}
  .contact-icon{
    width:44px;height:44px;background:rgba(232,91,30,0.12);
    border-radius:10px;display:flex;align-items:center;justify-content:center;
    font-size:20px;flex-shrink:0;
  }
  .contact-item h4{font-size:12px;color:var(--orange);font-weight:700;letter-spacing:1.5px;text-transform:uppercase;margin-bottom:6px;}
  .contact-item p{font-size:14px;color:rgba(255,255,255,0.75);line-height:1.5;}
  .contact-form{background:rgba(255,255,255,0.03);border:1px solid rgba(255,255,255,0.08);border-radius:16px;padding:36px;}
  .form-group{margin-bottom:20px;}
  .form-group label{display:block;font-size:11px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;color:rgba(255,255,255,0.55);margin-bottom:8px;}
  .form-group input,.form-group textarea,.form-group select{
    width:100%;background:rgba(255,255,255,0.05);border:1px solid rgba(255,255,255,0.12);
    border-radius:8px;padding:13px 16px;color:var(--white);font-size:14px;
    font-family:'Open Sans',sans-serif;outline:none;transition:border-color 0.3s;
    -webkit-appearance:none;
  }
  .form-group input:focus,.form-group textarea:focus,.form-group select:focus{border-color:var(--orange);}
  .form-group textarea{resize:vertical;min-height:110px;}
  .form-group select option{background:var(--dark);}
  .form-row{display:grid;grid-template-columns:1fr 1fr;gap:16px;}

  /* FOOTER */
  footer{
    background:#060a10;border-top:1px solid rgba(232,91,30,0.2);
    padding:50px 0 20px;
  }
  .footer-inner{max-width:1200px;margin:0 auto;padding:0 40px;}
  .footer-top{display:grid;grid-template-columns:1.5fr 1fr 1fr;gap:50px;margin-bottom:40px;}
  .footer-brand p{font-size:13.5px;color:rgba(255,255,255,0.5);line-height:1.75;margin-top:14px;}
  .footer-col h4{font-size:12px;font-weight:800;letter-spacing:2px;text-transform:uppercase;color:var(--orange);margin-bottom:18px;}
  .footer-links{list-style:none;display:flex;flex-direction:column;gap:10px;}
  .footer-links a{font-size:13.5px;color:rgba(255,255,255,0.5);text-decoration:none;transition:color 0.3s;}
  .footer-links a:hover{color:var(--orange);}
  .footer-bottom{border-top:1px solid rgba(255,255,255,0.06);padding-top:20px;display:flex;justify-content:space-between;align-items:center;flex-wrap:gap;}
  .footer-bottom p{font-size:12px;color:rgba(255,255,255,0.35);}
  .footer-bottom span{color:var(--orange);}

  /* SCROLL REVEAL */
  .reveal{opacity:0;transform:translateY(30px);transition:opacity 0.7s ease,transform 0.7s ease;}
  .reveal.visible{opacity:1;transform:translateY(0);}
  .reveal-left{opacity:0;transform:translateX(-30px);transition:opacity 0.7s ease,transform 0.7s ease;}
  .reveal-left.visible{opacity:1;transform:translateX(0);}
  .reveal-right{opacity:0;transform:translateX(30px);transition:opacity 0.7s ease,transform 0.7s ease;}
  .reveal-right.visible{opacity:1;transform:translateX(0);}

  /* ANIMATIONS */
  @keyframes fadeInDown{from{opacity:0;transform:translateY(-20px);}to{opacity:1;transform:translateY(0);}}
  @keyframes fadeInUp{from{opacity:0;transform:translateY(30px);}to{opacity:1;transform:translateY(0);}}
  @keyframes fadeInRight{from{opacity:0;transform:translateX(30px);}to{opacity:1;transform:translateX(0);}}
  @keyframes ticker-scroll{from{transform:translateX(0);}to{transform:translateX(-50%);};}
  @keyframes pulse-dot{0%,100%{opacity:1;}50%{opacity:0.3;}}
  @keyframes pulse-badge{0%,100%{box-shadow:0 0 0 0 rgba(232,91,30,0.4);}70%{box-shadow:0 0 0 8px rgba(232,91,30,0);}}
  @keyframes progress-grow{from{width:0;}to{width:var(--progress-width);}}
  @keyframes float{0%,100%{transform:translateY(0);}50%{transform:translateY(-12px);}}

  /* RESPONSIVE */
  @media(max-width:900px){
    .hero-content,.about-grid,.services-grid,.ongoing-grid,.cmd-inner,.contact-grid,.footer-top{grid-template-columns:1fr;}
    .hero-right{order:-1;}
    .cmd-frame,.cmd-photo-wrap{max-width:400px;margin:0 auto;}
    .machinery-grid{grid-template-columns:repeat(2,1fr);}
    .reg-list{grid-template-columns:1fr;}
    .nav-links{display:none;}
    .hamburger{display:flex;}
    .form-row{grid-template-columns:1fr;}
    .services-grid{grid-template-columns:1fr 1fr;}
  }
  @media(max-width:600px){
    nav{padding:0 20px;}
    .section-inner{padding:0 20px;}
    .hero-content{padding:0 20px;}
    .hero-title{font-size:28px;}
    .section-title{font-size:26px;}
    .services-grid{grid-template-columns:1fr;}
    .machinery-grid{grid-template-columns:repeat(2,1fr);}
    .hero-stats{grid-template-columns:repeat(3,1fr);}
    .stat-num{font-size:22px;}
    footer .footer-inner{padding:0 20px;}
  }

  /* MOBILE NAV */
  .mobile-menu{
    display:none;position:fixed;top:72px;left:0;width:100%;
    background:rgba(13,19,32,0.98);backdrop-filter:blur(12px);
    z-index:999;padding:20px;flex-direction:column;gap:2px;
    border-bottom:1px solid rgba(232,91,30,0.2);
  }
  .mobile-menu.open{display:flex;}
  .mobile-menu a{display:block;padding:14px 20px;color:rgba(255,255,255,0.8);text-decoration:none;font-size:14px;font-weight:600;letter-spacing:1px;border-radius:6px;transition:background 0.3s;}
  .mobile-menu a:hover{background:rgba(232,91,30,0.1);color:var(--orange);}

  /* LOGO SVG inline */
  .logo-inline{display:flex;align-items:center;gap:10px;}
</style>
</head>
<body>

<!-- NAVBAR -->
<nav id="navbar">
  <div class="nav-logo">
    <svg class="logo-svg" viewBox="0 0 80 80" xmlns="http://www.w3.org/2000/svg">
      <circle cx="26" cy="40" r="22" fill="#E85B1E" opacity="0.15"/>
      <circle cx="26" cy="40" r="16" fill="#E85B1E"/>
      <text x="18" y="46" font-family="Georgia,serif" font-size="20" font-weight="bold" fill="white">M</text>
      <!-- swooshes -->
      <path d="M20 12 Q55 5 78 20" stroke="#E85B1E" stroke-width="4" fill="none" stroke-linecap="round"/>
      <path d="M20 18 Q55 11 78 26" stroke="#1A2240" stroke-width="3" fill="none" stroke-linecap="round"/>
      <path d="M20 24 Q55 17 78 32" stroke="#E85B1E" stroke-width="2.5" fill="none" stroke-linecap="round"/>
    </svg>
    <div class="nav-brand">
      <h1>Maa Nirmala Group</h1>
      <span>Way of Success</span>
    </div>
  </div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#machinery">Machinery</a></li>
    <li><a href="#leadership">Leadership</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a href="#contact" class="nav-cta">Get In Touch</a>
  <div class="hamburger" onclick="toggleMenu()">
    <span></span><span></span><span></span>
  </div>
</nav>
<div class="mobile-menu" id="mobileMenu">
  <a href="#about" onclick="toggleMenu()">About</a>
  <a href="#services" onclick="toggleMenu()">Services</a>
  <a href="#projects" onclick="toggleMenu()">Projects</a>
  <a href="#machinery" onclick="toggleMenu()">Machinery</a>
  <a href="#leadership" onclick="toggleMenu()">Leadership</a>
  <a href="#contact" onclick="toggleMenu()">Contact</a>
</div>

<!-- HERO -->
<section class="hero" id="home">
  <canvas id="hero-canvas"></canvas>
  <div class="hero-diagonal"></div>
  <div class="hero-content">
    <div class="hero-left">
      <div class="hero-eyebrow">🏗️ India's Trusted Infrastructure Partner</div>
      <div class="hero-title">Maa Nirmala <span>Business</span> Consulting <span>Pvt. Ltd.</span></div>
      <div class="hero-subtitle">Way of Success — Est. 2008</div>
      <p class="hero-desc">Building the Nation's backbone — from 6-Lane Expressways and NHAI Road Projects to Coal Mining, Transportation, Security Services and Manpower Supply across India and Abroad.</p>
      <div class="hero-btns">
        <a href="#projects" class="btn-primary">🚧 View Live Projects</a>
        <a href="#contact" class="btn-outline">Contact Us</a>
      </div>
      <div class="hero-stats">
        <div class="stat-item">
          <div class="stat-num" data-target="17">0</div>
          <div class="stat-label">Years of Excellence</div>
        </div>
        <div class="stat-item">
          <div class="stat-num" data-target="500">0</div>
          <div class="stat-label">+ Skilled Staff</div>
        </div>
        <div class="stat-item">
          <div class="stat-num" data-target="90">0</div>
          <div class="stat-label">Cr+ Projects</div>
        </div>
      </div>
    </div>
    <div class="hero-right">
      <div class="cmd-frame" style="animation:float 6s ease-in-out infinite;">
        <img src="data:image/jpeg;base64,iVBORw0KGgoAAAANSUhEUgAABXoAAARiCAIAAACVptgUAABhWmNhQlgAAGFaanVtYgAAAB5qdW1kYzJwYQARABCAAACqADibcQNjMnBhAAAAYTRqdW1iAAAAR2p1bWRjMm1hABEAEIAAAKoAOJtxA3VybjpjMnBhOmZmOTA2ZjdkLTdhYWYtNDY1NC1hMmI0LWRkNjk3ZGY3YWU2OQAAABf9anVtYgAAAClqdW1kYzJhcwARABCAAACqADibcQNjMnBhLmFzc2VydGlvbnMAAAAJ0Wp1bWIAAAA7anVtZEDLDDK7ikidpwsq1vR/Q2kTYzJwYS5pY29uAAAAABhjMnNoZpeHFn5md8VFLpbW2nI2agAAABdiZmRiAGltYWdlL3N2Zyt4bWwAAAAJd2JpZGI8c3ZnIHdpZHRoPSI3MTYiIGhlaWdodD0iNzE2IiB2aWV3Qm94PSIwIDAgNzE2IDcxNiIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTUwOC43NDkgMzE3LjM5OUM1MTYuNzc3IDI4Ny4zMTQgNTA4Ljk5MSAyNTMuODg0IDQ4NS4zODkgMjMwLjI4MkM0NjEuNzg4IDIwNi42ODEgNDI4LjM2IDE5OC44OTUgMzk4LjI3MyAyMDYuOTIzQzM3Ni4yMzEgMTg0LjkyOCAzNDMuMzkgMTc0Ljk1NiAzMTEuMTQ4IDE4My41OTZDMjc4LjkwNiAxOTIuMjM0IDI1NS40NSAyMTcuMjkyIDI0Ny4zNiAyNDcuMzYxQzIxNy4yOTEgMjU1LjQ1MSAxOTIuMjMzIDI3OC45MSAxODMuNTk1IDMxMS4xNDlDMTc0Ljk1NyAzNDMuMzkxIDE4NC45MjcgMzc2LjIzMiAyMDYuOTI0IDM5OC4yNzRDMTk4Ljg5NiA0MjguMzU5IDIwNi42ODMgNDYxLjc4OSAyMzAuMjg0IDQ4NS4zOTFDMjUzLjg4NSA1MDguOTkyIDI4Ny4zMTMgNTE2Ljc3OSAzMTcuNDAxIDUwOC43NUMzMzkuNDQyIDUzMC43NDUgMzcyLjI4NiA1NDAuNzE3IDQwNC41MjUgNTMyLjA3OUM0MzYuNzY3IDUyMy40NDEgNDYwLjIyMyA0OTguMzg0IDQ2OC4zMTMgNDY4LjMxNUM0OTguMzgzIDQ2MC4yMjQgNTIzLjQ0IDQzNi43NjYgNTMyLjA3OCA0MDQuNTI2QzU0MC43MTYgMzcyLjI4NSA1MzAuNzQ3IDMzOS40NDMgNTA4Ljc0OSAzMTcuNDAyVjMxNy4zOTlaTTQ3MC44OTkgMjQ0Ljc3NkM0ODYuODkyIDI2MC43NyA0OTMuNDg4IDI4Mi42MDEgNDkwLjY4NyAzMDMuNDEyTDQxNS41NzcgMjYwLjA0NkM0MTIuNDExIDI1OC4yMTggNDA4LjUwOSAyNTguMjE4IDQwNS4zNDUgMjYwLjA0NkwzMTcuNDAxIDMxMC44MlYyNzcuNTI2QzMxNy40MDEgMjc1LjE5MSAzMTguNjUyIDI3My4wMDUgMzIwLjY3NiAyNzEuODM3TDM4Ny42NDQgMjMzLjE3NEM0MTQuMTc4IDIxOC4zNTMgNDQ4LjM0NiAyMjIuMjIzIDQ3MC45MDEgMjQ0Ljc3Nkg0NzAuODk5Wk0zNTcuODM3IDMxMS4xNDRMMzk4LjI3NSAzMzQuNDkxVjM4MS4xODVMMzU3LjgzNyA0MDQuNTMyTDMxNy4zOTggMzgxLjE4NVYzMzQuNDkxTDM1Ny44MzcgMzExLjE0NFpNMjY0Ljc3NiAyNjkuNjkzQzI2NS4yMDcgMjM5LjMwNSAyODUuNjQ0IDIxMS42NDkgMzE2LjQ1MyAyMDMuMzkzQzMzOC4zIDE5Ny41NCAzNjAuNTA1IDIwMi43NDQgMzc3LjEyNyAyMTUuNTczTDMwMi4wMTQgMjU4LjkzN0MyOTguODQ4IDI2MC43NjQgMjk2Ljg5OCAyNjQuMTQ0IDI5Ni44OTggMjY3Ljc5OFYzNjkuMzQ2TDI2OC4wNjUgMzUyLjY5OUMyNjYuMDQzIDM1MS41MzEgMjY0Ljc3NiAzNDkuMzUzIDI2NC43NzYgMzQ3LjAxN1YyNjkuNjkxVjI2OS42OTNaTTIwMy4zOTEgMzE2LjQ1NEMyMDkuMjQ0IDI5NC42MDggMjI0Ljg1NCAyNzcuOTc4IDI0NC4yNzYgMjY5Ljk5OVYzNTYuNzNDMjQ0LjI3NiAzNjAuMzg0IDI0Ni4yMjYgMzYzLjc2MyAyNDkuMzkyIDM2NS41OTFMMzM3LjMzNyA0MTYuMzY1TDMwOC41MDMgNDMzLjAxM0MzMDYuNDgxIDQzNC4xODEgMzAzLjk2MSA0MzQuMTg4IDMwMS45MzkgNDMzLjAyTDIzNC45NzEgMzk0LjM1N0MyMDguODY4IDM3OC43ODkgMTk1LjEzOCAzNDcuMjYxIDIwMy4zOTEgMzE2LjQ1NFpNMjQ0Ljc3NSA0NzAuOUMyMjguNzgxIDQ1NC45MDYgMjIyLjE4NiA0MzMuMDc1IDIyNC45ODYgNDEyLjI2NEwzMDAuMDk2IDQ1NS42M0MzMDMuMjYzIDQ1Ny40NTcgMzA3LjE2NCA0NTcuNDU3IDMxMC4zMjggNDU1LjYzTDM5OC4yNzMgNDA0Ljg1NlY0MzguMTQ5QzM5OC4yNzMgNDQwLjQ4NSAzOTcuMDIyIDQ0Mi42NzEgMzk0Ljk5NyA0NDMuODM5TDMyOC4wMjkgNDgyLjUwMkMzMDEuNDk1IDQ5Ny4zMjIgMjY3LjMyNyA0OTMuNDUyIDI0NC43NzIgNDcwLjlIMjQ0Ljc3NVpNNDUwLjg5NyA0NDUuOTgyQzQ1MC40NjYgNDc2LjM3MSA0MzAuMDI5IDUwNC4wMjcgMzk5LjIyIDUxMi4yODNDMzc3LjM3MyA1MTguMTM2IDM1NS4xNjggNTEyLjkzMiAzMzguNTQ3IDUwMC4xMDJMNDEzLjY1OSA0NTYuNzM4QzQxNi44MjYgNDU0LjkxMSA0MTguNzc1IDQ1MS41MzIgNDE4Ljc3NSA0NDcuODc3VjM0Ni4zMjlMNDQ3LjYwOSAzNjIuOTc3QzQ0OS42MzEgMzY0LjE0NSA0NTAuODk3IDM2Ni4zMjMgNDUwLjg5NyAzNjguNjU5VjQ0NS45ODVWNDQ1Ljk4MlpNNTEyLjI4MiAzOTkuMjIxQzUwNi40MjkgNDIxLjA2OCA0OTAuODE5IDQzNy42OTcgNDcxLjM5NyA0NDUuNjc2VjM1OC45NDZDNDcxLjM5NyAzNTUuMjkyIDQ2OS40NDggMzUxLjkxMiA0NjYuMjgxIDM1MC4wODVMMzc4LjMzNiAyOTkuMzExTDQwNy4xNyAyODIuNjYzQzQwOS4xOTIgMjgxLjQ5NSA0MTEuNzEyIDI4MS40ODcgNDEzLjczNCAyODIuNjU1TDQ4MC43MDIgMzIxLjMxOEM1MDYuODA1IDMzNi44ODcgNTIwLjUzNiAzNjguNDE1IDUxMi4yODIgMzk5LjIyMVoiIGZpbGw9ImJsYWNrIi8+Cjwvc3ZnPgoAAAF+anVtYgAAAEFqdW1kY2JvcgARABCAAACqADibcRNjMnBhLmFjdGlvbnMudjIAAAAAGGMyc2iHD5UUymyON60hGqYUU65QAAABNWNib3KhZ2FjdGlvbnODpGZhY3Rpb25sYzJwYS5jcmVhdGVkZHdoZW7AdDIwMjYtMDYtMjRUMDA6MDA6MDBabXNvZnR3YXJlQWdlbnSiZG5hbWVpZ3B0LWltYWdlZ3ZlcnNpb25jMi4wcWRpZ2l0YWxTb3VyY2VUeXBleEZodHRwOi8vY3YuaXB0Yy5vcmcvbmV3c2NvZGVzL2RpZ2l0YWxzb3VyY2V0eXBlL3RyYWluZWRBbGdvcml0aG1pY01lZGlhomZhY3Rpb25uYzJwYS5jb252ZXJ0ZWRkd2hlbsB0MjAyNi0wNi0yNFQwMDowMDowMFqiZmFjdGlvbngYYzJwYS53YXRlcm1hcmtlZC51bmJvdW5kZHdoZW7AdDIwMjYtMDYtMjRUMDA6MDA6MDBaAAALump1bWIAAABJanVtZGNib3IAEQAQgAAAqgA4m3ETYzJwYS5jZXJ0aWZpY2F0ZS1zdGF0dXMAAAAAGGMyc2j35S13abG+STqVf4d6kW7uAAALaWNib3KhaG9jc3BWYWxzgnkFhE1JSUVIZ29CQUtDQ0JCY3dnZ1FUQmdrckJnRUZCUWN3QVFFRWdnUUVNSUlFQURDQm9xSVdCQlNEREpGTmMrOU9VZ1ZVU0dzclFwU0ZjenpkL0JnUE1qQXlOakEyTWpNeE56VTNORFphTUhjd2RUQk5NQWtHQlNzT0F3SWFCUUFFRkQ1TWZJNVFDNGRzY3hXK3IyNlg2aER1bENESkJCVERzeVNXTkpPaFdlcFNHR3VlRitDcHV0YXdUQUlVVXBRbEI0RzFhb2I1TXhkNGNOYU9yZTlpR2tHQUFCZ1BNakF5TmpBMk1qTXhOelUzTkRSYW9CRVlEekl3TWpZd05qTXdNVGMxTnpRMFdqQUtCZ2dxaGtqT1BRUURBZ05KQURCR0FpRUFqY0V3dklNcnlSK0ZwZ0dkci9oVnAxM3Ztbmt6cE5Qc3BROVo2azU2QUJVQ0lRRHVJem9FaUJ2QzFkVHZvVzh3T1IrWUFIQ2gzNUVuM0xIMjFvMnE5dnVLcEtDQ0F3QXdnZ0w4TUlJQytEQ0NBbjZnQXdJQkFnSVVZRUFKekozU1BmRy9QMmxleVhnWFNVenZLVEF3Q2dZSUtvWkl6ajBFQXdNd2dhY3hDekFKQmdOVkJBWVRBbFZUTVJFd0R3WURWUVFJREFoT1pYY2dXVzl5YXpFUk1BOEdBMVVFQnd3SVRtVjNJRmx2Y21zeEV6QVJCZ05WQkFvTUNsUnlkV1p2SUVsdVl5NHhGREFTQmdOVkJBc01DME5CSUVScGRtbHphVzl1TVJvd0dBWUpLb1pJaHZjTkFRa0JGZ3RqWVVCMGNuVm1ieTVoYVRFck1Da0dBMVVFQXd3aVZISjFabThnUXpKUVFTQkRiR0ZwYlNCVGFXZHVhVzVuSUVOQklDZ3lNREkxS1RBZUZ3MHlOakEyTVRjd01EQXpNakZhRncweU5qQTNNVGN3TURBek1qRmFNSUdsTVFzd0NRWURWUVFHRXdKVlV6RVJNQThHQTFVRUNBd0lUbVYzSUZsdmNtc3hFVEFQQmdOVkJBY01DRTVsZHlCWmIzSnJNUk13RVFZRFZRUUtEQXBVY25WbWJ5QkpibU11TVJRd0VnWURWUVFMREF0RFFTQkVhWFpwYzJsdmJqRWFNQmdHQ1NxR1NJYjNEUUVKQVJZTFkyRkFkSEoxWm04dVlXa3hLVEFuQmdOVkJBTU1JRlJ5ZFdadklFTXlVRUVnVDBOVFVDQlNaWE53YjI1a1pYSWdLREl3TWpVcE1Ga3dFd1lIS29aSXpqMENBUVlJS29aSXpqMERBUWNEUWdBRTc3ODRCQ3cwcS9KTnNQZG5sSDdXU0tocUVENnF0WDdYdGZ5eVdaK1FvbGxZa0hGUk5lUjNCU3pXTVpzYThvK0FYR1BJclNtSUNBekEyRFhEZG1DNkdhT0JoekNCaERBZEJnTlZIUTRFRmdRVWd3eVJUWFB2VGxJRlZFaHJLMEtVaFhNODNmd3dId1lEVlIwakJCZ3dGb0FVdzdNa2xqU1RvVm5xVWhocm5oZmdxYnJXc0V3d0RBWURWUjBUQVFIL0JBSXdBREFPQmdOVkhROEJBZjhFQkFNQ0I0QXdFd1lEVlIwbEJBd3dDZ1lJS3dZQkJRVUhBd2t3RHdZSkt3WUJCUVVITUFFRkJBSUZBREFLQmdncWhrak9QUVFEQXdOb0FEQmxBakVBbVdOaCt4L21pdGtaT1Z5T2Y5MFZha1NCZkQ0TkRGK2NSMnhwNmQ5eGx3anFaZWdEblZvR2loZ0ltakduclZWN0FqQk9Oeno2UzRHNEl3VllHaytUbWFFOW16V0RHOXlFYWhkSnRoYVAzNmdRUmRDdnY2bS9paExZVzZManVhZFliMnc9eQXMTUlJRVV3b0JBS0NDQkV3d2dnUklCZ2tyQmdFRkJRY3dBUUVFZ2dRNU1JSUVOVENCb3FJV0JCVEwySTQyaWlFUmN5eTU3NG9hbzJxZXZGTk1RQmdQTWpBeU5qQTJNak14TnpVNE1qRmFNSGN3ZFRCTk1Ba0dCU3NPQXdJYUJRQUVGSUFnOWJ6aUpPbHR2Tlp2eGhjcFpYd2t5UEg5QkJRRDFWK3Zmb1BsQkIxWmdDZEtOUDlGL2V0SmVBSVVNT2loOEtXSlFtdlN1WUpJUjVrWjNCWTNBc3VBQUJnUE1qQXlOakEyTWpNeE56VTRNakZhb0JFWUR6SXdNall3TmpNd01UYzFPREl4V2pBS0JnZ3Foa2pPUFFRREF3Tm5BREJrQWpBc2N3eVZLQWQ2cjFrbm96YXNUZXF5NTNKRnFvWW5vT1U0cGhJMno4Y2x4SlFzNzM5WDlOa2R6ZjRBT0d0SnFTNENNR2VPSVFXMFRTNjRobEtEaGhyNHBLb3hhMnI3RldBKzByRTZYb25rVVpvV3FSZlBURll0U2J5aXA0R2lBbXRweXFDQ0F4Y3dnZ01UTUlJRER6Q0NBcFdnQXdJQkFnSVVBOUI5TkpKdFZ4bHd4dGdVa0V4enhkUGxtK0F3Q2dZSUtvWkl6ajBFQXdNd2dhZ3hDekFKQmdOVkJBWVRBbFZUTVJFd0R3WURWUVFJREFoT1pYY2dXVzl5YXpFUk1BOEdBMVVFQnd3SVRtVjNJRmx2Y21zeEV6QVJCZ05WQkFvTUNsUnlkV1p2SUVsdVl5NHhGREFTQmdOVkJBc01DME5CSUVScGRtbHphVzl1TVJvd0dBWUpLb1pJaHZjTkFRa0JGZ3RqWVVCMGNuVm1ieTVoYVRFc01Db0dBMVVFQXd3alZISjFabThnUXpKUVFTQlNiMjkwSUVOQklDZ3lNREkxTENCRlEwTWdVRE00TkNrd0hoY05Nall3TlRFeE1qTTBNakkxV2hjTk16WXdOVEE0TWpNME1qSTFXakNCbmpFTE1Ba0dBMVVFQmhNQ1ZWTXhFVEFQQmdOVkJBZ01DRTVsZHlCWmIzSnJNUkV3RHdZRFZRUUhEQWhPWlhjZ1dXOXlhekVUTUJFR0ExVUVDZ3dLVkhKMVptOGdTVzVqTGpFVU1CSUdBMVVFQ3d3TFEwRWdSR2wyYVhOcGIyNHhHakFZQmdrcWhraUc5dzBCQ1FFV0MyTmhRSFJ5ZFdadkxtRnBNU0l3SUFZRFZRUUREQmxVY25WbWJ5QlNiMjkwSUU5RFUxQWdVbVZ6Y0c5dVpHVnlNSFl3RUFZSEtvWkl6ajBDQVFZRks0RUVBQ0lEWWdBRVl2ZlhiS0NndGVHczI4aUdJdG5KY3N4N21QZ3Nnd09HdUhUQTJWbG92MXBZK2V3eFY1UVJ4SUZCUzZ5aWY4bFdKY01qN3RwYkk2bXhhc3BXZTZwYlNwZVQxQ2pyZSt2Sk4yVGZQMUpwR0ticllrYzBaQW1jdXdJaFdJSW51UjA1bzRHSE1JR0VNQjBHQTFVZERnUVdCQlRMMkk0MmlpRVJjeXk1NzRvYW8ycWV2Rk5NUURBZkJnTlZIU01FR0RBV2dCUUQxVit2Zm9QbEJCMVpnQ2RLTlA5Ri9ldEplREFNQmdOVkhSTUJBZjhFQWpBQU1BNEdBMVVkRHdFQi93UUVBd0lIZ0RBVEJnTlZIU1VFRERBS0JnZ3JCZ0VGQlFjRENUQVBCZ2tyQmdFRkJRY3dBUVVFQWdVQU1Bb0dDQ3FHU000OUJBTURBMmdBTUdVQ01RRHQ3UitMOTh2TXpoTlR3M3IwR3RETURBOGFCT25FT2xhRk5ab3F2Z2VKc2thWlhrbjh0WWJsVk5aU09zWnB4M3dDTUJjWUpOcmZEOFY4d1pXSjFMVngxTXFzS2VFRHFJaXJMemZ3NlVIK1czNFo0eEp1cmJEcTlCTGVUUFd3VVNQSEdBPT0AAADDanVtYgAAAEBqdW1kY2JvcgARABCAAACqADibcRNjMnBhLmhhc2guZGF0YQAAAAAYYzJzaGSFNlNeQFigOP6P4PP17xQAAAB7Y2JvcqVqZXhjbHVzaW9uc4GiZXN0YXJ0GCFmbGVuZ3RoGWFmZG5hbWVuanVtYmYgbWFuaWZlc3RjYWxnZnNoYTI1NmRoYXNoWCAkCGWQ6/GYdE4Kd718uDdG0AHogG/Mk+cJBIuypDjb82NwYWRIAAAAAAAAAAAAAAMaanVtYgAAACdqdW1kYzJjbAARABCAAACqADibcQNjMnBhLmNsYWltLnYyAAAAAutjYm9ypmppbnN0YW5jZUlEeCx4bXA6aWlkOjY3NDA5N2UzLTRlNjAtNDZkYi04OTcxLWIwNGI0ZjFjMmNlOXRjbGFpbV9nZW5lcmF0b3JfaW5mb6RkbmFtZXgYT3BlbkFJIE1lZGlhIFNlcnZpY2UgQVBJZGljb26iY3VybHgkc2VsZiNqdW1iZj1jMnBhLmFzc2VydGlvbnMvYzJwYS5pY29uZGhhc2hYIOH0N0LQS5tymrLUrstYklWfIKG0eVORgXzJ29Lmjw8+a3NwZWNWZXJzaW9uZTIuMi4wd29yZy5jb250ZW50YXV0aC5jMnBhX3JzZjAuNzkuMmlzaWduYXR1cmV4TXNlbGYjanVtYmY9L2MycGEvdXJuOmMycGE6ZmY5MDZmN2QtN2FhZi00NjU0LWEyYjQtZGQ2OTdkZjdhZTY5L2MycGEuc2lnbmF0dXJlcmNyZWF0ZWRfYXNzZXJ0aW9uc4SiY3VybHgkc2VsZiNqdW1iZj1jMnBhLmFzc2VydGlvbnMvYzJwYS5pY29uZGhhc2hYIOH0N0LQS5tymrLUrstYklWfIKG0eVORgXzJ29Lmjw8+omN1cmx4KnNlbGYjanVtYmY9YzJwYS5hc3NlcnRpb25zL2MycGEuYWN0aW9ucy52MmRoYXNoWCDWz7GBUKuqkI99WVLQiRgZ9rqBdZzDRS28VMg/icO2l6JjdXJseDJzZWxmI2p1bWJmPWMycGEuYXNzZXJ0aW9ucy9jMnBhLmNlcnRpZmljYXRlLXN0YXR1c2RoYXNoWCBNAVxxVmd2jztMQYJceJP7HAPPBEziSu3FwswWe3H4D6JjdXJseClzZWxmI2p1bWJmPWMycGEuYXNzZXJ0aW9ucy9jMnBhLmhhc2guZGF0YWRoYXNoWCA9AQ8kSpiR/0qD8hyQeyjPryetoDhbSxLExIFw+A+gU2hkYzp0aXRsZWlpbWFnZS5wbmdjYWxnZnNoYTI1NgAARc5qdW1iAAAAKGp1bWRjMmNzABEAEIAAAKoAOJtxA2MycGEuc2lnbmF0dXJlAAAARZ5jYm9y0oRZB1WiASYYIYJZA3IwggNuMIIC86ADAgECAhRSlCUHgbVqhvkzF3hw1o6t72IaQTAK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AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA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
