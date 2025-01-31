<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Will You Be My Valentine? ❤️</h1>
        <div class="buttons">
            <button id="yesBtn">Yes</button>
            <button id="noBtn">No</button>
        </div>
    </div>

    <div id="popup" class="hidden">
        <h2>Yay! ❤️</h2>
        <p>I'm so happy! Can't wait to celebrate together! 🎉</p>
        <img src="hearts.gif" alt="Hearts">
    </div>

    <script src="script.js"></script>
</body>
</html>

body {
    text-align: center;
    font-family: Arial, sans-serif;
    background-color: #ffccdc;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    flex-direction: column;
}

.container {
    background: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.2);
}

h1 {
    color: #ff4d6d;
}

.buttons {
    margin-top: 20px;
}

button {
    font-size: 18px;
    padding: 10px 20px;
    margin: 10px;
    border: none;
    cursor: pointer;
    border-radius: 5px;
}

#yesBtn {
    background-color: #ff4d6d;
    color: white;
}

#noBtn {
    background-color: black;
    color: white;
    position: absolute;
}

.hidden {
    display: none;
}

#popup {
    margin-top: 30px;
    font-size: 24px;
    background: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.2);
}

img {
    width: 100px;
    margin-top: 10px;
}

document.getElementById("yesBtn").addEventListener("click", function() {
    document.getElementById("popup").classList.remove("hidden");
});

document.getElementById("noBtn").addEventListener("mouseover", function() {
    let x = Math.random() * window.innerWidth;
    let y = Math.random() * window.innerHeight;
    this.style.left = x + "px";
    this.style.top = y + "px";
});