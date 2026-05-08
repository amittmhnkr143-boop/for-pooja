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
            position: relative;
        }

        /* Active Page */
        .active { display: flex; }

        /* Overlay to make text readable */
        .overlay {
            background: rgba(0, 0, 0, 0.4);
            padding: 40px;
            border-radius: 20px;
            color: white;
            box-shadow: 0 0 20px rgba(0,0,0,0.5);
        }

        h1 { font-size: 2.5rem; margin-bottom: 30px; }

        button {
            padding: 15px 40px;
            font-size: 1.2rem;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 50px;
            transition: transform 0.2s;
        }

        .btn-yes { background-color: #ff4d6d; color: white; }
        .btn-no { background-color: #6c757d; color: white; }
        
        button:hover { transform: scale(1.1); }

        /* Final Page Animation */
        .heart-text {
            font-size: 4rem;
            animation: pulse 1.5s infinite;
            color: #ff4d6d;
            text-shadow: 2px 2px 10px white;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>

    <div id="page1" class="page active" style="background-image: url('image1.jpg');">
        <div class="overlay">
            <h1>If you think Amit is smarter than you, click here!</h1>
            <button class="btn-yes" onclick="nextPage(2)">CLICK HERE</button>
        </div>
    </div>

    <div id="page2" class="page" style="background-image: url('image2.jpg');">
        <div class="overlay">
            <h1>Do you love Amit?</h1>
            <button class="btn-yes" onclick="nextPage(3)">YES</button>
            <button class="btn-no" onclick="notAnOption()">NO</button>
        </div>
    </div>

    <div id="page3" class="page" style="background-image: url('image3.jpg');">
        <div class="overlay">
            <h1>I’m sorry Pooja, do you forgive me?</h1>
            <button class="btn-yes" onclick="nextPage(4)">YES</button>
            <button class="btn-no" onclick="notAnOption()">NO</button>
        </div>
    </div>

    <div id="page4" class="page" style="background-image: url('image4.jpg');">
        <div class="overlay">
            <h1>Do you love Amit?</h1>
            <button class="btn-yes" onclick="nextPage(5)">YES</button>
            <button class="btn-no" onclick="notAnOption()">NO</button>
        </div>
    </div>

    <div id="page5" class="page" style="background-image: url('image5.jpg');">
        <div class="overlay">
            <h1 class="heart-text">Pooja ❤️ Amit</h1>
            <h1 style="color: #ffd700;">लग्न पुढच्या वर्षी हा 😉</h1>
        </div>
    </div>

    <script>
        function nextPage(pageNumber) {
            // Hide all pages
            document.querySelectorAll('.page').forEach(page => {
                page.classList.remove('active');
            });
            // Show requested page
            document.getElementById('page' + pageNumber).classList.add('active');
        }

        function notAnOption() {
            alert("It’s not an option!");
        }
    </script>
</body>
</html>
