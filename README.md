<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ELOHH 💗</title>

<style>
*{box-sizing:border-box;}

body{
    margin:0;
    font-family:'Segoe UI', sans-serif;
    background: linear-gradient(180deg,#ffd1dc,#ff9acb,#ff5fa2);
    min-height:100vh;
}

/* FUNDO */
.heart{
    position:fixed;
    animation: float 8s linear infinite;
    pointer-events:none;
    opacity:0.4;
}

@keyframes float{
    0%{transform:translateY(110vh) scale(0.6);}
    100%{transform:translateY(-10vh) scale(1.2);opacity:0;}
}

/* TÍTULO */
h1{
    text-align:center;
    font-size:38px;
    margin:25px 10px 5px;
    background: linear-gradient(45deg,#fff,#ffb6c1,#ff1493);
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
}

.subtitle{
    text-align:center;
    color:white;
    font-size:16px;
    margin-bottom:20px;
}

/* CARD PRINCIPAL */
.container{
    margin:0 12px 30px;
    background:rgba(255,255,255,0.22);
    backdrop-filter:blur(12px);
    padding:18px;
    border-radius:28px;
    box-shadow:0 10px 30px rgba(0,0,0,0.15);
}

/* FOTOS */
.photos{
    display:flex;
    flex-direction:column;
    gap:20px;
}

/* CARD DE FOTO */
.photo-card{
    width:100%;
    border-radius:24px;
    overflow:hidden;
    background:white;
    box-shadow:0 8px 25px rgba(0,0,0,0.18);
}

/* PROPORÇÃO BONITA (NÃO ESTICA) */
.photo-frame{
    width:100%;
    aspect-ratio: 4 / 5;   /* formato vertical bonito */
    overflow:hidden;
}

.photo-frame img{
    width:100%;
    height:100%;
    object-fit:cover;      /* NÃO DISTORCE */
    display:block;
}

/* TEXTO */
.message{
    margin-top:25px;
    text-align:center;
    color:white;
    font-size:18px;
    line-height:1.5;
}

/* BOTÕES */
.music-box{
    margin-top:28px;
    display:flex;
    flex-direction:column;
    gap:16px;
}

.btn{
    width:100%;
    padding:18px;
    font-size:18px;
    border-radius:50px;
    border:none;
    cursor:pointer;
    text-align:center;
    text-decoration:none;
    color:white;
    background:linear-gradient(135deg,#ff69b4,#ff1493);
    box-shadow:0 6px 20px rgba(0,0,0,0.25);
    transition:transform .2s;
}

.btn:active{
    transform:scale(0.97);
}

.btn.youtube{
    background:linear-gradient(135deg,#ffb6c1,#ff69b4);
}

footer{
    text-align:center;
    color:white;
    font-size:13px;
    margin:25px 0;
}

/* PC */
@media(min-width:768px){
    .container{
        max-width:500px;
        margin:20px auto 40px;
    }
}
</style>
</head>

<body>

<script>
for(let i=0;i<30;i++){
    const h=document.createElement("div");
    h.className="heart";
    h.innerHTML="💖";
    h.style.left=Math.random()*100+"vw";
    h.style.fontSize=(16+Math.random()*26)+"px";
    h.style.animationDuration=(5+Math.random()*6)+"s";
    document.body.appendChild(h);
}
</script>

<h1>ELOHH 💗</h1>
<p class="subtitle">Cada momento com você é eterno</p>

<div class="container">

    <div class="photos">

        <div class="photo-card">
            <div class="photo-frame">
                <img src="1000001185.jpg">
            </div>
        </div>

        <div class="photo-card">
            <div class="photo-frame">
                <img src="1000006544.jpg">
            </div>
        </div>

        <div class="photo-card">
            <div class="photo-frame">
                <img src="1000012733.jpg">
            </div>
        </div>

    </div>

    <div class="message">
        <p>💌 Você é o meu lugar seguro.</p>
        <p>Com você, todos os dias são especiais 💕</p>
    </div>

    <div class="music-box">
        <button class="btn" onclick="toggleMusica()">🎶 Tocar música</button>

        <a class="btn youtube"
           href="https://youtu.be/j_a55VGxiEU"
           target="_blank">
           ▶️ Abrir vídeo no YouTube
        </a>
    </div>

</div>

<footer>
Feito com amor infinito 💞
</footer>

<audio id="musica" loop>
    <source src="Carol e Junior - Grava essa ideia(MP3_160K).mp3">
</audio>

<script>
let tocando=false;
function toggleMusica(){
    const m=document.getElementById("musica");
    if(!tocando){m.play();tocando=true;}
    else{m.pause();tocando=false;}
}
</script>

</body>
</html>

