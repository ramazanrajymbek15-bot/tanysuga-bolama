<!DOCTYPE html>
<html lang="kk">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Танысуға бола ма?</title>

<style>
body{
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:#ffd1dc;
    font-family:Arial, sans-serif;
    overflow:hidden;
}

.container{
    text-align:center;
}

h1{
    color:white;
    font-size:36px;
}

.buttons{
    display:flex;
    justify-content:center;
    gap:100px;
    margin-top:20px;
}

button{
    border:none;
    border-radius:8px;
    padding:12px 30px;
    font-size:18px;
    cursor:pointer;
}

#yes{
    background:#28a745;
    color:white;
    transition:0.3s;
}

#no{
    background:#dc3545;
    color:white;
}
</style>
</head>

<body>

<div class="container">
    <h1>Танысуға бола ма?</h1>

    <div class="buttons">
        <button id="yes">Иә</button>
        <button id="no">Жоқ</button>
    </div>
</div>

<script>
const yesBtn = document.getElementById("yes");
const noBtn = document.getElementById("no");

let scale = 1;

noBtn.addEventListener("mouseover", () => {
    scale += 0.2;
    yesBtn.style.transform = `scale(${scale})`;

    let x = Math.random() * (window.innerWidth - 100);
    let y = Math.random() * (window.innerHeight - 50);

    noBtn.style.position = "fixed";
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
});

yesBtn.addEventListener("click", () => {
    alert("Урааа! 🥳");
});
</script>

</body>
</html>
