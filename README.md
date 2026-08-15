<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For You ❤️</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    min-height: 100vh;
    font-family: "Segoe UI", Arial, sans-serif;
    background:
        radial-gradient(circle at top, #3b0a2e, #160014 45%, #050005);
    color: white;
    overflow-x: hidden;
}

/* STARS */
.stars {
    position: fixed;
    inset: 0;
    pointer-events: none;
}

.star {
    position: absolute;
    width: 3px;
    height: 3px;
    background: white;
    border-radius: 50%;
    animation: twinkle 2s infinite alternate;
}

@keyframes twinkle {
    from { opacity: .2; transform: scale(.7); }
    to { opacity: 1; transform: scale(1.4); }
}

/* INTRO */
.intro {
    position: fixed;
    inset: 0;
    z-index: 100;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    background: #080006;
    transition: 1s;
}

.intro.hide {
    opacity: 0;
    visibility: hidden;
}

.intro-box {
    padding: 35px;
}

.big-heart {
    font-size: 90px;
    animation: heartbeat 1.2s infinite;
    filter: drop-shadow(0 0 25px #ff3d81);
}

@keyframes heartbeat {
    0%,100% { transform: scale(1); }
    50% { transform: scale(1.2); }
}

.intro h1 {
    font-size: 32px;
    margin: 20px 0 10px;
}

.intro p {
    opacity: .75;
    margin-bottom: 25px;
}

/* BUTTON */
button {
    border: none;
    padding: 15px 32px;
    border-radius: 50px;
    font-size: 16px;
    font-weight: bold;
    color: white;
    background: linear-gradient(135deg, #ff2f75, #ff0055);
    box-shadow: 0 0 25px rgba(255,0,85,.5);
    cursor: pointer;
    transition: .3s;
}

button:hover {
    transform: scale(1.08);
    box-shadow: 0 0 40px rgba(255,0,85,.8);
}

/* MAIN */
main {
    min-height: 100vh;
    padding: 70px 20px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.card {
    width: 100%;
    max-width: 650px;
    padding: 45px 30px;
    text-align: center;

    background: rgba(255,255,255,.07);
    border: 1px solid rgba(255,255,255,.15);
    border-radius: 30px;

    backdrop-filter: blur(20px);
    box-shadow:
        0 0 50px rgba(255,0,100,.15),
        inset 0 0 30px rgba(255,255,255,.03);
}

.card .heart {
    font-size: 70px;
    filter: drop-shadow(0 0 20px #ff2670);
    animation: heartbeat 1.2s infinite;
}

h2 {
    font-size: 35px;
    margin: 15px 0;
}

.subtitle {
    color: #ff9cbd;
    letter-spacing: 2px;
    font-size: 13px;
    text-transform: uppercase;
}

.message {
    margin-top: 30px;
    text-align: left;
    line-height: 1.9;
    color: #f5dce6;
    font-size: 16px;
}

.message p {
    margin-bottom: 18px;
}

.highlight {
    color: #ff6f9f;
    font-weight: bold;
}

/* SECRET */
.secret {
    display: none;
    margin-top: 30px;
    padding: 25px;
    border-radius: 20px;
    background: rgba(255,20,100,.1);
    border: 1px solid rgba(255,100,150,.25);
    animation: appear 1s ease;
}

@keyframes appear {
    from {
        opacity: 0;
        transform: translateY(25px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.secret h3 {
    font-size: 25px;
    color: #ff82aa;
    margin-bottom: 12px;
}

/* FLOATING HEARTS */
.heart-float {
    position: fixed;
    bottom: -50px;
    font-size: 20px;
    pointer-events: none;
    animation: floatUp 7s linear forwards;
}

@keyframes floatUp {
    0% {
        transform: translateY(0) rotate(0);
        opacity: 0;
    }

    15% {
        opacity: 1;
    }

    100% {
        transform: translateY(-110vh) rotate(360deg);
        opacity: 0;
    }
}

/* FOOTER */
footer {
    text-align: center;
    padding: 20px;
    color: #8d6878;
    font-size: 12px;
}
</style>
</head>

<body>

<!-- STARS -->
<div class="stars" id="stars"></div>

<!-- INTRO SCREEN -->
<section class="intro" id="intro">

    <div class="intro-box">

        <div class="big-heart">❤️</div>

        <h1>I Made Something For You</h1>

        <p>
            There is something I've been wanting to say...
        </p>

        <button onclick="openHeart()">
            Open My Heart 💌
        </button>

    </div>

</section>


<!-- MAIN MESSAGE -->
<main>

<div class="card">

    <div class="heart">💗</div>

    <div class="subtitle">
        A message from my heart
    </div>

    <h2>For Someone Special ❤️</h2>

    <div class="message">

        <p>
            I don't know if I say it enough,
            but <span class="highlight">you mean a lot to me.</span>
        </p>

        <p>
            Since you became part of my life,
            some ordinary days started feeling
            a little more special.
        </p>

        <p>
            Your smile, your words, your presence,
            even the smallest moments with you
            are memories that I genuinely treasure.
        </p>

        <p>
            I don't promise that everything will
            always be perfect. But I can promise
            that whenever I care about someone,
            I care with all my heart.
        </p>

        <p>
            And if you ever wonder how important
            you are to me, just remember this:
            <span class="highlight">
                you are someone I never want to take for granted.
            </span>
        </p>

    </div>

    <button onclick="showSecret()">
        There's One More Thing... 💕
    </button>

    <!-- SECRET MESSAGE -->
    <div class="secret" id="secret">

        <h3>My Little Secret 💌</h3>

        <p>
            If I could choose one person to keep
            making beautiful memories with,
            I'd choose you. ❤️
        </p>

        <p>
            No matter how many people I meet,
            there will always be something
            special about you that I can't explain.
        </p>

        <p>
            <strong>
                Thank you for existing in my world. 🥺❤️
            </strong>
        </p>

        <p>
            — From someone who cares about you deeply.
        </p>

    </div>

</div>

</main>

<footer>
    Made with ❤️ just for you
</footer>


<script>

/* OPEN HEART */
function openHeart() {
    document.getElementById("intro").classList.add("hide");

    setInterval(createHeart, 700);
}


/* SECRET MESSAGE */
function showSecret() {

    const secret = document.getElementById("secret");

    secret.style.display = "block";

    for(let i = 0; i < 15; i++) {
        setTimeout(createHeart, i * 100);
    }
}


/* FLOATING HEARTS */
function createHeart() {

    const heart = document.createElement("div");

    heart.className = "heart-float";

    const emojis = ["❤️","💕","💗","💖","💘","💓"];

    heart.innerHTML =
        emojis[Math.floor(Math.random() * emojis.length)];

    heart.style.left =
        Math.random() * 100 + "vw";

    heart.style.fontSize =
        (15 + Math.random() * 25) + "px";

    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 7000);
}


/* CREATE STARS */
for(let i = 0; i < 80; i++) {

    const star = document.createElement("div");

    star.className = "star";

    star.style.left =
        Math.random() * 100 + "%";

    star.style.top =
        Math.random() * 100 + "%";

    star.style.animationDelay =
        Math.random() * 2 + "s";

    document.getElementById("stars").appendChild(star);
}

</script>

</body>
</html>
