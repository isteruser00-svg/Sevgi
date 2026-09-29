<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Kalp</title>

<style>
body {
    margin: 0;
    height: 100vh;
    background: #111;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
}

.heart {
    font-size: 100px;
    cursor: pointer;
    transition: transform 0.3s;
    user-select: none;
}

.heart:active {
    transform: scale(1.5);
}

.heart.grow {
    animation: buyu 0.7s ease;
}

@keyframes buyu {
    0% {
        transform: scale(1);
    }

    50% {
        transform: scale(1.6);
    }

    100% {
        transform: scale(1);
    }
}
</style>
</head>

<body>

<div class="heart" onclick="kalp()">❤️</div>

<script>
function kalp() {
    const kalp = document.querySelector(".heart");

    kalp.classList.remove("grow");

    void kalp.offsetWidth;

    kalp.classList.add("grow");
}
</script>

</body>
</html>
