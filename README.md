<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>❤️ لينا</title>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700;900&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Cairo', sans-serif;
    background: #0f0f0f;
    color: white;
    overflow: hidden;
    text-align: center;
}

/* 🎬 Intro */
#intro {
    position: fixed;
    width: 100%;
    height: 100%;
    background: black;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    z-index: 9999;
}

.glow {
    width: 20px;
    height: 20px;
    background: #ff4d6d;
    border-radius: 50%;
    animation: grow 2s forwards;
}

@keyframes grow {
    to {
        transform: scale(40);
        opacity: 0;
    }
}

#introText {
    position: absolute;
    font-size: 22px;
    font-weight: 700;
}

/* 🔐 Password */
#lock {
    display: none;
    height: 100vh;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background: linear-gradient(135deg, #1a1a1a, #2c2c2c);
}

.phone {
    background: rgba(17, 17, 17, 0.8);
    backdrop-filter: blur(10px);
    padding: 25px;
    border-radius: 30px;
    box-shadow: 0 0 40px rgba(255, 0, 100, 0.4);
    border: 1px solid rgba(255, 255, 255, 0.1);
}

.display {
    height: 50px;
    margin-bottom: 15px;
    letter-spacing: 15px;
    font-size: 30px;
    background: rgba(0,0,0,0.3);
    border-radius: 15px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.keys {
    display: grid;
    grid-template-columns: repeat(3, 75px);
    gap: 12px;
    justify-content: center;
}

.key {
    background: #222;
    padding: 18px;
    border-radius: 18px;
    cursor: pointer;
    transition:.2s;
    font-size: 20px;
    font-weight: 700;
    border: 1px solid rgba(255, 255, 255, 0.05);
}

.key:active {
    transform: scale(0.9);
    background: #ff4d6d;
    box-shadow: 0 0 20px #ff4d6d;
}

#error {
    color: #ff4d6d;
    margin-top: 15px;
    height: 20px;
}

/* 💌 message */
#message {
    display: none;
    padding: 30px;
    font-size: 22px;
    line-height: 2;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}

/* 😏 kiss */
#kiss {
    display: none;
    height: 100vh;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 20px;
}

/* ❤️ hearts */
.heart {
    position: fixed;
    color: #ff4d6d;
    animation: float 2s linear;
    z-index: 999;
    pointer-events: none;
}

@keyframes float {
    to {
        transform: translateY(-100vh) rotate(360deg);
        opacity: 0;
    }
}

/* 🎵 */
#audioSection {
    display: none;
    height: 100vh;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 20px;
}

/* 🖼️ */
#gallery {
    display: none;
    height: 100vh;
    background: #000;
    align-items: center;
    justify-content: center;
}

img {
    max-width: 90%;
    max-height: 90vh;
    border-radius: 25px;
    box-shadow: 0 0 50px rgba(255, 77, 109, 0.5);
    transition: 1s;
}

/* 📖 الكتاب الجديد */
#book {
    display: none;
    height: 100vh;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 30px;
    background: linear-gradient(135deg, #2a1a1f, #1a1a1a);
}

.book-frame {
    width: 320px;
    height: 450px;
    background: linear-gradient(145deg, #3d2b2f, #2a1a1f);
    border-radius: 5px 20px 5px;
    box-shadow: 
        0 0 30px rgba(255, 77, 109, 0.3),
        inset -5px 0 15px rgba(0,0,0,0.5),
        5px 5px 20px rgba(0,0,0,0.8);
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 40px;
    border-right: 8px solid #1a0f11;
}

.book-frame::before {
    content: '';
    position: absolute;
    right: 0;
    top: 10px;
    bottom: 10px;
    width: 3px;
    background: linear-gradient(to bottom, transparent, #ff4d6d, transparent);
}

#page {
    font-size: 32px;
    font-weight: 900;
    color: #ffd4dc;
    text-shadow: 0 0 10px rgba(255, 77, 109, 0.5);
}

/* ⏳ العداد الجديد */
#counter {
    display: none;
    height: 100vh;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background: linear-gradient(135deg, #ffb3c1, #ff8fa3);
    gap: 30px;
}

.counter-title {
    font-size: 28px;
    font-weight: 900;
    color: white;
    text-shadow: 0 2px 10px rgba(0,0,0,0.2);
}

.counter-cards {
    display: flex;
    gap: 15px;
    flex-wrap: wrap;
    justify-content: center;
    max-width: 400px;
}

.time-card {
    background: white;
    border-radius: 20px;
    padding: 20px 25px;
    min-width: 100px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.15);
    transform: translateY(0);
    transition:.3s;
}

.time-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 40px rgba(0,0,0,0.2);
}

.time-number {
    font-size: 42px;
    font-weight: 900;
    color: #ff4d6d;
    line-height: 1;
}

.time-label {
    font-size: 16px;
    color: #ff8fa3;
    margin-top: 5px;
    font-weight: 700;
}

/* ❤️ الأزرار الأيقونية الخرافية */
.icon-btn {
    padding: 15px 35px;
    background: linear-gradient(135deg, #ff4d6d, #ff8fa3);
    border: none;
    border-radius: 25px;
    color: white;
    font-size: 18px;
    font-weight: 700;
    cursor: pointer;
    box-shadow: 0 5px 20px rgba(255, 77, 109, 0.4);
    transition:.3s;
    display: inline-flex;
    align-items: center;
    gap: 10px;
    position: relative;
    overflow: hidden;
}

.icon-btn::before {
    content: '';
    position: absolute;
    top: 50%;
    left: 50%;
    width: 0;
    height: 0;
    border-radius: 50%;
    background: rgba(255,255,255,0.3);
    transform: translate(-50%, -50%);
    transition:.5s;
}

.icon-btn:hover::before {
    width: 300px;
    height: 300px;
}

.icon-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 30px rgba(255, 77, 109, 0.6);
}

