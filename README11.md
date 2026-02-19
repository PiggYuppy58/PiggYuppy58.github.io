<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🎮 piggyuppy58 · game hub (EN/RU)</title>
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
            position: relative;
        }
        /* language switch */
        .lang-switcher {
            position: absolute;
            top: 1.5rem;
            right: 2rem;
            display: flex;
            gap: 0.3rem;
            background: #1e3343;
            padding: 0.3rem;
            border-radius: 40px;
            border: 1px solid #3e6077;
            box-shadow: 0 4px 6px #00000040;
        }
        .lang-btn {
            background: transparent;
            border: none;
            color: #9bb8d4;
            font-weight: 600;
            font-size: 1rem;
            padding: 0.3rem 1rem;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.15s;
            min-width: 50px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        .lang-btn.active {
            background: #f1e9db;
            color: #1f3c4f;
            box-shadow: 0 2px 6px black;
        }
        h1 {
            text-align: center;
            font-weight: 500;
            font-size: 2.5rem;
            letter-spacing: 1px;
            color: #f1e9db;
            text-shadow: 0 4px 10px #00000040;
            margin-bottom: 1rem;
            padding-right: 100px; /* make room for switcher */
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
        @media (max-width: 750px) {
            h1 { font-size: 2rem; padding-right: 0; margin-top: 1.8rem; }
            .lang-switcher { position: static; justify-content: center; margin-bottom: 1rem; width: fit-content; margin-left: auto; margin-right: auto; }
        }
        @media (max-width: 650px) {
            .launcher-card { padding: 1.5rem 1rem; }
            .game-btn { min-width: 140px; padding: 0.8rem 1rem; font-size: 0.95rem; }
        }
        @media (max-width: 420px) {
            .button-grid { gap: 0.7rem; }
            .game-btn { min-width: 100%; }
        }
    </style>
</head>
<body>
    <div class="launcher-card">
        <!-- language switcher -->
        <div class="lang-switcher">
            <button class="lang-btn active" data-lang="en">EN</button>
            <button class="lang-btn" data-lang="ru">RU</button>
        </div>

        <!-- main title with data attributes for translation -->
        <h1 id="page-title" data-en="🚀 piggyuppy58 · games in browser" data-ru="🚀 piggyuppy58 · игры в браузере">🚀 piggyuppy58 · game hub</h1>
        <div class="sub" id="page-sub" data-en="click any button to launch the game (opens in new tab)" data-ru="нажми на кнопку, чтобы запустить игру (откроется в новой вкладке)">click any button to launch the game (opens in new tab)</div>

        <div class="button-grid">
            <!-- all game links with english (default) and russian button texts stored in data attributes -->
            <a href="https://piggyuppy58.github.io/Block%20Blast.html" class="game-btn" target="_blank" rel="noopener" data-en="📦 Block Blast" data-ru="📦 Блок Бласт">📦 Block Blast</a>

            <a href="https://piggyuppy58.github.io/Color%20Water%20Sort%203D.html" class="game-btn" target="_blank" rel="noopener" data-en="💧 Color Water Sort 3D" data-ru="💧 Сортировка цветной воды 3D">💧 Color Water Sort 3D</a>

            <a href="https://piggyuppy58.github.io/Five%20Nights%20at%20Epstein's.html" class="game-btn" target="_blank" rel="noopener" data-en="🌙 Five Nights at Epstein's" data-ru="🌙 Пять ночей у Эпштейна">🌙 Five Nights at Epstein's</a>

            <a href="https://piggyuppy58.github.io/Five%20Nights%20at%20Freddy's%202.html" class="game-btn" target="_blank" rel="noopener" data-en="🐻 FNaF 2" data-ru="🐻 ФНАФ 2">🐻 FNaF 2</a>

            <a href="https://piggyuppy58.github.io/Five%20Nights%20at%20Freddy's%203.html" class="game-btn" target="_blank" rel="noopener" data-en="🐰 FNaF 3" data-ru="🐰 ФНАФ 3">🐰 FNaF 3</a>

            <a href="https://piggyuppy58.github.io/Five%20Nights%20at%20Freddy's%204.html" class="game-btn" target="_blank" rel="noopener" data-en="👻 FNaF 4" data-ru="👻 ФНАФ 4">👻 FNaF 4</a>

            <a href="https://piggyuppy58.github.io/Five%20Nights%20at%20Freddy's.html" class="game-btn" target="_blank" rel="noopener" data-en="🎪 Five Nights at Freddy's" data-ru="🎪 Пять ночей с Фредди">🎪 Five Nights at Freddy's</a>

            <a href="https://piggyuppy58.github.io/Geometry%20Dash%20Lite%20(REMAKE).html" class="game-btn" target="_blank" rel="noopener" data-en="🔷 Geometry Dash Lite (REMAKE)" data-ru="🔷 Геометри Деш Лайт (РЕМЕЙК)">🔷 Geometry Dash Lite (REMAKE)</a>

            <a href="https://piggyuppy58.github.io/Google%20Feud.html" class="game-btn" target="_blank" rel="noopener" data-en="🔎 Google Feud" data-ru="🔎 Гугл Фьюд">🔎 Google Feud</a>

            <a href="https://piggyuppy58.github.io/Minecraft%201.12.2.html" class="game-btn" target="_blank" rel="noopener" data-en="⛏️ Minecraft 1.12.2" data-ru="⛏️ Майнкрафт 1.12.2">⛏️ Minecraft 1.12.2</a>

            <a href="https://piggyuppy58.github.io/Minecraft%201.21.4.html" class="game-btn" target="_blank" rel="noopener" data-en="🪓 Minecraft 1.21.4" data-ru="🪓 Майнкрафт 1.21.4">🪓 Minecraft 1.21.4</a>

            <a href="https://piggyuppy58.github.io/Minecraft%20Indev.html" class="game-btn" target="_blank" rel="noopener" data-en="🗺️ Minecraft Indev" data-ru="🗺️ Майнкрафт Indev">🗺️ Minecraft Indev</a>

            <a href="https://piggyuppy58.github.io/R.E.P.O.html" class="game-btn" target="_blank" rel="noopener" data-en="⚙️ R.E.P.O" data-ru="⚙️ Р.Е.П.О">⚙️ R.E.P.O</a>

            <a href="https://piggyuppy58.github.io/Terraria.html" class="game-btn" target="_blank" rel="noopener" data-en="🌳 Terraria" data-ru="🌳 Террария">🌳 Terraria</a>
        </div>

        <footer>
            <span class="note" id="footer-note" data-en="🎯 buttons open directly — all games hosted on piggyuppy58.github.io" data-ru="🎯 кнопки открывают игры напрямую — все игры сделаны piggyuppy58">🎯 buttons open directly — all games hosted by piggyuppy58</span>
        </footer>
    </div>

    <script>
        (function() {
            // language switcher functionality
            const langButtons = document.querySelectorAll('.lang-btn');
            const translatableElements = document.querySelectorAll('[data-en][data-ru]'); // all elements that have both language attributes

            // Function to set language
            function setLanguage(lang) {
                // update html lang attribute
                document.documentElement.lang = lang;

                // update all elements with data-en and data-ru
                translatableElements.forEach(el => {
                    const enText = el.getAttribute('data-en');
                    const ruText = el.getAttribute('data-ru');
                    if (lang === 'ru' && ruText) {
                        el.textContent = ruText;
                    } else if (lang === 'en' && enText) {
                        el.textContent = enText;
                    }
                });

                // update active class on switcher buttons
                langButtons.forEach(btn => {
                    const btnLang = btn.getAttribute('data-lang');
                    if (btnLang === lang) {
                        btn.classList.add('active');
                    } else {
                        btn.classList.remove('active');
                    }
                });
            }

            // add click listeners
            langButtons.forEach(btn => {
                btn.addEventListener('click', function(e) {
                    const lang = this.getAttribute('data-lang');
                    setLanguage(lang);
                    // optional: save to localStorage
                    // localStorage.setItem('preferred-lang', lang);
                });
            });

            // initial language from default (EN is active in html, but we ensure consistency)
            // You could also read from localStorage, but we start with EN (active class already on EN)
            // Ensure that displayed text matches the active language (in case of mismatch)
            // The default active is EN, so we set language to EN explicitly to sync
            setLanguage('en');
        })();
    </script>
</body>
</html>
