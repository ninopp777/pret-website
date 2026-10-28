# pret-website

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>PRÊT ♡ Ready Immediately</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Playfair+Display:wght@400;500;600&family=DM+Sans:wght@400;500&display=swap" rel="stylesheet">

<style>
:root {
  --pink: #f8dce6;
  --pale: #fff5f7;
  --rose: #bc718b;
  --dark: #744858;
  --line: #e8b9ca;
}

* { box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  margin: 0;
  color: var(--dark);
  font-family: "DM Sans", sans-serif;
  background-color: #f9e2e9;
  background-image:
    radial-gradient(ellipse at 10% 15%, #fff4f7 0 2px, transparent 3px),
    radial-gradient(ellipse at 90% 70%, #efbfd0 0 2px, transparent 3px),
    linear-gradient(135deg, #fbe8ee, #f4d2df, #fff0f4);
  background-size: 35px 35px, 43px 43px, 100% 100%;
  overflow-x: hidden;
}

.page {
  width: min(100%, 1100px);
  margin: auto;
  padding: 20px clamp(14px, 4vw, 42px) 35px;
  position: relative;
}

.page::before {
  content: "";
  position: fixed;
  inset: 7px;
  border: 2px solid #e9b8cb;
  outline: 1px solid #fceff3;
  outline-offset: -7px;
  pointer-events: none;
  z-index: 5;
}

.lace {
  height: 19px;
  background:
    radial-gradient(circle at 10px 0, #fff3f7 8px, transparent 9px)
    0 0 / 20px 20px repeat-x;
  border-bottom: 1px solid #e8bdcc;
  opacity: .9;
}

.envelope {
  position: absolute;
  font-size: clamp(25px, 5vw, 45px);
  color: #d99bb2;
  opacity: .65;
  z-index: 0;
  user-select: none;
}

.e1 { top: 70px; left: 18px; transform: rotate(-15deg); }
.e2 { top: 75px; right: 22px; transform: rotate(13deg); }
.e3 { top: 470px; right: 12px; transform: rotate(-12deg); }
.e4 { bottom: 80px; left: 18px; transform: rotate(12deg); }
.e5 { bottom: 85px; right: 18px; transform: rotate(-10deg); }

.hero {
  display: grid;
  grid-template-columns: minmax(0, .9fr) minmax(0, 1.1fr);
  align-items: center;
  gap: clamp(20px, 5vw, 60px);
  padding: 42px 4% 48px;
  position: relative;
  z-index: 1;
}

.portrait-frame {
  position: relative;
  padding: 12px;
  border: 3px double #d59bb0;
  border-radius: 48% 48% 8px 8px;
  background: linear-gradient(145deg, #fff7f9, #e9bdce);
  box-shadow: 0 5px 18px #b76e881f;
}

.portrait-frame::before {
  content: "୨୧";
  position: absolute;
  top: -20px;
  left: 50%;
  transform: translateX(-50%);
  font-size: 38px;
  color: #bc718b;
  z-index: 3;
}

.portrait-frame::after {
  content: "♡";
  position: absolute;
  bottom: -19px;
  left: 12px;
  font-size: 31px;
  color: #bc718b;
}

.portrait-inner {
  position: relative;
  overflow: hidden;
  border-radius: 48% 48% 5px 5px;
  border: 1px solid #e1aabd;
  aspect-ratio: 4 / 5;
  background: #edc9d7;
}

.portrait-inner img {
  width: 100%;
  height: 100%;
  display: block;
  object-fit: cover;
  object-position: center;
  filter: sepia(.08) saturate(.8);
}

.curtain {
  position: absolute;
  top: 0;
  right: -2px;
  height: 100%;
  width: 22%;
  z-index: 2;
  pointer-events: none;
  background:
    repeating-linear-gradient(
      90deg,
      #f9e3eb 0 5px,
      #dca8bc 7px,
      #fff0f5 12px,
      #e7b7c9 16px
    );
  opacity: .88;
  border-left: 2px solid #fff2f6;
  border-radius: 0 0 0 40%;
  box-shadow: -3px 0 7px #9d5e751c;
}

.curtain::after {
  content: "🎀";
  position: absolute;
  top: 45%;
  left: -8px;
  font-size: 24px;
}

.brand {
  text-align: center;
  padding: 15px 0;
}

.tiny {
  text-transform: uppercase;
  letter-spacing: 4px;
  font-size: 10px;
  color: #a96982;
}

.brand h1 {
  font-family: "Playfair Display", serif;
  font-size: clamp(53px, 10vw, 100px);
  font-weight: 400;
  letter-spacing: 5px;
  line-height: 1.05;
  margin: 12px 0 0;
  color: #ad637f;
  text-shadow: 1px 2px #fff4f7, 2px 4px #d9a2b7;
}

.tagline {
  font-family: "Great Vibes", cursive;
  font-size: clamp(29px, 5.5vw, 53px);
  margin: 8px 0 15px;
  color: #a85c79;
}

.brand-bow {
  font-size: 26px;
  color: #bd7792;
  letter-spacing: 9px;
}

.intro {
  font-size: 12px;
  line-height: 1.9;
  max-width: 280px;
  margin: 18px auto 0;
  color: #936477;
}

.gallery-title {
  text-align: center;
  font-family: "Great Vibes", cursive;
  font-size: 34px;
  margin: 5px 0 25px;
  color: #a65d79;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: clamp(9px, 2.5vw, 25px);
  align-items: center;
  position: relative;
  z-index: 1;
  padding: 5px 1% 35px;
}

.photo-card {
  position: relative;
  background: #fff9fa;
  padding: 8px 8px 15px;
  border: 1px solid #e7bbcb;
  box-shadow: 0 7px 16px #a5687d20;
  transition: transform .25s ease;
}

.photo-card:nth-child(1) { transform: rotate(-4deg); }
.photo-card:nth-child(2) { transform: translateY(-13px) rotate(2deg); }
.photo-card:nth-child(3) { transform: rotate(4deg); }

.photo-card:hover { transform: translateY(-5px) rotate(0); }

.photo-card img {
  display: block;
  width: 100%;
  aspect-ratio: 3 / 4;
  object-fit: cover;
  border: 1px solid #f1d4de;
}

.photo-card .caption {
  font-family: "Great Vibes", cursive;
  text-align: center;
  font-size: clamp(17px, 2.8vw, 27px);
  padding-top: 11px;
  color: #ad637f;
}

.photo-card .ribbon {
  position: absolute;
  top: -13px;
  left: 50%;
  transform: translateX(-50%);
  font-size: 23px;
  z-index: 2;
}

.manifesting { position: relative; }

.manifesting::after {
  content: "MANIFESTING";
  position: absolute;
  top: 36%;
  left: 0;
  width: 100%;
  text-align: center;
  color: white;
  font-family: "Playfair Display", serif;
  letter-spacing: 2px;
  font-size: clamp(11px, 2vw, 17px);
  text-shadow: 0 2px 8px #52303c;
}

.quote-card {
  display: flex;
  aspect-ratio: 3 / 4;
  padding: 12px;
  align-items: center;
  justify-content: center;
  text-align: center;
  background:
    radial-gradient(ellipse at top left, #fff6fa, transparent 70%),
    linear-gradient(145deg, #f3d0df, #fff0f5);
  border: 1px solid #e8bdce;
  outline: 1px solid #f2d6e0;
  outline-offset: -6px;
}

.quote-card p {
  font-family: "Great Vibes", cursive;
  font-size: clamp(22px, 3.8vw, 37px);
  line-height: 1.5;
  color: #a75e7b;
}

.quote-card small {
  display: block;
  font-family: "DM Sans", sans-serif;
  font-size: 9px;
  letter-spacing: 2px;
  margin-top: 12px;
}

footer {
  text-align: center;
  font-family: "Great Vibes", cursive;
  font-size: 25px;
  color: #a65d79;
  padding: 15px 0 25px;
  position: relative;
  z-index: 1;
}

@media (max-width: 600px) {
  .page { padding: 20px 17px 28px; }
  .hero {
    grid-template-columns: 1fr;
    gap: 28px;
    padding: 42px 8% 36px;
  }
  .portrait-frame {
    width: min(78%, 270px);
    margin: auto;
  }
  .brand h1 { font-size: clamp(58px, 15vw, 86px); }
  .intro { font-size: 12px; }
  .gallery { gap: 10px; padding-inline: 1%; }
  .photo-card { padding: 5px 5px 10px; }
  .photo-card .caption { font-size: 17px; }
  .photo-card .ribbon { font-size: 19px; }
  .quote-card { padding: 7px; }
  .quote-card p { font-size: clamp(19px, 5vw, 28px); }
  .e1 { left: 8px; }
  .e2 { right: 8px; }
}

@media (prefers-reduced-motion: reduce) {
  html { scroll-behavior: auto; }
  *, *::before, *::after { transition: none !important; }
}
</style>
</head>

<body>
<div class="page">
  <div class="lace"></div>

  <span class="envelope e1" aria-hidden="true">✉</span>
  <span class="envelope e2" aria-hidden="true">✉</span>
  <span class="envelope e3" aria-hidden="true">♡</span>
  <span class="envelope e4" aria-hidden="true">✉</span>
  <span class="envelope e5" aria-hidden="true">✉</span>

  <header class="hero">
    <div class="portrait-frame">
      <div class="portrait-inner">
        <img
          src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=800&q=85"
          alt="Portrait in the decorative Prêt frame">
        <div class="curtain"></div>
      </div>
    </div>

    <div class="brand">
      <div class="tiny">♡ your little dream space ♡</div>
      <h1>PRÊT</h1>
      <p class="tagline">Ready Immediately</p>
      <div class="brand-bow">୨୧ ♡ ୨୧</div>
      <p class="intro">
        A little space for your intentions, your affirmations,
        and the dreams you're creating. ♡
      </p>
    </div>
  </header>

  <div class="gallery-title">a little daily magic ୨୧</div>

  <section class="gallery" aria-label="Prêt inspiration cards">
    <article class="photo-card">
      <span class="ribbon" aria-hidden="true">🎀</span>
      <div class="manifesting">
        <img
          src="https://images.unsplash.com/photo-1506126613408-eca07ce68773?auto=format&fit=crop&w=600&q=85"
          alt="A peaceful meditation moment">
      </div>
      <div class="caption">manifesting ♡</div>
    </article>

    <article class="photo-card">
      <span class="ribbon" aria-hidden="true">🎀</span>
      <img
        src="https://images.unsplash.com/photo-1518837695005-2083093ee35b?auto=format&fit=crop&w=600&q=85"
        alt="Peaceful nature inspiration">
      <div class="caption">find your peace</div>
    </article>

    <article class="photo-card">
      <span class="ribbon" aria-hidden="true">🎀</span>
      <div class="quote-card">
        <p>
          reminder to listen to your daily subliminal
          <small>♡ A LITTLE NOTE TO YOU ♡</small>
        </p>
      </div>
      <div class="caption">a gentle reminder</div>
    </article>
  </section>

  <footer>made with love & little bows ♡</footer>
  <div class="lace"></div>
</div>
</body>
</html>