.icon-btn:active {
    transform: translateY(0);
}

#runawayBtn {
    position: relative;
    transition:.2s;
}

.btns-container {
    display: flex;
    gap: 20px;
    position: relative;
    height: 60px;
    width: 100%;
    justify-content: center;
}

#loveCount {
    font-size: 24px;
    font-weight: 700;
    margin-top: 15px;
}
</style>
</head>

<body>

<!-- 🎬 Intro -->
<div id="intro">
    <div class="glow"></div>
    <p id="introText">في حكاية بدأت من غير ما ناخد بالنا…</p>
</div>

<!-- 🔐 Password -->
<div id="lock">
    <p style="font-size: 20px; margin-bottom: 20px;">المكان ده لينا بس 🤍</p>
    <div class="phone">
        <div class="display" id="display"></div>
        <div class="keys">
            <div class="key">1</div><div class="key">2</div><div class="key">3</div>
            <div class="key">4</div><div class="key">5</div><div class="key">6</div>
            <div class="key">7</div><div class="key">8</div><div class="key">9</div>
            <div class="key" style="grid-column: 2;">0</div>
        </div>
    </div>
    <p id="error"></p>
</div>

<!-- 💌 -->
<div id="message"></div>

<!-- 😏 -->
<div id="kiss">
    <p id="kissText" style="font-size: 26px; font-weight: 700;">مش هتعدي غير لما تديني بوسة 😏</p>
    <div class="btns-container">
        <button class="icon-btn" onclick="kiss()">
            <i class="fa-solid fa-lips"></i> امواااه
        </button>
        <button class="icon-btn" id="runawayBtn" style="background: linear-gradient(135deg, #6c757d, #495057);">
            <i class="fa-solid fa-face-frown"></i> لا مش هديك
        </button>
    </div>
</div>

<!-- 🎵 -->
<div id="audioSection">
    <p style="font-size: 24px; font-weight: 700;">دوسي هنا عشان تسمعي قلبنا 🎧</p>
    <audio id="song" src="song.mp3"></audio>
    <button class="icon-btn" onclick="playSong()">
        <i class="fa-solid fa-play"></i> تشغيل
    </button>
</div>

<!-- 🖼️ -->
<div id="gallery">
    <img id="img" src="img1.jpg">
</div>

<!-- 📖 -->
<div id="book">
    <div class="book-frame">
        <p id="page"></p>
    </div>
    <button class="icon-btn" onclick="nextPage()">
        <i class="fa-solid fa-book-open"></i> اقلب الصفحة
    </button>
</div>

<!-- ⏳ -->
<div id="counter">
    <h2 class="counter-title">الوقت اللي قضيناه مع بعض ⏳</h2>
    <div class="counter-cards">
        <div class="time-card">
            <div class="time-number" id="days">0</div>
            <div class="time-label">يوم</div>
        </div>
        <div class="time-card">
            <div class="time-number" id="hours">0</div>
            <div class="time-label">ساعة</div>
        </div>
        <div class="time-card">
            <div class="time-number" id="minutes">0</div>
            <div class="time-label">دقيقة</div>
        </div>
        <div class="time-card">
            <div class="time-number" id="seconds">0</div>
            <div class="time-label">ثانية</div>
        </div>
    </div>
    <button class="icon-btn" onclick="love()">
        <i class="fa-solid fa-heart"></i> بتحبني قد اي
    </button>
    <p id="loveCount"></p>
</div>

<script>
// 🎬 intro
setTimeout(() => {
    document.getElementById("intro").style.display = "none";
    document.getElementById("lock").style.display = "flex";
}, 3000);

// 🔐 password
let pass = "2024326";
let input = "";
document.querySelectorAll(".key").forEach(k => {
    k.onclick = () => {
        if (input.length >= pass.length) return;
        input += k.innerText;
        document.getElementById("display").innerText = "*".repeat(input.length);

        if (input.length == pass.length) {
            if (input == pass) {
                document.getElementById("lock").style.display = "none";
                startMessage();
            } else {
                document.getElementById("error").innerText = "غلط 😏 ركزي";
                input = "";
                setTimeout(() => {
                    document.getElementById("display").innerText = "";
                    document.getElementById("error").innerText = "";
                }, 1000);
            }
        }
    }
});

// 💌 typing
let text = [
    "فاكرة أول مرة اتكلمنا فيها؟",
    "أنا بحبك بطريقة مش بعرف أشرحها",
    "بس بحسها كويس أوي ❤️",
    "كملي معايا…"
];
let i = 0;
function startMessage() {
    document.getElementById("message").style.display = "flex";
    type();
}
function type() {
    if (i < text.length) {
        let p = document.createElement("p");
        p.innerText = text[i];
        p.style.opacity = "0";
        p.style.transition = "1s";
        document.getElementById("message").appendChild(p);
        setTimeout(() => p.style.opacity = "1", 100);
        i++;
        setTimeout(type, 2000);
    } else {
        setTimeout(() => {
            document.getElementById("message").style.display = "none";
            document.getElementById("kiss").style.display = "flex";
        }, 2000);
    }
}

// 😏 kiss
let k = 0;
function kiss() {
    k++;
    for (let i = 0; i < 30; i++) {
        let h = document.createElement("div");
        h.className = "heart";
        h.innerText = "❤️";
        h.style.left = Math.random() * 100 + "%";
        h.style.fontSize = (Math.random() * 20 + 10) + "px";
        document.body.appendChild(h);
        setTimeout(() => h.remove(), 2000);
    }
    if (k == 3) {
        document.getElementById("kiss").style.display = "none
