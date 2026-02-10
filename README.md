[index.html](https://github.com/user-attachments/files/25205221/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>A Card for Ysabella 🖤🌹</title>

  <!-- Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Patrick+Hand&family=Playfair+Display:wght@500;600&display=swap" rel="stylesheet">

  <style>
    * { box-sizing: border-box; }

    body {
      margin: 0;
      width: 100vw;
      height: 100vh;
      background:
        radial-gradient(circle at top, rgba(120,0,30,0.6), transparent 60%),
        linear-gradient(160deg, #000000, #120006);
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: 'Patrick Hand', cursive;
      overflow: hidden;
    }

    .book {
      width: 90vw;
      height: 90vh;
      max-width: 900px;
      max-height: 1200px;
      perspective: 3000px;
      cursor: pointer;
      position: relative;
    }

    .page {
      position: absolute;
      width: 100%;
      height: 100%;
      background:
        linear-gradient(135deg, #160008, #2b000f);
      border-radius: 24px;
      box-shadow: 0 40px 90px rgba(0,0,0,0.9);
      transform-origin: left center;
      transition: transform 1.8s ease;
      padding: 56px 64px;
      backface-visibility: hidden;
      border: 1px solid rgba(255,50,90,0.25);
    }

    .page::after {
      content: "";
      position: absolute;
      inset: 0;
      background-image:
        radial-gradient(circle at 20% 30%, rgba(0,0,0,0.55) 0 40%, transparent 42%),
        radial-gradient(circle at 80% 70%, rgba(0,0,0,0.45) 0 38%, transparent 40%);
      opacity: 0.25;
      pointer-events: none;
    }

    .page:nth-child(1) { z-index: 4; }
    .page:nth-child(2) { z-index: 3; }
    .page:nth-child(3) { z-index: 2; }
    .page:nth-child(4) { z-index: 1; }

    .page.flipped {
      transform: rotateY(-180deg);
    }

    .center { text-align: center; }

    .cover-title {
      font-family: 'Great Vibes', cursive;
      font-size: clamp(56px, 6vw, 92px);
      color: #ff2b5f;
      margin-top: 25vh;
      text-shadow: 0 0 20px rgba(255,40,90,0.7);
    }

    .cover-sub {
      margin-top: 12px;
      font-size: 18px;
      color: #ff9bb3;
    }

    .tap {
      position: absolute;
      bottom: 16px;
      width: 100%;
      text-align: center;
      font-size: 14px;
      opacity: 0.6;
      color: #ff9bb3;
    }

    .photo-frame {
      width: 100%;
      max-height: 45%;
      border-radius: 22px;
      overflow: hidden;
      margin: 32px 0;
      box-shadow: 0 18px 40px rgba(0,0,0,0.7);
      border: 1px solid rgba(255,60,100,0.45);
    }

    .photo-frame img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .message {
      font-size: 26px;
      color: #ffd6df;
      line-height: 1.9;
    }

    .question {
      font-family: 'Playfair Display', serif;
      font-size: 34px;
      color: #ff3b6f;
      margin-top: 80px;
      text-align: center;
      text-shadow: 0 0 14px rgba(255,40,90,0.6);
    }

    .buttons {
      margin-top: 26px;
      text-align: center;
    }

    button {
      padding: 14px 34px;
      border-radius: 40px;
      border: none;
      font-size: 18px;
      cursor: pointer;
      background: linear-gradient(135deg, #ff1e56, #8b001f);
      color: white;
      font-family: 'Patrick Hand', cursive;
      box-shadow: 0 14px 36px rgba(255,30,86,0.8);
      margin: 0 8px;
    }

    .final {
      display: none;
      text-align: center;
      margin-top: 120px;
      font-size: 30px;
      color: #ff6f91;
      font-family: 'Great Vibes', cursive;
      text-shadow: 0 0 14px rgba(255,40,90,0.7);
    }

    .signature {
      font-family: 'Brush Script MT', 'Comic Sans MS', cursive;
      font-size: 18px;
      opacity: 0.9;
      margin-top: 18px;
      color: #ffd6df;
    }

    /* Heart pop animation */
    .heart {
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%) scale(0);
      font-size: 80px;
      color: #000000;
      pointer-events: none;
      animation: pop 1.2s ease forwards;
      text-shadow: 0 0 18px rgba(255,40,90,0.8);
    }

    @keyframes pop {
      0% { transform: translate(-50%, -50%) scale(0); opacity: 0; }
      40% { transform: translate(-50%, -50%) scale(1.3); opacity: 1; }
      70% { transform: translate(-50%, -50%) scale(1); }
      100% { transform: translate(-50%, -120%) scale(0.8); opacity: 0; }
    }
  </style>
</head>
<body>

<audio id="bgMusic" loop>
  <source src="sparkle-piano-violin.mp3" type="audio/mpeg">
</audio>

<div class="book" onclick="nextPage()">

  <!-- Cover -->
  <div class="page center">
    <div class="cover-title">Happy Valentine’s Day</div>
    <div class="cover-sub">For Ysabella 🖤</div>
    <div class="tap">tap to open</div>
  </div>

  <!-- Page 1 -->
  <div class="page">
    <div class="photo-frame"><img src="photo1.jpg"></div>
    <div class="photo-frame"><img src="photo2.jpg"></div>
    <div class="message">
      We’ve had a lot of problems lately, like you said… but even with all of that, I still love you deeply.
    </div>
  </div>

  <!-- Page 2 -->
  <div class="page">
    <div class="photo-frame"><img src="photo3.jpg"></div>
    <div class="photo-frame"><img src="photo4.jpg"></div>
    <div class="message">
      I love your smile that brightens my day, your bungisngis, your eyes that are sometimes scary but mostly lovely.<br><br>
      I love your pouty lips that I always want to kiss, your nose that I want beside my face when we cuddle, your voice that I always want to hear kahit ayaw mo akong kantahan.
    </div>
  </div>

  <!-- Page 3 -->
  <div class="page">
    <div class="photo-frame"><img src="photo5.jpg"></div>
    <div class="message">
      Every little trait — but most of all, your heart. Even with its edge, it’s still kind, lovable, and the one I choose.
    </div>
    <div class="question">Will you be my Valentine? 🌹</div>
    <div class="buttons" id="choiceButtons">
      <button onclick="event.stopPropagation(); yes()">Yes</button>
      <button onclick="event.stopPropagation(); no(this)">No</button>
    </div>
  </div>

  <!-- Final -->
  <div class="page">
    <div class="final" id="final">
      Happy Valentine’s Day 🌹
      <div class="signature">always yours,<br>boop</div>
    </div>
  </div>

</div>

<script>
  const pages = document.querySelectorAll('.page');
  let current = 0;
  const music = document.getElementById('bgMusic');

  function nextPage() {
    if (music.paused) music.play();
    if (current < pages.length - 1) {
      pages[current].classList.add('flipped');
      current++;
    }
  }

  function yes() {
    document.getElementById('choiceButtons').style.display = 'none';
    document.getElementById('final').style.display = 'block';

    const heart = document.createElement('div');
    heart.className = 'heart';
    heart.innerHTML = '🖤🌹';
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 1200);

    nextPage();
  }

  function no(btn) {
    btn.innerText = 'Absolutely';
    setTimeout(() => yes(), 700);
  }
</script>

</body>
</html>
