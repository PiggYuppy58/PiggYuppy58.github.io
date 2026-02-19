<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🎮 piggyuppy58 game launcher</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            font-family: 'Segoe UI', Roboto, system-ui, sans-serif;
            background: linear-gradient(145deg, #1a2f3f 0%, #102129 100%);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 2rem 1rem;
        }
        .launcher-card {
            max-width: 1300px;
            width: 100%;
            background: rgba(255,255,255,0.05);
            backdrop-filter: blur(8px);
            -webkit-backdrop-filter: blur(8px);
            border-radius: 3rem;
            padding: 2.5rem 2rem;
            box-shadow: 0 20px 40px rgba(0,0,0,0.6), 0 0 0 1px rgba(255,255,255,0.03);
            border: 1px solid rgba(255,255,255,0.06);
        }
        h1 {
            text-align: center;
            font-weight: 500;
            font-size: 2.5rem;
            letter-spacing: 1px;
            color: #f1e9db;
            text-shadow: 0 4px 10px #00000040;
            margin-bottom: 1rem;
        }
        .sub {
            text-align: center;
            color: #a0b8cc;
            margin-bottom: 2.5rem;
            font-size: 1.2rem;
            border-bottom: 1px dashed #3d5567;
            padding-bottom: 1rem;
        }
        .button-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
            align-items: center;
        }
        .game-btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            background: #2f455b;
            color: #f5f0e6;
            padding: 0.9rem 1.8rem;
            border-radius: 60px;
            font-size: 1rem;
            font-weight: 500;
            text-decoration: none;
            letter-spacing: 0.3px;
            border: 1px solid #5b7a98;
            box-shadow: 0 8px 0 #1b2a36, 0 6px 12px black;
            transition: all 0.1s ease-out;
            text-align: center;
            line-height: 1.4;
            min-width: 180px;
            backdrop-filter: blur(4px);
            word-break: break-word;
            cursor: pointer;
        }
        .game-btn:hover {
            background: #3e5a75;
            border-color: #8ab3d0;
            transform: translateY(-2px);
            box-shadow: 0 10px 0 #1b2a36, 0 10px 18px black;
        }
        .game-btn:active {
            transform: translateY(5px);
            box-shadow: 0 4px 0 #1b2a36, 0 8px 12px black;
        }
        /* special accent for variety */
        .game-btn:nth-child(4n+1) {
            background: #3d2e4b;
            border-color: #9f7fc2;
        }
        .game-btn:nth-child(4n+2) {
            background: #1f4a4a;
            border-color: #4caaaa;
        }
        .game-btn:nth-child(4n+3) {
            background: #733e3e;
            border-color: #d18a8a;
        }
        footer {
            margin-top: 2.5rem;
            color: #7f95ab;
            font-size: 0.9rem;
        }
        .note {
            background: #0b1a24;
            padding: 0.6rem 1.5rem;
            border-radius: 40px;
            display: inline-block;
            color: #b6cdff;
            border: 1px solid #2c4d5e;
        }
    </style>
</head>
<body>
    <div class="launcher-card">
        <h1>🚀 piggyuppy58 · game hub</h1>
        <div class="sub">click any button to launch the game (opens in new tab)</div>

        <div class="button-grid">
            <!-- all links from the list, with human readable labels -->
            <a href="https://piggyuppy58.github.io/Block%20Blast.html" class="game-btn" target="_blank" rel="noopener">📦 Block Blast</a>
            <a href="https://piggyuppy58.github.io/Color%20Water%20Sort%203D.html" class="game-btn" target="_blank" rel="noopener">💧 Color Water Sort 3D</a>
            <a href="https://piggyuppy58.github.io/Five%20Nights%20at%20Epstein's.html" class="game-btn" target="_blank" rel="noopener">🌙 Five Nights at Epstein's</a>
            <a href="https://piggyuppy58.github.io/Five%20Nights%20at%20Freddy's%202.html" class="game-btn" target="_blank" rel="noopener">🐻 FNaF 2</a>
            <a href="https://piggyuppy58.github.io/Five%20Nights%20at%20Freddy's%203.html" class="game-btn" target="_blank" rel="noopener">🐰 FNaF 3</a>
            <a href="https://piggyuppy58.github.io/Five%20Nights%20at%20Freddy's%204.html" class="game-btn" target="_blank" rel="noopener">👻 FNaF 4</a>
            <a href="https://piggyuppy58.github.io/Five%20Nights%20at%20Freddy's.html" class="game-btn" target="_blank" rel="noopener">🎪 Five Nights at Freddy's</a>
            <a href="https://piggyuppy58.github.io/Geometry%20Dash%20Lite%20(REMAKE).html" class="game-btn" target="_blank" rel="noopener">🔷 Geometry Dash Lite (REMAKE)</a>
            <a href="https://piggyuppy58.github.io/Google%20Feud.html" class="game-btn" target="_blank" rel="noopener">🔎 Google Feud</a>
            <a href="https://piggyuppy58.github.io/Minecraft%201.12.2.html" class="game-btn" target="_blank" rel="noopener">⛏️ Minecraft 1.12.2</a>
            <a href="https://piggyuppy58.github.io/Minecraft%201.21.4.html" class="game-btn" target="_blank" rel="noopener">🪓 Minecraft 1.21.4</a>
            <a href="https://piggyuppy58.github.io/Minecraft%20Indev.html" class="game-btn" target="_blank" rel="noopener">🗺️ Minecraft Indev</a>
            <a href="https://piggyuppy58.github.io/R.E.P.O.html" class="game-btn" target="_blank" rel="noopener">⚙️ R.E.P.O</a>
            <a href="https://piggyuppy58.github.io/Terraria.html" class="game-btn" target="_blank" rel="noopener">🌳 Terraria</a>
        </div>

        <footer>
            <span class="note">🎯 buttons open directly — all games hosted by piggyuppy58</span>
        </footer>
    </div>

    <!-- small extra style for stacked small screens -->
    <style>
        @media (max-width: 650px) {
            .launcher-card { padding: 1.5rem 1rem; }
            h1 { font-size: 1.9rem; }
            .game-btn { min-width: 140px; padding: 0.8rem 1rem; font-size: 0.95rem; }
        }
        @media (max-width: 420px) {
            .button-grid { gap: 0.7rem; }
            .game-btn { min-width: 100%; }
        }
    </style>
</body>
</html>
