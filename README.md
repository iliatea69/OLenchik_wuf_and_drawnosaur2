<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<title>Да или Нет</title>
<style>
body {
    background: #111;
    color: white;
    font-family: Arial, sans-serif;
    text-align: center;
    margin-top: 100px;
}

button {
    padding: 15px 30px;
    font-size: 20px;
    margin: 10px;
    cursor: pointer;
}

#result {
    margin-top: 30px;
    display: none;
}

img {
    max-width: 400px;
    border-radius: 10px;
}
</style>
</head>
<body>

<h2>Нажми кнопку</h2>

<button onclick="showYes()">Да</button>
<button onclick="showNo()">Нет</button>

<div id="result">
    <img id="image" src="" alt="">
    <h1 id="text"></h1>
</div>

<script>
function showYes() {
    document.getElementById("image").src =
        "https://via.placeholder.com/400x250?text=ДА";
    document.getElementById("text").innerText =
        "привет я говорил что могу и смог ))) @iliatea69";
    document.getElementById("result").style.display = "block";
}

function showNo() {
    document.getElementById("image").src =
        "https://via.placeholder.com/400x250?text=НЕТ";
    document.getElementById("text").innerText =
        "привет я говорил что могу и смог ))) @iliatea69";
    document.getElementById("result").style.display = "block";
}
</script>

</body>
</html>
