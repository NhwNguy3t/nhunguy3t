# nhunguy3t
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chúc mừng 8/3!</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ffe6f2;
            color: #d63384;
            padding: 50px;
            position: relative;
        }
        .container {
            max-width: 600px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            position: relative;
        }
        h1 {
            font-size: 36px;
        }
        p {
            font-size: 20px;
        }
        .name {
            font-weight: bold;
            color: #ff4081;
        }
        .btn {
            background-color: #ff4081;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 18px;
            margin-top: 20px;
        }
        .flower {
            position: absolute;
            width: 50px;
            animation: fall 4s linear infinite;
        }
        @keyframes fall {
            0% { transform: translateY(-100px); opacity: 1; }
            100% { transform: translateY(100vh); opacity: 0; }
        }
        .decor {
            width: 100px;
            position: absolute;
            bottom: -20px;
            right: -20px;
        }
        .heart {
            position: absolute;
            width: 80px;
            top: 10px;
            left: 10px;
        }
    </style>
</head>
<body>
    <audio autoplay loop>
        <source src="https://www.bensound.com/bensound-music/bensound-sunny.mp3" type="audio/mpeg">
        Trình duyệt của bạn không hỗ trợ phát nhạc.
    </audio>
    <div class="container">
        <h1>Chúc mừng ngày 8/3!</h1>
        <p id="message">Gửi đến tất cả những người phụ nữ tuyệt vời, chúc các bạn luôn xinh đẹp, mạnh mẽ và hạnh phúc!</p>
        <p>Chúc mừng từ <span class="name">Nguyễn Thị Như Nguyệt</span> ❤️</p>
        <p>Đặc biệt gửi lời chúc đến các chị em phòng 109!</p>
        <button class="btn" onclick="changeMessage()">Nhận lời chúc mới</button>
        <img src="https://cdn.pixabay.com/photo/2016/03/27/18/21/bouquet-1283607_1280.png" alt="Bó hoa hồng" class="decor">
        <img src="https://cdn.pixabay.com/photo/2017/09/18/16/52/heart-2761524_1280.png" alt="Trái tim lấp lánh" class="heart">
    </div>
    <script>
        const messages = [
            "Chúc các chị em 109 có ngày 8/3 siêu nhiều quà, nhiều niềm vui, may mắn nha!",
            "Chúc mọi người luôn xinh đẹp, rạng rỡ và hạnh phúc!",
            "Chúc mọi người luôn nở nụ cười trên môi!",
            "Chúc bạn có một ngày 8/3 tràn đầy yêu thương và niềm vui!",
            "Mong rằng nụ cười của bạn luôn rạng rỡ như ánh mặt trời!"
        ];
        function changeMessage() {
            const randomIndex = Math.floor(Math.random() * messages.length);
            document.getElementById("message").innerText = messages[randomIndex];
        }
        function createFlower() {
            const flower = document.createElement("img");
            flower.src = "https://upload.wikimedia.org/wikipedia/commons/thumb/4/4f/Pink_rose_flower.png/120px-Pink_rose_flower.png";
            flower.className = "flower";
            flower.style.left = Math.random() * window.innerWidth + "px";
            document.body.appendChild(flower);
            setTimeout(() => document.body.removeChild(flower), 4000);
        }
        setInterval(createFlower, 1000);
    </script>
</body>
</html>
