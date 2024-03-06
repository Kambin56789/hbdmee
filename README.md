# hbdmee
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Birthday Gift Box Animation</title>
<style>
    body {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        margin: 0;
        background-color: #f3f3f3;
    }

    .gift-box {
        width: 200px;
        height: 200px;
        background-color: #ff7f50;
        border-radius: 10px;
        position: relative;
        overflow: hidden;
        cursor: pointer;
    }

    .ribbon {
        width: 150px;
        height: 150px;
        border: 20px solid #ffebcd;
        border-radius: 50%;
        position: absolute;
        top: -30px;
        left: 25px;
        transform: rotate(-45deg);
    }

    .lid {
        width: 100%;
        height: 50%;
        background-color: #ffebcd;
        position: absolute;
        top: 0;
        left: 0;
        transform-origin: top;
        transition: transform 1s ease-in-out;
    }

    .box-content {
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        color: #fff;
        font-size: 24px;
        position: absolute;
        top: 0;
        left: 0;
        opacity: 0;
        transition: opacity 1s ease-in-out;
    }

    .gift-box.opened .lid {
        transform: rotateX(-110deg);
    }

    .gift-box.opened .box-content {
        opacity: 1;
    }
    .lid-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 50px;
    color: #fff;
    font-family: Arial, sans-serif;
}

</style>
</head>
<body>
    <div class="gift-box" id="gift-box">
        <div class="ribbon"></div>
        <div class="lid">
            <div class="lid-text">🎁</div>
        </div>
        
        <div class="box-content" id="birthday-text">🎁</div>
    </div>

    <script>
        document.getElementById('gift-box').addEventListener('click', function() {
            this.classList.add('opened');
            document.getElementById('birthday-text').innerText = "🎺 Happy Birthday to Me! 🍰";
            document.getElementById('birthday-text').style.color = "black";
        });
    </script>
    
</body>
</html>
