
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>For You — ♡</title>
  <style>
    :root{
      --bg:#0f1022;
      --card:#121227;
      --accent:#ff6b9a;
      --accent-2:#ffd166;
      --glass: rgba(255,255,255,0.06);
      --soft: rgba(255,255,255,0.04);
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;font-family:Inter,ui-sans-serif,system-ui,-apple-system,'Segoe UI',Roboto,'Helvetica Neue',Arial}
    body{background: radial-gradient(1200px 600px at 10% 20%, rgba(241, 0, 76, 0.5), transparent), radial-gradient(1000px 500px at 90% 80%, rgba(255,209,102,0.03), transparent), var(--bg); color:#eee; -webkit-font-smoothing:antialiased; display:flex; align-items:center; justify-content:center; padding:32px}
   .card{width:100%; max-width:960px; background: linear-gradient(180deg, rgba(138, 4, 131, 0.5), rgba(255,255,255,0.01)); border-radius:18px; padding:28px; box-shadow: 0 10px 40px rgba(2,6,23,0.6); position:relative; overflow:hidden; border:1px solid rgba(255,255,255,0.03)}
   .split{display:grid; grid-template-columns: 1fr 420px; gap:22px; align-items:center}
    @media (max-width:880px){ .split{grid-template-columns:1fr} .side{order:-1} }
  .greeting{padding:18px}
    h1{font-size:2.1rem; margin:0 0 8px 0; letter-spacing:0.4px}
    .subtitle{color:rgba(255, 0, 179, 1); margin-bottom:18px}
  .photo{ background:linear-gradient(135deg, rgba(202, 0, 185, 0.03), rgba(255,255,255,0.01)); border-radius:14px; padding:12px; display:flex; align-items:center; justify-content:center; flex-direction:column; gap:12px }
    .photo img{ width:100%; max-width:320px; border-radius:10px; display:block; box-shadow:0 8px 30px rgba(2,6,23,0.6); transition:opacity 1s ease-in-out }
    .caption{font-size:0.95rem; text-align:center}
  .controls{display:flex; gap:12px; margin-top:8px}
    button{background:linear-gradient(90deg,var(--accent),var(--accent-2)); border:none; color:#111; padding:10px 14px; border-radius:12px; font-weight:700; cursor:pointer; box-shadow:0 6px 18px rgba(255,107,154,0.12)}
 .message{ margin-top:18px; padding:16px; background:var(--glass); border-radius:12px; color:#fff; line-height:1.5; font-size:1rem }
 footer{ margin-top:14px; color:rgba(255,255,255,0.45); font-size:0.86rem }
  </style>
</head>
<body>
  <div class="card">
    <div class="split">
      <div class="greeting">
        <h1>Hello, my dear greatest love!! — <span style="color:var(--accent)">I miss you a lot!!</span></h1>
        <div class="subtitle">A little message for you okay?✨</div>
        <div class="message" id="longmsg">
          I made this because I wanted you to realize that i'm always here even though i'm the one who left
          i didnt mean to left, it's just you're not happy with me anymore, so i decide to make you happy without me.
          this is the last surprise i will make it for you okay? i always love you ashley, My baby. ❤️
        </div>
        <div class="controls">
          <button id="surpriseBtn">Show Surprise</button>
        </div>
        <footer>I failed as your man.</footer>
      </div>
     <aside class="side photo">
        <img id="mainPhoto" src="ashley.jpg" style="opacity:0lt">
        <div class="caption">Look You're so beautiful ✨</div>
      </aside>
    </div>
 
      
    
  </div>

  <script>
    const photos = [
      "baby2.jpg",
      "baby3.jpg",
      "baby4.jpg",
      "baby5.jpg",
    ];

    let index = 0;
    const mainPhoto = document.getElementById('mainPhoto');

    function changePhoto(){
      index = (index + 1) % photos.length;
      mainPhoto.style.opacity = 0;
      setTimeout(()=>{
        mainPhoto.src = photos[index];
        mainPhoto.style.opacity = 1;
      }, 1000);
    }

    setInterval(changePhoto, 4000);

    document.getElementById('surpriseBtn').addEventListener('click', ()=>{
      document.getElementById('longmsg').textContent = "I felt Lonely nung nawala ka, but it's okay you atleast you're happy now, i like to say that, mahal kita, minahal kita. i will stop coming to you, sorry for being not good enough, i'm really sorry for what i did, maybe in another universe it will be you and me.";
    });
  </script>
</body>

