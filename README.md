<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Impulso Digital — Projeto de extensão acadêmica em Ciência da Computação da GRAN Faculdade para apoio tecnológico gratuito a profissionais liberais.">
  <meta name="author" content="Auriçon de Jesus Gomes">
  <meta name="theme-color" content="#071f33">
  <meta property="og:title" content="Impulso Digital | Tecnologia para Profissionais Liberais">
  <meta property="og:description" content="Diagnóstico digital gratuito e orientação tecnológica para profissionais liberais, como parte de atividade extensionista acadêmica.">
  <meta property="og:type" content="website">
  <title>Impulso Digital | Extensão Acadêmica — GRAN Faculdade</title>

  <style>
    :root {
      --navy-950: #061827;
      --navy-900: #071f33;
      --navy-800: #0b2d46;
      --petrol-700: #0d5d67;
      --petrol-600: #117680;
      --petrol-500: #15919c;
      --aqua-300: #72d6d8;
      --green-500: #18a47a;
      --green-100: #dff7ef;
      --white: #ffffff;
      --gray-50: #f7f9fb;
      --gray-100: #eef2f5;
      --gray-200: #dde4ea;
      --gray-400: #94a3b1;
      --gray-600: #526273;
      --gray-700: #3b4b5b;
      --gray-900: #14202b;
      --danger: #b42318;
      --shadow-sm: 0 8px 24px rgba(6, 24, 39, .08);
      --shadow-md: 0 18px 50px rgba(6, 24, 39, .13);
      --radius-sm: 12px;
      --radius-md: 20px;
      --radius-lg: 30px;
      --container: 1180px;
      --header-height: 76px;
      --transition: 180ms ease;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: calc(var(--header-height) + 18px);
    }

    body {
      min-height: 100vh;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      color: var(--gray-900);
      background: var(--white);
      line-height: 1.6;
      -webkit-font-smoothing: antialiased;
      text-rendering: optimizeLegibility;
    }

    img, svg {
      display: block;
      max-width: 100%;
    }

    button, input, select, textarea {
      font: inherit;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button, a {
      -webkit-tap-highlight-color: transparent;
    }

    :focus-visible {
      outline: 3px solid rgba(21, 145, 156, .45);
      outline-offset: 3px;
      border-radius: 8px;
    }

    .container {
      width: min(calc(100% - 32px), var(--container));
      margin-inline: auto;
    }

    .section {
      padding: 76px 0;
    }

    .section-soft {
      background: var(--gray-50);
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 14px;
      padding: 8px 12px;
      border-radius: 999px;
      background: rgba(21, 145, 156, .10);
      color: var(--petrol-700);
      font-size: .82rem;
      font-weight: 800;
      letter-spacing: .06em;
      text-transform: uppercase;
    }

    .eyebrow::before {
      content: "";
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: var(--green-500);
      box-shadow: 0 0 0 5px rgba(24, 164, 122, .12);
    }

    .section-heading {
      max-width: 760px;
      margin-bottom: 34px;
    }

    .section-heading h2 {
      font-size: clamp(1.8rem, 5vw, 3rem);
      line-height: 1.13;
      letter-spacing: -.035em;
      margin-bottom: 14px;
      color: var(--navy-950);
    }

    .section-heading p {
      color: var(--gray-600);
      font-size: clamp(1rem, 2vw, 1.12rem);
    }

    .skip-link {
      position: fixed;
      top: 10px;
      left: 10px;
      z-index: 999;
      transform: translateY(-150%);
      padding: 10px 14px;
      border-radius: 10px;
      background: var(--white);
      color: var(--navy-950);
      font-weight: 800;
      box-shadow: var(--shadow-md);
    }

    .skip-link:focus {
      transform: translateY(0);
    }

    /* Header */
    .site-header {
      position: sticky;
      top: 0;
      z-index: 100;
      min-height: var(--header-height);
      background: rgba(255,255,255,.94);
      border-bottom: 1px solid rgba(221,228,234,.85);
      backdrop-filter: blur(16px);
    }

    .nav-wrap {
      min-height: var(--header-height);
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 18px;
    }

    .brand {
      display: inline-flex;
      align-items: center;
      gap: 11px;
      font-weight: 900;
      color: var(--navy-950);
      letter-spacing: -.03em;
      white-space: nowrap;
    }

    .brand-mark {
      width: 42px;
      height: 42px;
      display: grid;
      place-items: center;
      border-radius: 14px;
      color: var(--white);
      background:
        linear-gradient(135deg, rgba(114,214,216,.9), transparent 48%),
        linear-gradient(135deg, var(--petrol-700), var(--navy-900));
      box-shadow: 0 10px 24px rgba(13,93,103,.22);
    }

    .brand-mark svg {
      width: 24px;
      height: 24px;
    }

    .brand-text {
      font-size: 1.08rem;
    }

    .brand-text span {
      color: var(--petrol-600);
    }

    .nav-links {
      position: fixed;
      inset: var(--header-height) 0 auto 0;
      display: none;
      flex-direction: column;
      padding: 18px 24px 24px;
      background: rgba(255,255,255,.98);
      border-bottom: 1px solid var(--gray-200);
      box-shadow: var(--shadow-sm);
    }

    .nav-links.open {
      display: flex;
    }

    .nav-links a {
      padding: 14px 6px;
      color: var(--gray-700);
      font-weight: 750;
      border-bottom: 1px solid var(--gray-100);
    }

    .nav-links a:hover {
      color: var(--petrol-700);
    }

    .nav-cta {
      margin-top: 12px;
      border: 0 !important;
      border-radius: 12px;
      background: var(--navy-900);
      color: var(--white) !important;
      text-align: center;
    }

    .menu-toggle {
      width: 44px;
      height: 44px;
      display: grid;
      place-items: center;
      border: 1px solid var(--gray-200);
      border-radius: 12px;
      background: var(--white);
      color: var(--navy-950);
      cursor: pointer;
    }

    .menu-toggle svg {
      width: 22px;
      height: 22px;
    }

    /* Hero */
    .hero {
      position: relative;
      overflow: hidden;
      padding: 64px 0 70px;
      background:
        radial-gradient(circle at 88% 15%, rgba(21,145,156,.16), transparent 24%),
        radial-gradient(circle at 10% 60%, rgba(24,164,122,.11), transparent 23%),
        linear-gradient(180deg, #fbfdfd 0%, #f6f9fb 100%);
    }

    .hero::after {
      content: "";
      position: absolute;
      width: 360px;
      height: 360px;
      right: -190px;
      bottom: -210px;
      border: 54px solid rgba(11,45,70,.035);
      border-radius: 50%;
      pointer-events: none;
    }

    .hero-grid {
      position: relative;
      z-index: 1;
      display: grid;
      gap: 34px;
      align-items: center;
    }

    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 9px;
      margin-bottom: 18px;
      padding: 8px 12px;
      border: 1px solid rgba(13,93,103,.18);
      border-radius: 999px;
      background: rgba(255,255,255,.82);
      color: var(--petrol-700);
      font-size: .84rem;
      font-weight: 800;
      box-shadow: var(--shadow-sm);
    }

    .hero-badge svg {
      width: 18px;
      height: 18px;
    }

    .hero h1 {
      max-width: 820px;
      margin-bottom: 18px;
      font-size: clamp(2.3rem, 8vw, 5rem);
      line-height: .98;
      letter-spacing: -.055em;
      color: var(--navy-950);
    }

    .hero h1 .accent {
      color: var(--petrol-600);
    }

    .hero-copy {
      max-width: 720px;
      color: var(--gray-600);
      font-size: clamp(1.04rem, 2.6vw, 1.24rem);
    }

    .hero-actions {
      display: flex;
      flex-direction: column;
      gap: 12px;
      margin-top: 28px;
    }

    .btn {
      min-height: 52px;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      padding: 13px 18px;
      border: 1px solid transparent;
      border-radius: 14px;
      font-weight: 850;
      cursor: pointer;
      transition: transform var(--transition), box-shadow var(--transition), background var(--transition);
    }

    .btn:hover {
      transform: translateY(-2px);
    }

    .btn-primary {
      color: var(--white);
      background: linear-gradient(135deg, var(--petrol-600), var(--navy-900));
      box-shadow: 0 14px 28px rgba(13,93,103,.22);
    }

    .btn-secondary {
      background: var(--white);
      border-color: var(--gray-200);
      color: var(--navy-950);
      box-shadow: var(--shadow-sm);
    }

    .btn svg {
      width: 20px;
      height: 20px;
    }

    .hero-note {
      margin-top: 16px;
      display: flex;
      align-items: flex-start;
      gap: 8px;
      color: var(--gray-600);
      font-size: .9rem;
    }

    .hero-note svg {
      width: 18px;
      min-width: 18px;
      margin-top: 2px;
      color: var(--green-500);
    }

    .hero-panel {
      padding: 22px;
      border: 1px solid rgba(255,255,255,.8);
      border-radius: var(--radius-lg);
      background:
        linear-gradient(145deg, rgba(255,255,255,.96), rgba(247,249,251,.9));
      box-shadow: var(--shadow-md);
    }

    .panel-label {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 10px;
      margin-bottom: 18px;
      color: var(--gray-600);
      font-size: .9rem;
      font-weight: 800;
    }

    .panel-status {
      display: inline-flex;
      align-items: center;
      gap: 7px;
      color: var(--green-500);
    }

    .panel-status::before {
      content: "";
      width: 9px;
      height: 9px;
      border-radius: 50%;
      background: currentColor;
      box-shadow: 0 0 0 5px rgba(24,164,122,.10);
    }

    .diagnostic-list {
      display: grid;
      gap: 12px;
    }

    .diagnostic-item {
      display: grid;
      grid-template-columns: 42px 1fr auto;
      gap: 12px;
      align-items: center;
      padding: 14px;
      border: 1px solid var(--gray-200);
      border-radius: 16px;
      background: var(--white);
    }

    .diagnostic-icon {
      width: 42px;
      height: 42px;
      display: grid;
      place-items: center;
      border-radius: 12px;
      background: rgba(21,145,156,.09);
      color: var(--petrol-700);
    }

    .diagnostic-icon svg {
      width: 21px;
      height: 21px;
    }

    .diagnostic-title {
      font-weight: 850;
      color: var(--navy-950);
    }

    .diagnostic-subtitle {
      font-size: .82rem;
      color: var(--gray-600);
    }

    .check {
      width: 26px;
      height: 26px;
      display: grid;
      place-items: center;
      border-radius: 50%;
      background: var(--green-100);
      color: var(--green-500);
      font-weight: 900;
    }

    /* Trust strip */
    .trust-strip {
      margin-top: -24px;
      position: relative;
      z-index: 3;
    }

    .trust-card {
      display: grid;
      gap: 18px;
      padding: 22px;
      border-radius: 20px;
      background: var(--navy-900);
      color: var(--white);
      box-shadow: var(--shadow-md);
    }

    .trust-item {
      display: flex;
      gap: 12px;
      align-items: flex-start;
    }

    .trust-icon {
      width: 38px;
      height: 38px;
      min-width: 38px;
      display: grid;
      place-items: center;
      border-radius: 11px;
      background: rgba(255,255,255,.09);
      color: var(--aqua-300);
    }

    .trust-icon svg {
      width: 19px;
      height: 19px;
    }

    .trust-item strong {
      display: block;
      margin-bottom: 2px;
      font-size: .96rem;
    }

    .trust-item span {
      color: rgba(255,255,255,.70);
      font-size: .82rem;
    }

    /* Services */
    .services-grid {
      display: grid;
      gap: 18px;
    }

    .service-card {
      height: 100%;
      padding: 24px;
      border: 1px solid var(--gray-200);
      border-radius: var(--radius-md);
      background: var(--white);
      box-shadow: 0 10px 28px rgba(6,24,39,.05);
      transition: transform var(--transition), box-shadow var(--transition), border-color var(--transition);
    }

    .service-card:hover {
      transform: translateY(-5px);
      box-shadow: var(--shadow-md);
      border-color: rgba(21,145,156,.25);
    }

    .service-number {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 20px;
    }

    .service-icon {
      width: 52px;
      height: 52px;
      display: grid;
      place-items: center;
      border-radius: 16px;
      background: linear-gradient(145deg, rgba(21,145,156,.12), rgba(24,164,122,.08));
      color: var(--petrol-700);
    }

    .service-icon svg {
      width: 26px;
      height: 26px;
    }

    .service-index {
      font-size: .82rem;
      font-weight: 900;
      color: var(--gray-400);
      letter-spacing: .08em;
    }

    .service-card h3 {
      margin-bottom: 9px;
      font-size: 1.22rem;
      line-height: 1.2;
      color: var(--navy-950);
    }

    .service-card p {
      color: var(--gray-600);
      font-size: .95rem;
    }

    .service-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 18px;
    }

    .tag {
      padding: 6px 9px;
      border-radius: 8px;
      background: var(--gray-50);
      border: 1px solid var(--gray-200);
      color: var(--gray-700);
      font-size: .76rem;
      font-weight: 750;
    }

    /* Process */
    .process-grid {
      display: grid;
      gap: 14px;
    }

    .step {
      position: relative;
      padding: 22px 22px 22px 74px;
      border-radius: 18px;
      background: var(--white);
      border: 1px solid var(--gray-200);
    }

    .step-number {
      position: absolute;
      left: 20px;
      top: 21px;
      width: 38px;
      height: 38px;
      display: grid;
      place-items: center;
      border-radius: 12px;
      background: var(--navy-900);
      color: var(--white);
      font-weight: 900;
    }

    .step h3 {
      margin-bottom: 5px;
      color: var(--navy-950);
      font-size: 1rem;
    }

    .step p {
      color: var(--gray-600);
      font-size: .9rem;
    }

    /* Institutional */
    .about-grid {
      display: grid;
      gap: 28px;
      align-items: stretch;
    }

    .about-copy {
      padding: 28px;
      border-radius: var(--radius-lg);
      background: var(--navy-900);
      color: var(--white);
      overflow: hidden;
      position: relative;
    }

    .about-copy::after {
      content: "";
      position: absolute;
      width: 220px;
      height: 220px;
      border-radius: 50%;
      right: -100px;
      top: -90px;
      background: rgba(114,214,216,.08);
      border: 32px solid rgba(114,214,216,.06);
    }

    .about-copy h3 {
      position: relative;
      z-index: 1;
      margin-bottom: 14px;
      font-size: clamp(1.5rem, 4vw, 2.2rem);
      line-height: 1.15;
    }

    .about-copy p {
      position: relative;
      z-index: 1;
      color: rgba(255,255,255,.76);
    }

    .about-highlights {
      position: relative;
      z-index: 1;
      display: grid;
      gap: 12px;
      margin-top: 22px;
    }

    .about-highlight {
      display: flex;
      align-items: flex-start;
      gap: 10px;
      padding: 13px 14px;
      border: 1px solid rgba(255,255,255,.10);
      border-radius: 14px;
      background: rgba(255,255,255,.05);
    }

    .about-highlight svg {
      width: 18px;
      min-width: 18px;
      margin-top: 2px;
      color: var(--aqua-300);
    }

    .author-card {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      padding: 28px;
      border: 1px solid var(--gray-200);
      border-radius: var(--radius-lg);
      background: var(--white);
      box-shadow: var(--shadow-sm);
    }

    .author-avatar {
      width: 74px;
      height: 74px;
      display: grid;
      place-items: center;
      margin-bottom: 20px;
      border-radius: 22px;
      color: var(--white);
      background: linear-gradient(145deg, var(--petrol-600), var(--navy-900));
      font-size: 1.5rem;
      font-weight: 900;
      box-shadow: 0 14px 30px rgba(13,93,103,.18);
    }

    .author-card h3 {
      margin-bottom: 6px;
      font-size: 1.35rem;
      color: var(--navy-950);
    }

    .author-role {
      margin-bottom: 16px;
      color: var(--petrol-700);
      font-weight: 800;
    }

    .author-card p {
      color: var(--gray-600);
    }

    .author-meta {
      display: grid;
      gap: 10px;
      margin-top: 22px;
    }

    .meta-line {
      display: flex;
      align-items: flex-start;
      gap: 10px;
      color: var(--gray-700);
      font-size: .9rem;
      overflow-wrap: anywhere;
    }

    .meta-line svg {
      width: 18px;
      min-width: 18px;
      margin-top: 2px;
      color: var(--petrol-600);
    }

    /* Disclaimer */
    .notice {
      margin-top: 28px;
      padding: 18px 20px;
      display: flex;
      align-items: flex-start;
      gap: 12px;
      border: 1px solid rgba(13,93,103,.17);
      border-radius: 16px;
      background: rgba(21,145,156,.07);
      color: var(--gray-700);
    }

    .notice svg {
      width: 22px;
      min-width: 22px;
      margin-top: 1px;
      color: var(--petrol-700);
    }

    .notice strong {
      color: var(--navy-950);
    }

    /* Contact */
    .contact-section {
      background:
        radial-gradient(circle at 10% 20%, rgba(114,214,216,.08), transparent 24%),
        linear-gradient(145deg, var(--navy-950), var(--navy-900));
      color: var(--white);
    }

    .contact-section .section-heading h2 {
      color: var(--white);
    }

    .contact-section .section-heading p {
      color: rgba(255,255,255,.70);
    }

    .contact-section .eyebrow {
      background: rgba(114,214,216,.10);
      color: var(--aqua-300);
    }

    .contact-grid {
      display: grid;
      gap: 24px;
      align-items: start;
    }

    .contact-intro {
      display: grid;
      gap: 16px;
    }

    .contact-point {
      display: flex;
      gap: 13px;
      align-items: flex-start;
      padding: 15px;
      border: 1px solid rgba(255,255,255,.10);
      border-radius: 15px;
      background: rgba(255,255,255,.045);
    }

    .contact-point svg {
      width: 21px;
      min-width: 21px;
      margin-top: 2px;
      color: var(--aqua-300);
    }

    .contact-point strong {
      display: block;
      margin-bottom: 2px;
      font-size: .9rem;
    }

    .contact-point span,
    .contact-point a {
      color: rgba(255,255,255,.70);
      font-size: .88rem;
      overflow-wrap: anywhere;
    }

    .form-card {
      padding: 22px;
      border-radius: var(--radius-md);
      background: var(--white);
      color: var(--gray-900);
      box-shadow: var(--shadow-md);
    }

    .form-card h3 {
      margin-bottom: 5px;
      color: var(--navy-950);
      font-size: 1.3rem;
    }

    .form-card > p {
      margin-bottom: 20px;
      color: var(--gray-600);
      font-size: .9rem;
    }

    .form-grid {
      display: grid;
      gap: 16px;
    }

    .field {
      display: grid;
      gap: 7px;
    }

    .field label {
      color: var(--gray-700);
      font-size: .86rem;
      font-weight: 800;
    }

    .field input,
    .field select,
    .field textarea {
      width: 100%;
      border: 1px solid var(--gray-200);
      border-radius: 12px;
      background: var(--gray-50);
      color: var(--gray-900);
      padding: 13px 14px;
      transition: border-color var(--transition), background var(--transition), box-shadow var(--transition);
    }

    .field textarea {
      min-height: 132px;
      resize: vertical;
    }

    .field input:focus,
    .field select:focus,
    .field textarea:focus {
      outline: 0;
      border-color: var(--petrol-500);
      background: var(--white);
      box-shadow: 0 0 0 4px rgba(21,145,156,.10);
    }

    .field small {
      color: var(--gray-600);
      font-size: .75rem;
    }

    .form-error {
      display: none;
      margin-top: 12px;
      padding: 10px 12px;
      border-radius: 10px;
      background: #fff1f0;
      color: var(--danger);
      font-size: .85rem;
      font-weight: 750;
    }

    .form-error.show {
      display: block;
    }

    .form-consent {
      margin-top: 12px;
      color: var(--gray-600);
      font-size: .76rem;
    }

    .form-card .btn {
      width: 100%;
      margin-top: 4px;
    }

    /* Footer */
    .site-footer {
      padding: 34px 0;
      background: #04131f;
      color: rgba(255,255,255,.68);
    }

    .footer-grid {
      display: grid;
      gap: 24px;
    }

    .footer-brand {
      color: var(--white);
      font-size: 1.05rem;
      font-weight: 900;
    }

    .footer-brand span {
      color: var(--aqua-300);
    }

    .footer-copy {
      max-width: 620px;
      margin-top: 8px;
      font-size: .86rem;
    }

    .footer-links {
      display: flex;
      flex-wrap: wrap;
      gap: 12px 18px;
      align-items: center;
    }

    .footer-links a {
      color: rgba(255,255,255,.78);
      font-size: .86rem;
      font-weight: 750;
    }

    .footer-links a:hover {
      color: var(--aqua-300);
    }

    .footer-bottom {
      margin-top: 26px;
      padding-top: 18px;
      border-top: 1px solid rgba(255,255,255,.09);
      font-size: .78rem;
    }

    /* Floating WhatsApp */
    .whatsapp-float {
      position: fixed;
      right: 18px;
      bottom: 18px;
      z-index: 80;
      width: 54px;
      height: 54px;
      display: grid;
      place-items: center;
      border-radius: 50%;
      background: #20b970;
      color: var(--white);
      box-shadow: 0 12px 32px rgba(0,0,0,.20);
      transition: transform var(--transition);
    }

    .whatsapp-float:hover {
      transform: translateY(-3px) scale(1.03);
    }

    .whatsapp-float svg {
      width: 27px;
      height: 27px;
    }

    /* Reveal on scroll */
    .reveal {
      opacity: 0;
      transform: translateY(16px);
      transition: opacity 500ms ease, transform 500ms ease;
    }

    .reveal.visible {
      opacity: 1;
      transform: none;
    }

    /* Responsive */
    @media (min-width: 640px) {
      .hero-actions {
        flex-direction: row;
        align-items: center;
      }

      .trust-card {
        grid-template-columns: repeat(3, 1fr);
      }

      .services-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .process-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .form-grid.two {
        grid-template-columns: 1fr 1fr;
      }

      .footer-grid {
        grid-template-columns: 1.5fr .8fr;
        align-items: start;
      }
    }

    @media (min-width: 860px) {
      .menu-toggle {
        display: none;
      }

      .nav-links {
        position: static;
        display: flex !important;
        flex-direction: row;
        align-items: center;
        gap: 6px;
        padding: 0;
        background: transparent;
        border: 0;
        box-shadow: none;
      }

      .nav-links a {
        padding: 10px 12px;
        border: 0;
        font-size: .9rem;
      }

      .nav-cta {
        margin: 0 0 0 6px;
        padding-inline: 16px !important;
      }

      .hero {
        padding: 96px 0 98px;
      }

      .hero-grid {
        grid-template-columns: minmax(0, 1.28fr) minmax(330px, .72fr);
        gap: 54px;
      }

      .services-grid {
        grid-template-columns: repeat(4, 1fr);
      }

      .process-grid {
        grid-template-columns: repeat(4, 1fr);
      }

      .about-grid {
        grid-template-columns: 1.08fr .92fr;
      }

      .contact-grid {
        grid-template-columns: .78fr 1.22fr;
        gap: 42px;
      }

      .form-card {
        padding: 30px;
      }
    }

    @media (min-width: 1100px) {
      .section {
        padding: 96px 0;
      }

      .service-card {
        padding: 28px;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      html {
        scroll-behavior: auto;
      }

      *, *::before, *::after {
        animation-duration: .01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: .01ms !important;
      }

      .reveal {
        opacity: 1;
        transform: none;
      }
    }
  </style>
</head>

<body>
  <a class="skip-link" href="#conteudo">Ir para o conteúdo principal</a>

  <header class="site-header" id="inicio">
    <div class="container nav-wrap">
      <a class="brand" href="#inicio" aria-label="Impulso Digital — início">
        <span class="brand-mark" aria-hidden="true">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M4 17l5-5 4 4 7-8"/>
            <path d="M15 8h5v5"/>
          </svg>
        </span>
        <span class="brand-text">Impulso <span>Digital</span></span>
      </a>

      <button class="menu-toggle" id="menuToggle" type="button" aria-expanded="false" aria-controls="navLinks" aria-label="Abrir menu">
        <svg id="menuIcon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
          <path d="M4 7h16M4 12h16M4 17h16"/>
        </svg>
      </button>

      <nav class="nav-links" id="navLinks" aria-label="Navegação principal">
        <a href="#servicos">Serviços</a>
        <a href="#processo">Como funciona</a>
        <a href="#sobre">Sobre o Projeto</a>
        <a href="#contato">Contato</a>
        <a class="nav-cta" href="#contato">Solicitar diagnóstico</a>
      </nav>
    </div>
  </header>

  <main id="conteudo">
    <section class="hero" aria-labelledby="hero-title">
      <div class="container hero-grid">
        <div>
          <div class="hero-badge">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
              <path d="M3 10l9-5 9 5-9 5-9-5z"/>
              <path d="M7 12.5V16c0 1.5 2.2 3 5 3s5-1.5 5-3v-3.5"/>
            </svg>
            Atividade Extensionista • Ciência da Computação • GRAN Faculdade
          </div>

          <h1 id="hero-title">
            Tecnologia simples para <span class="accent">impulsionar</span> quem presta serviços.
          </h1>

          <p class="hero-copy">
            Apoio tecnológico e orientação digital para profissionais liberais que desejam melhorar sua presença online, atendimento, organização comercial e relacionamento com clientes.
          </p>

          <div class="hero-actions">
            <a class="btn btn-primary" href="#contato">
              Solicitar diagnóstico digital gratuito
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
                <path d="M5 12h14M13 6l6 6-6 6"/>
              </svg>
            </a>
            <a class="btn btn-secondary" href="#sobre">Conhecer o projeto</a>
          </div>

          <div class="hero-note">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
              <path d="M20 6L9 17l-5-5"/>
            </svg>
            <span>Iniciativa acadêmica de caráter extensionista, sem cobrança pelo diagnóstico inicial e com foco em impacto social e inclusão digital.</span>
          </div>
        </div>

        <aside class="hero-panel" aria-label="Itens avaliados no diagnóstico digital">
          <div class="panel-label">
            <span>Diagnóstico de presença digital</span>
            <span class="panel-status">Disponível</span>
          </div>

          <div class="diagnostic-list">
            <div class="diagnostic-item">
              <div class="diagnostic-icon" aria-hidden="true">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <rect x="3" y="4" width="18" height="14" rx="2"/>
                  <path d="M8 20h8"/>
                </svg>
              </div>
              <div>
                <div class="diagnostic-title">Presença Web</div>
                <div class="diagnostic-subtitle">Site, responsividade e performance</div>
              </div>
              <span class="check" aria-hidden="true">✓</span>
            </div>

            <div class="diagnostic-item">
              <div class="diagnostic-icon" aria-hidden="true">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M12 21s7-4.5 7-11a7 7 0 1 0-14 0c0 6.5 7 11 7 11z"/>
                  <circle cx="12" cy="10" r="2"/>
                </svg>
              </div>
              <div>
                <div class="diagnostic-title">Visibilidade local</div>
                <div class="diagnostic-subtitle">Maps, reputação e informações públicas</div>
              </div>
              <span class="check" aria-hidden="true">✓</span>
            </div>

            <div class="diagnostic-item">
              <div class="diagnostic-icon" aria-hidden="true">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M21 15a4 4 0 0 1-4 4H8l-5 3V7a4 4 0 0 1 4-4h10a4 4 0 0 1 4 4z"/>
                </svg>
              </div>
              <div>
                <div class="diagnostic-title">Atendimento digital</div>
                <div class="diagnostic-subtitle">WhatsApp, fluxo de contato e teleatendimento</div>
              </div>
              <span class="check" aria-hidden="true">✓</span>
            </div>

            <div class="diagnostic-item">
              <div class="diagnostic-icon" aria-hidden="true">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M4 19V9M10 19V5M16 19v-7M22 19H2"/>
                </svg>
              </div>
              <div>
                <div class="diagnostic-title">Marketing básico</div>
                <div class="diagnostic-subtitle">Métricas, leads e oportunidades</div>
              </div>
              <span class="check" aria-hidden="true">✓</span>
            </div>
          </div>
        </aside>
      </div>
    </section>

    <div class="trust-strip">
      <div class="container">
        <div class="trust-card">
          <div class="trust-item">
            <div class="trust-icon" aria-hidden="true">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M12 3l7 4v5c0 4.8-2.9 7.7-7 9-4.1-1.3-7-4.2-7-9V7l7-4z"/>
              </svg>
            </div>
            <div>
              <strong>Orientação responsável</strong>
              <span>Soluções compatíveis com a realidade e maturidade digital de cada profissional.</span>
            </div>
          </div>

          <div class="trust-item">
            <div class="trust-icon" aria-hidden="true">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M4 12h4l2-7 4 14 2-7h4"/>
              </svg>
            </div>
            <div>
              <strong>Impacto prático</strong>
              <span>Foco em ações simples, mensuráveis e que possam melhorar o relacionamento com clientes.</span>
            </div>
          </div>

          <div class="trust-item">
            <div class="trust-icon" aria-hidden="true">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <circle cx="12" cy="8" r="4"/>
                <path d="M5 21a7 7 0 0 1 14 0"/>
              </svg>
            </div>
            <div>
              <strong>Projeto acadêmico</strong>
              <span>Atividade extensionista que aproxima conhecimento universitário e comunidade.</span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <section class="section" id="servicos" aria-labelledby="servicos-title">
      <div class="container">
        <div class="section-heading reveal">
          <span class="eyebrow">Soluções</span>
          <h2 id="servicos-title">Tecnologia aplicada ao cotidiano dos profissionais liberais.</h2>
          <p>O projeto busca identificar gargalos digitais e indicar melhorias adequadas a negócios de serviços, com linguagem clara e foco em utilidade.</p>
        </div>

        <div class="services-grid">
          <article class="service-card reveal">
            <div class="service-number">
              <div class="service-icon" aria-hidden="true">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M8 9l-4 3 4 3M16 9l4 3-4 3M14 5l-4 14"/>
                </svg>
              </div>
              <span class="service-index">01</span>
            </div>
            <h3>Desenvolvimento Web</h3>
            <p>Orientação e criação de landing pages responsivas, páginas institucionais enxutas e melhorias de performance, usabilidade e SEO local.</p>
            <div class="service-tags">
              <span class="tag">Landing Page</span>
              <span class="tag">Responsividade</span>
              <span class="tag">SEO local</span>
            </div>
          </article>

          <article class="service-card reveal">
            <div class="service-number">
              <div class="service-icon" aria-hidden="true">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M12 21s7-4.5 7-11a7 7 0 1 0-14 0c0 6.5 7 11 7 11z"/>
                  <circle cx="12" cy="10" r="2"/>
                </svg>
              </div>
              <span class="service-index">02</span>
            </div>
            <h3>Google Meu Negócio</h3>
            <p>Boas práticas para presença no Google Maps, consistência das informações, apresentação dos serviços, catálogo e gestão da reputação online.</p>
            <div class="service-tags">
              <span class="tag">Maps</span>
              <span class="tag">Reputação</span>
              <span class="tag">Catálogo</span>
            </div>
          </article>

          <article class="service-card reveal">
            <div class="service-number">
              <div class="service-icon" aria-hidden="true">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M4 5h16v12H8l-4 3V5z"/>
                  <path d="M8 9h8M8 13h5"/>
                </svg>
              </div>
              <span class="service-index">03</span>
            </div>
            <h3>Ferramentas Comerciais</h3>
            <p>Configuração orientada de WhatsApp Business, organização de contatos, respostas rápidas, tags analíticas e automações simples de captação de leads.</p>
            <div class="service-tags">
              <span class="tag">WhatsApp Business</span>
              <span class="tag">Leads</span>
              <span class="tag">Métricas</span>
            </div>
          </article>

          <article class="service-card reveal">
            <div class="service-number">
              <div class="service-icon" aria-hidden="true">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <rect x="4" y="3" width="16" height="18" rx="2"/>
                  <path d="M9 7h6M8 11h8M8 15h5"/>
                </svg>
              </div>
              <span class="service-index">04</span>
            </div>
            <h3>Boas Práticas de Teleatendimento</h3>
            <p>Orientações para uma experiência digital mais organizada, clara e profissional, respeitando privacidade, segurança, limites éticos e regras da profissão.</p>
            <div class="service-tags">
              <span class="tag">Atendimento</span>
              <span class="tag">Privacidade</span>
              <span class="tag">Organização</span>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section class="section section-soft" id="processo" aria-labelledby="processo-title">
      <div class="container">
        <div class="section-heading reveal">
          <span class="eyebrow">Como funciona</span>
          <h2 id="processo-title">Um processo simples para transformar diagnóstico em próximos passos.</h2>
          <p>O objetivo não é complicar a operação do profissional, mas organizar prioridades e mostrar onde pequenas melhorias digitais podem gerar valor.</p>
        </div>

        <div class="process-grid">
          <article class="step reveal">
            <span class="step-number">1</span>
            <h3>Contato inicial</h3>
            <p>O profissional informa sua área de atuação e descreve brevemente a necessidade.</p>
          </article>

          <article class="step reveal">
            <span class="step-number">2</span>
            <h3>Levantamento digital</h3>
            <p>São observados os principais pontos de presença online, comunicação e atendimento.</p>
          </article>

          <article class="step reveal">
            <span class="step-number">3</span>
            <h3>Recomendações</h3>
            <p>São apresentadas oportunidades de melhoria priorizadas por simplicidade e impacto.</p>
          </article>

          <article class="step reveal">
            <span class="step-number">4</span>
            <h3>Orientação prática</h3>
            <p>Quando aplicável, o projeto orienta ajustes ou demonstra soluções tecnológicas acessíveis.</p>
          </article>
        </div>
      </div>
    </section>

    <section class="section" id="sobre" aria-labelledby="sobre-title">
      <div class="container">
        <div class="section-heading reveal">
          <span class="eyebrow">Extensão universitária</span>
          <h2 id="sobre-title">Conhecimento acadêmico conectado às necessidades reais da comunidade.</h2>
          <p>A atividade extensionista aproxima universidade e sociedade ao aplicar fundamentos de computação, web, experiência do usuário e transformação digital em problemas cotidianos de prestadores de serviço.</p>
        </div>

        <div class="about-grid">
          <div class="about-copy reveal">
            <h3>Sobre o projeto Impulso Digital</h3>
            <p>
              O projeto foi concebido no contexto da formação em Ciência da Computação da GRAN Faculdade para apoiar profissionais liberais — como advogados, psicólogos, contadores, médicos, arquitetos e outros prestadores de serviço — na adoção consciente de soluções digitais.
            </p>

            <div class="about-highlights">
              <div class="about-highlight">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
                  <path d="M4 12l5 5L20 6"/>
                </svg>
                <span>Aplicação prática de conhecimentos de tecnologia e desenvolvimento web.</span>
              </div>
              <div class="about-highlight">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
                  <path d="M4 12l5 5L20 6"/>
                </svg>
                <span>Contribuição social por meio da inclusão e orientação digital.</span>
              </div>
              <div class="about-highlight">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
                  <path d="M4 12l5 5L20 6"/>
                </svg>
                <span>Respeito às limitações técnicas, éticas e regulatórias de cada profissão.</span>
              </div>
            </div>
          </div>

          <article class="author-card reveal">
            <div>
              <div class="author-avatar" aria-hidden="true">AG</div>
              <h3>Auriçon de Jesus Gomes</h3>
              <div class="author-role">Responsável pelo desenvolvimento acadêmico</div>
              <p>Graduando em Ciência da Computação (1º Período) — GRAN Faculdade, responsável pela concepção, desenvolvimento e apresentação desta iniciativa extensionista.</p>
            </div>

            <div class="author-meta">
              <div class="meta-line">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
                  <path d="M4 4h16v16H4z"/><path d="M4 7l8 6 8-6"/>
                </svg>
                <a href="mailto:gomesgestor@gmail.com">gomesgestor@gmail.com</a>
              </div>

              <div class="meta-line">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
                  <path d="M21 15a4 4 0 0 1-4 4H8l-5 3V7a4 4 0 0 1 4-4h10a4 4 0 0 1 4 4z"/>
                </svg>
                <a href="https://api.whatsapp.com/send?phone=5518998102129" target="_blank" rel="noopener noreferrer">WhatsApp: +55 (18) 99810-2129</a>
              </div>

              <div class="meta-line">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
                  <path d="M3 10l9-5 9 5-9 5-9-5z"/>
                  <path d="M7 12.5V16c0 1.5 2.2 3 5 3s5-1.5 5-3v-3.5"/>
                </svg>
                <span>Atividade Extensionista — Ciência da Computação — GRAN Faculdade</span>
              </div>
            </div>
          </article>
        </div>

        <div class="notice reveal">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
            <circle cx="12" cy="12" r="9"/>
            <path d="M12 8h.01M11 11h1v5h1"/>
          </svg>
          <div>
            <strong>Informação importante:</strong>
            esta página apresenta um projeto acadêmico de extensão. As orientações de teleatendimento e transformação digital têm caráter tecnológico e informativo e não substituem regras profissionais, normas de conselhos de classe, políticas de privacidade, requisitos de segurança, nem assessoria jurídica, médica, contábil ou de outra natureza especializada.
          </div>
        </div>
      </div>
    </section>

    <section class="section contact-section" id="contato" aria-labelledby="contato-title">
      <div class="container">
        <div class="section-heading reveal">
          <span class="eyebrow">Contato</span>
          <h2 id="contato-title">Conte sua necessidade e inicie um diagnóstico digital.</h2>
          <p>Preencha os dados abaixo. Ao enviar, o navegador abrirá o WhatsApp com uma mensagem formatada para facilitar o primeiro contato.</p>
        </div>

        <div class="contact-grid">
          <div class="contact-intro reveal">
            <div class="contact-point">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
                <path d="M21 15a4 4 0 0 1-4 4H8l-5 3V7a4 4 0 0 1 4-4h10a4 4 0 0 1 4 4z"/>
              </svg>
              <div>
                <strong>WhatsApp</strong>
                <a href="https://api.whatsapp.com/send?phone=5518998102129" target="_blank" rel="noopener noreferrer">+55 (18) 99810-2129</a>
              </div>
            </div>

            <div class="contact-point">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
                <rect x="3" y="5" width="18" height="14" rx="2"/>
                <path d="M3 7l9 6 9-6"/>
              </svg>
              <div>
                <strong>E-mail</strong>
                <a href="mailto:gomesgestor@gmail.com">gomesgestor@gmail.com</a>
              </div>
            </div>

            <div class="contact-point">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
                <path d="M12 3l7 4v5c0 4.8-2.9 7.7-7 9-4.1-1.3-7-4.2-7-9V7l7-4z"/>
              </svg>
              <div>
                <strong>Uso dos dados</strong>
                <span>As informações preenchidas são usadas apenas para montar a mensagem de WhatsApp no seu próprio navegador. Esta página não possui banco de dados nem armazenamento de formulário.</span>
              </div>
            </div>
          </div>

          <form class="form-card reveal" id="contactForm" novalidate>
            <h3>Solicitar diagnóstico</h3>
            <p>Informe apenas o necessário para o primeiro contato.</p>

            <div class="form-grid two">
              <div class="field">
                <label for="nome">Nome completo *</label>
                <input id="nome" name="nome" type="text" autocomplete="name" maxlength="120" placeholder="Seu nome" required>
              </div>

              <div class="field">
                <label for="area">Área de atuação *</label>
                <select id="area" name="area" required>
                  <option value="">Selecione uma opção</option>
                  <option>Advocacia</option>
                  <option>Psicologia</option>
                  <option>Contabilidade</option>
                  <option>Medicina</option>
                  <option>Arquitetura</option>
                  <option>Odontologia</option>
                  <option>Consultoria</option>
                  <option>Engenharia</option>
                  <option>Nutrição</option>
                  <option>Fisioterapia</option>
                  <option>Outro profissional liberal</option>
                </select>
              </div>
            </div>

            <div class="form-grid">
              <div class="field">
                <label for="mensagem">Mensagem / necessidade *</label>
                <textarea id="mensagem" name="mensagem" maxlength="1200" placeholder="Ex.: preciso melhorar minha presença no Google, organizar o atendimento no WhatsApp ou criar uma página profissional." required></textarea>
                <small>Evite informar dados sensíveis, sigilosos, dados de pacientes/clientes ou qualquer informação confidencial.</small>
              </div>

              <button class="btn btn-primary" type="submit">
                Enviar pelo WhatsApp
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
                  <path d="M5 12h14M13 6l6 6-6 6"/>
                </svg>
              </button>
            </div>

            <div class="form-error" id="formError" role="alert">
              Preencha corretamente o nome, a área de atuação e a mensagem antes de continuar.
            </div>

            <p class="form-consent">
              Ao clicar em “Enviar pelo WhatsApp”, você será redirecionado para o serviço do WhatsApp, sujeito aos termos e à política de privacidade da própria plataforma.
            </p>
          </form>
        </div>
      </div>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container">
      <div class="footer-grid">
        <div>
          <div class="footer-brand">Impulso <span>Digital</span></div>
          <p class="footer-copy">
            Projeto desenvolvido como atividade extensionista curricular do curso de Ciência da Computação (1º Período) da GRAN Faculdade, com foco em apoio tecnológico e inclusão digital de profissionais liberais.
          </p>
        </div>

        <div class="footer-links" aria-label="Links do rodapé">
          <a href="#servicos">Serviços</a>
          <a href="#sobre">Sobre</a>
          <a href="#contato">Contato</a>
          <a href="mailto:gomesgestor@gmail.com">E-mail</a>
        </div>
      </div>

      <div class="footer-bottom">
        © <span id="year"></span> Auriçon de Jesus Gomes. Projeto acadêmico — GRAN Faculdade. Todos os direitos reservados sobre o desenvolvimento desta página.
      </div>
    </div>
  </footer>

  <a
    class="whatsapp-float"
    href="https://api.whatsapp.com/send?phone=5518998102129&text=Ol%C3%A1%2C%20gostaria%20de%20saber%20mais%20sobre%20o%20projeto%20Impulso%20Digital."
    target="_blank"
    rel="noopener noreferrer"
    aria-label="Falar pelo WhatsApp"
    title="Falar pelo WhatsApp"
  >
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" aria-hidden="true">
      <path d="M20.5 11.5a8.5 8.5 0 0 1-12.8 7.35L3 20l1.18-4.45A8.5 8.5 0 1 1 20.5 11.5z"/>
      <path d="M8.2 8.1c.2-.45.42-.46.7-.47h.35c.12 0 .3.04.46.4l.65 1.55c.08.19.07.34-.04.5l-.38.54c-.12.15-.24.28-.1.52.14.24.63 1.03 1.36 1.66.93.8 1.72 1.05 1.96 1.17.24.12.38.1.52-.06l.74-.86c.17-.2.34-.16.57-.08l1.48.7c.24.12.4.18.46.28.06.1.06.58-.14 1.14-.2.56-1.16 1.07-1.6 1.14-.42.07-.95.1-1.54-.1-.36-.12-.82-.27-1.42-.52-.25-.1-4.4-2.04-5.3-5.13-.22-.76-.03-1.5.27-2.18z"/>
    </svg>
  </a>

  <script>
    (() => {
      "use strict";

      const menuToggle = document.getElementById("menuToggle");
      const navLinks = document.getElementById("navLinks");
      const navAnchors = navLinks.querySelectorAll("a");
      const contactForm = document.getElementById("contactForm");
      const formError = document.getElementById("formError");
      const year = document.getElementById("year");
      const whatsappPhone = "5518998102129";

      // Ano automático no rodapé
      year.textContent = new Date().getFullYear();

      // Menu mobile acessível
      const setMenuState = (isOpen) => {
        navLinks.classList.toggle("open", isOpen);
        menuToggle.setAttribute("aria-expanded", String(isOpen));
        menuToggle.setAttribute("aria-label", isOpen ? "Fechar menu" : "Abrir menu");
      };

      menuToggle.addEventListener("click", () => {
        const isOpen = menuToggle.getAttribute("aria-expanded") === "true";
        setMenuState(!isOpen);
      });

      navAnchors.forEach((link) => {
        link.addEventListener("click", () => setMenuState(false));
      });

      document.addEventListener("keydown", (event) => {
        if (event.key === "Escape") setMenuState(false);
      });

      window.addEventListener("resize", () => {
        if (window.innerWidth >= 860) setMenuState(false);
      });

      // Formulário -> WhatsApp API
      contactForm.addEventListener("submit", (event) => {
        event.preventDefault();

        const nome = document.getElementById("nome").value.trim();
        const area = document.getElementById("area").value.trim();
        const mensagem = document.getElementById("mensagem").value.trim();

        if (!nome || !area || !mensagem) {
          formError.classList.add("show");
          return;
        }

        formError.classList.remove("show");

        const texto = [
          "Olá! Gostaria de solicitar um diagnóstico digital gratuito pelo projeto Impulso Digital.",
          "",
          `*Nome:* ${nome}`,
          `*Área de atuação:* ${area}`,
          `*Necessidade / mensagem:* ${mensagem}`,
          "",
          "Contato realizado pelo formulário da página da Atividade Extensionista — Ciência da Computação / GRAN Faculdade."
        ].join("\n");

        const whatsappUrl =
          `https://api.whatsapp.com/send?phone=${whatsappPhone}&text=${encodeURIComponent(texto)}`;

        // Redireciona a aba atual, evitando que bloqueadores de popup impeçam o contato.
        window.location.href = whatsappUrl;
      });

      // Animações leves de entrada; respeita prefers-reduced-motion via CSS
      const revealItems = document.querySelectorAll(".reveal");

      if ("IntersectionObserver" in window) {
        const observer = new IntersectionObserver((entries, obs) => {
          entries.forEach((entry) => {
            if (entry.isIntersecting) {
              entry.target.classList.add("visible");
              obs.unobserve(entry.target);
            }
          });
        }, { threshold: 0.12 });

        revealItems.forEach((item) => observer.observe(item));
      } else {
        revealItems.forEach((item) => item.classList.add("visible"));
      }
    })();
  </script>
</body>
</html>
