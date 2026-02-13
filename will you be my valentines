<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Will You Be My Valentine?</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    background: linear-gradient(to bottom right, #ffccd5, #ffc2d1);
    overflow: hidden;
    text-align: center;
    transition: all 0.5s ease;
}

h1 {
    margin-top: 100px;
    font-size: 40px;
    color: #b30059;
}

p {
    font-size: 20px;
    color: #660033;
}

button {
    padding: 15px 30px;
    font-size: 18px;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    margin: 20px;
    transition: all 0.3s ease;
}

#yesBtn {
    background-color: #ff4d6d;
    color: white;
}

#noBtn {
    background-color: white;
    color: #ff4d6d;
    position: absolute;
}

.bigYes {
    font-size: 60px !important;
    padding: 40px 80px !important;
    transform: scale(1.5);
}

#reaction {
    font-size: 24px;
    color: #b30059;
    margin-top: 20px;
}

#finalMessage {
    display: none;
    font-size: 28px;
    color: #b30059;
    margin-top: 40px;
}

#kitty {
    display: none;
    width: 300px;
    margin-top: 20px;
}

.heart {
    position: absolute;
    animation: float 6s linear infinite;
}

@keyframes float {
    0% { transform: translateY(0); opacity: 1; }
    100% { transform: translateY(-100vh); opacity: 0; }
}
</style>
</head>

<body>

<div id="mainContent">
    <h1>Will You Be My Valentine? 💖</h1>
    <p>You make my world brighter every single day.</p>

    <button id="yesBtn">Yes 🥰</button>
    <button id="noBtn">No 😏</button>

    <div id="reaction"></div>
</div>

<div id="finalMessage">
    <div>You just made me the happiest boyfriend alive 🥹</div>
    <img id="kitty" src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" alt="Dancing Kitty">
</div>

<script>

const noBtn = document.getElementById("noBtn");
const yesBtn = document.getElementById("yesBtn");
const reaction = document.getElementById("reaction");
const mainContent = document.getElementById("mainContent");
const finalMessage = document.getElementById("finalMessage");
const kitty = document.getElementById("kitty");
const body = document.body;

let noCount = 0;
let heartInterval;

const messages = [
    "what the fk 😭",
    "bro press yes 😭",
    "are you serious right now",
    "this button is broken",
    "okay stop playing",
    "fk u"
];

function moveButton() {
    const x = Math.random() * (window.innerWidth - 120);
    const y = Math.random() * (window.innerHeight - 60);
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
}

noBtn.addEventListener("click", function() {
    reaction.innerText = messages[noCount];

    if (noCount === messages.length - 1) {
        noBtn.style.display = "none";
        yesBtn.classList.add("bigYes");
        body.style.transform = "scale(1.05)";
    } else {
        moveButton();
    }

    noCount++;
});

yesBtn.addEventListener("click", function() {
    // Stop hearts
    clearInterval(heartInterval);

    // Hide everything
    mainContent.style.display = "none";

    // Remove background gradient
    body.style.background = "#ffffff";

    // Show final screen
    finalMessage.style.display = "block";
    kitty.style.display = "block";
});

// Floating hearts
function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "💖";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = Math.random() * 20 + 20 + "px";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 6000);
}

heartInterval = setInterval(createHeart, 300);

</script>

</body>
</html>