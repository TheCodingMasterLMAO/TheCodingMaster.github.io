<!DOCTYPE html>
<html>
<head>
    <style>
        body {
            margin: 0;
            background-color: #000;
            color: #fff;
            margin-bottom: 2000px;
        }

        header {
            background-color: #333;
            padding: 10px 0;
            text-align: center;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
        }

        .digital-watch {
            display: inline-block;
            max-width: 120px;
            margin: 10px;
            background-color: #222;
            border: 2px solid #444;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
            margin-left: 100px;
            z-index: 999;
        }

        #time {
            font-size: 2em;
        }

        .audio-Etude {
            margin-top: 140px;
            margin-left: 1500px;
        }

        .header-buttons {
            background-color: #555;
            color: #fff;
            border: none;
            padding: 10px;
            margin: 0 10px; /* Adjusted margin for gap */
            cursor: pointer;
            border-radius: 5px;
            opacity: 1;
            transition: opacity 0.3s ease;
        }

        .header-buttons:hover {
            opacity: 0.8;
        }

        /* Center align the header buttons */
        header > div {
            display: flex;
            align-items: center;
            margin-right: 10px; /* Adjusted margin for space between buttons */
        }

    </style>
</head>
<body>
    <header>
        <div class="digital-watch">
            <div id="time"></div>
        </div>
        <div>
          <a href="http://127.0.0.1:5500/Calculator.html" target="_blank" >
            <button class="header-buttons">Calculator</button>
          </a>
           <a href="https://www.youtube.com/" target="_blank">
            <button class="header-buttons">Youtube</button>
           </a>
        <a href="https://agar.io/" target="_blank">
          <button class="header-buttons">Agar.io Game</button>
        </a>
        <a href="http://127.0.0.1:5500/RockPaperScissors.html" target="_blank">
          <button class="header-buttons">Rock Paper Scissors Game</button>
        </a>
            
        </div>
    </header>
    <audio class="audio-Etude" controls>
      <source src="PaganiniLiszt  Etude No 6.mp3" type="audio/mpeg">
    </audio>
    
    <script>
        function updateClock() {
            const now = new Date();
            const hours = String(now.getHours()).padStart(2, '0');
            const minutes = String(now.getMinutes()).padStart(2, '0');
            const seconds = String(now.getSeconds()).padStart(2, '0');
            
            const timeString = `${hours}:${minutes}:${seconds}`;
            document.getElementById('time').textContent = timeString;
        }

        setInterval(updateClock, 1000);
        updateClock();
    </script>
</body>
</html>

