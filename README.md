<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Girlfriend?</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');
        body {
            text-align: center;
            font-family: 'Pacifico', cursive;
            margin-top: 100px;
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://source.unsplash.com/1600x900/?love,romantic') no-repeat center center fixed; background-color: #ff6699;
            background-size: cover;
            color: white;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        #yes, #no {
            font-size: 20px;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            transition: transform 0.3s;
        }
        #yes {
            background-color: #28a745;
            color: white;
        }
        #no {
            background-color: #dc3545;
            color: white;
        }
        #yes:hover, #no:hover {
            transform: scale(1.1);
        }
    </style>
</head>
<body>
    <h1>For the last one year we've been talking, I've had the time of my life. 💖<br>Every smile, every laugh, every moment with you feels like a blessing.<br>Will you make me the happiest person by being my girlfriend? 💫💕</h1>
    <button id="yes">Yes</button>
    <button id="no">No</button>

    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>
    <script>
        let yesButton = document.getElementById("yes");
        let noButton = document.getElementById("no");

        noButton.addEventListener("click", function() {
            let currentSize = parseInt(window.getComputedStyle(yesButton).fontSize);
            yesButton.style.fontSize = (currentSize + 5) + "px";
        });

        yesButton.addEventListener("click", function() {
            confetti({
                particleCount: 200,
                spread: 100,
                origin: { y: 0.6 }
            });
            alert("Now I'm yours for life ❤️");
        });
    </script>
</body>
</html>
