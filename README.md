<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pooja I Love You</title>
    <style>
        body, html { 
            margin: 0; 
            padding: 0; 
            height: 100%; 
            font-family: 'Arial', sans-serif; 
            overflow: hidden; 
            background-color: #000; 
        }
        .page { 
            display: none; 
            height: 100vh; 
            width: 100vw; 
            background-size: cover; 
            background-position: center; 
            background-repeat: no-repeat; 
            flex-direction: column; 
            justify-content: center; 
            align-items: center; 
            text-align: center; 
        }
        .active { display: flex; }
        .overlay { 
            background: rgba(0, 0, 0, 0.5); 
            padding: 30px; 
            border-radius: 15px; 
            color: white; 
            margin: 20px; 
            backdrop-filter: blur(5px);
        }
        h1 { font-size: 2rem; margin-bottom: 20px; line-height: 1.4; }
        button { 
            padding: 15px 35px; 
            font-size: 1.2rem; 
            margin: 10px; 
            cursor: pointer; 
            border: none; 
            border-radius: 50px; 
            font-weight: bold; 
            transition: 0.3s;
        }
        .btn-yes { background-color: #ff4d6d; color: white; }
        .btn-no { background-color: #ffffff; color: #333; }
        .heart-text { 
            font-size: 3.5rem; 
            animation: pulse 1.5s infinite; 
            color: #ff4d6d; 
            text-shadow: 0 0 10px rgba(255,255,255,0.3);
        }
        @keyframes pulse { 
            0% { transform: scale(1); } 
            50% { transform: scale(1.1); } 
            100% { transform: scale(1); } 
        }
    </style>
</head>
<body>

    <div id="page1" class="page active" style="background-image: url('IMG_9405.png');">
        <div class="overlay">
            <h1>If you think Amit is smarter than you, click here!</h1>
            <button class="btn-yes" onclick="nextPage(2)">CLICK HERE</button>
        </div>
    </div>

    <div id="page2" class="page" style="background-image: url('IMG_9755.png');">
        <div class="overlay">
            <h1>Do you love Amit?</h1>
            <button class="btn-yes" onclick="nextPage(3)">YES</button>
            <button class="btn-no" onclick="notAnOption()">NO</button>
        </div>
    </div>

    <div id="page3" class="page" style="background-image: url('IMG_9899.png');">
        <div class="overlay">
            <h1>I’m sorry Pooja, do you forgive me?</h1>
            <button class="btn-yes" onclick="nextPage(4)">YES</button>
            <button class="btn-no" onclick="notAnOption()">NO</button>
        </div>
    </div>

    <div id="page4" class="page" style="background-image: url('IMG_9941.png');">
        <div class="overlay">
            <h1>Do you love Amit?</h1>
            <button class="btn-yes" onclick="nextPage(5)">YES</button>
            <button class="btn-no" onclick="notAnOption()">NO</button>
        </div>
    </div>

    <div id="page5" class="page" style="background-image: url('IMG_9950.png');">
        <div class="overlay">
            <h1 class="heart-text">Pooja ❤️ Amit</h1>
            <h1 style="color: #ffd700; font-size: 1.8rem;">लग्न पुढच्या वर्षी हा 😉</h1>
        </div>
    </div>

    <script>
        function nextPage(num) {
            document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
            document.getElementById('page' + num).classList.add('active');
        }
        function notAnOption() { 
            alert("It’s not an option!"); 
        }
    </script>
</body>
</html>
