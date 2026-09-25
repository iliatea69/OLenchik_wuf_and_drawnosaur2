<html lang="ru">
<head>
<meta charset="UTF-8">
<title>Вопрос</title>
<style>
    body {
        background: #111;
        color: white;
        font-family: Arial, sans-serif;
        text-align: center;
        margin-top: 100px;
        overflow: hidden;
    }

    h1 {
        margin-bottom: 40px;
    }

    button {
        padding: 15px 30px;
        font-size: 20px;
        cursor: pointer;
        position: absolute;
    }

    #yesBtn {
        left: 45%;
        top: 250px;
    }

    #noBtn {
        left: 55%;
        top: 250px;
    }

    #result {
        margin-top: 100px;
        font-size: 32px;
        color: #4cff4c;
        display: none;
    }
</style>
</head>
<body>

<h1>
Я могу поиграть чутка )))<br>
Ответьте на вопрос:<br><br>
Вы любите оленьчика?
</h1>

<button id="yesBtn" onclick="correctAnswer()">Да</button>
<button id="noBtn">Нет</button>

<div id="result">
    Молодец, ответ правильный!
</div>

<script>
function correctAnswer() {
    document.getElementById("result").style.display = "block";
}

const noBtn = document.getElementById("noBtn");

document.addEventListener("mousemove", (e) => {
    const rect = noBtn.getBoundingClientRect();

    const distance = Math.sqrt(
        Math.pow(e.clientX - (rect.left + rect.width / 2), 2) +
        Math.pow(e.clientY - (rect.top + rect.height / 2), 2)
    );

    if (distance < 120) {
        const maxX = window.innerWidth - noBtn.offsetWidth;
        const maxY = window.innerHeight - noBtn.offsetHeight;

        noBtn.style.left = Math.random() * maxX + "px";
        noBtn.style.top = Math.random() * maxY + "px";
    }
});
</script>

</body>
</html>
