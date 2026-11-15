<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pathball Arena – Paper Soccer</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background: radial-gradient(circle at 50% 0%, #1e293b 0%, #090d16 75%);
            color: #f8fafc;
            user-select: none;
        }
        canvas {
            display: block;
            width: 100%;
            height: 100%;
            cursor: pointer;
            touch-action: none;
        }
        .glass-panel {
            background: rgba(15, 23, 42, 0.76);
            backdrop-filter: blur(18px);
            -webkit-backdrop-filter: blur(18px);
            border: 1px solid rgba(255, 255, 255, 0.08);
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.65);
        }
    </style>
</head>
<body class="min-h-screen flex flex-col items-center justify-center p-4 lg:p-8">

    <!-- PRZEŁĄCZNIK JĘZYKA (PL / EN) W PRAWYM GÓRNYM ROGU -->
    <div class="fixed top-4 right-4 z-50 flex items-center gap-1 bg-slate-900/90 backdrop-blur-md p-1 rounded-xl border border-slate-700/80 shadow-xl">
        <button type="button" data-lang="pl" class="lang-btn px-3 py-1.5 rounded-lg text-xs font-extrabold bg-emerald-500 text-slate-950 cursor-pointer transition">
            🇵🇱 PL
        </button>
        <button type="button" data-lang="en" class="lang-btn px-3 py-1.5 rounded-lg text-xs font-extrabold text-slate-300 hover:text-white cursor-pointer transition">
            🇬🇧 EN
        </button>
    </div>

    <!-- EKRAN STARTOWY: Wybór stylu gry -->
    <div id="startScreen" class="w-full max-w-lg glass-panel p-7 sm:p-9 rounded-3xl relative overflow-hidden">
        <div class="absolute -top-20 -right-20 w-52 h-52 bg-emerald-500/20 rounded-full blur-3xl pointer-events-none"></div>
        <div class="absolute -bottom-20 -left-20 w-52 h-52 bg-blue-500/20 rounded-full blur-3xl pointer-events-none"></div>

        <div class="relative">
            <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-emerald-500/10 border border-emerald-500/30 text-emerald-400 text-[11px] font-bold uppercase tracking-wider mb-3">
                <span class="w-2 h-2 rounded-full bg-emerald-400 animate-ping"></span>
                <span data-i18n="badge">Edycja Turniejowa • Do 3 Goli</span>
            </div>
            <h1 class="text-3xl sm:text-4xl font-extrabold text-white tracking-tight">Pathball Arena</h1>
            <p data-i18n="subtitle" class="text-xs sm:text-sm text-slate-400 mt-1.5 mb-7 leading-relaxed">
                Klasyczne piłkarzyki na kartce w nowoczesnym wydaniu. Odbijaj się od band i istniejących linii, aby budować zabójcze akcje.
            </p>

            <div class="space-y-6">
                <!-- 1. Tryb gry -->
                <div>
                    <label data-i18n="selectModeLabel" class="block text-[11px] font-extrabold text-slate-400 uppercase tracking-widest mb-2.5">
                        Wybierz tryb meczu
                    </label>
                    <div class="grid grid-cols-2 gap-3">
                        <button type="button" data-mode="pve" class="mode-option p-4 rounded-2xl border-2 border-emerald-500 bg-emerald-500/15 text-left cursor-pointer transition-all duration-200 shadow-lg shadow-emerald-950/30">
                            <div class="text-base font-extrabold text-white" data-i18n="modePveTitle">🤖 vs Bot AI</div>
                            <div class="text-[11px] text-slate-300 mt-1 leading-snug" data-i18n="modePveDesc">Pojedynek ze sztuczną inteligencją</div>
                        </button>
                        <button type="button" data-mode="pvp" class="mode-option p-4 rounded-2xl border-2 border-slate-800 bg-slate-900/80 hover:border-slate-600 text-left cursor-pointer transition-all duration-200">
                            <div class="text-base font-extrabold text-white" data-i18n="modePvpTitle">⚔️ 2 Graczy</div>
                            <div class="text-[11px] text-slate-400 mt-1 leading-snug" data-i18n="modePvpDesc">Gra 1 na 1 na jednym urządzeniu</div>
                        </button>
                    </div>
                </div>

                <!-- 2. Poziom trudności Bota -->
                <div id="startBotSection" class="transition-opacity duration-200">
                    <label data-i18n="selectDiffLabel" class="block text-[11px] font-extrabold text-slate-400 uppercase tracking-widest mb-2.5">
                        Poziom trudności Bota
                    </label>
                    <div class="grid grid-cols-3 gap-2.5">
                        <button type="button" data-diff="1" class="diff-option py-3 px-2 rounded-xl border-2 border-slate-800 bg-slate-900/80 hover:border-slate-600 text-center cursor-pointer transition-all">
                            <div class="text-xs font-extrabold text-white" data-i18n="diffEasy">Prosty</div>
                            <div class="text-[10px] text-slate-400 mt-0.5" data-i18n="diffEasySub">Rekreacyjny</div>
                        </button>
                        <button type="button" data-diff="2" class="diff-option py-3 px-2 rounded-xl border-2 border-slate-800 bg-slate-900/80 hover:border-slate-600 text-center cursor-pointer transition-all">
                            <div class="text-xs font-extrabold text-white" data-i18n="diffMedium">Średni</div>
                            <div class="text-[10px] text-slate-400 mt-0.5" data-i18n="diffMediumSub">Taktyczny</div>
                        </button>
                        <button type="button" data-diff="3" class="diff-option py-3 px-2 rounded-xl border-2 border-emerald-500 bg-emerald-500/15 text-center cursor-pointer transition-all shadow-md">
                            <div class="text-xs font-extrabold text-white" data-i18n="diffExpert">Ekspert</div>
                            <div class="text-[10px] text-emerald-300 mt-0.5" data-i18n="diffExpertSub">Bezlitosny</div>
                        </button>
                    </div>
                </div>

                <button id="startGameBtn" data-i18n="startBtn" class="w-full py-4 rounded-2xl bg-gradient-to-r from-emerald-500 to-teal-500 hover:from-emerald-400 hover:to-teal-400 text-slate-950 font-extrabold text-sm uppercase tracking-wider shadow-xl shadow-emerald-950/50 cursor-pointer transition-all transform active:scale-[0.99] mt-2">
                    Wejdź na boisko →
                </button>
            </div>
        </div>
    </div>

    <!-- EKRAN GRY (DESKTOP VIEW: Układ 2-kolumnowy na dużych ekranach) -->
    <div id="gameContainer" class="hidden w-full max-w-5xl grid grid-cols-1 lg:grid-cols-12 gap-6 items-center">
        
        <!-- LEWA KOLUMNA (7/12 na Desktop): Duża plansza boiska -->
        <div class="lg:col-span-7 flex flex-col items-center justify-center glass-panel p-4 sm:p-6 rounded-3xl">
            <div id="boardWrapper" class="w-full max-w-[460px] aspect-[8/10] bg-[#f8fafc] rounded-2xl overflow-hidden shadow-[0_0_50px_rgba(0,0,0,0.55)] border-[6px] border-slate-800 relative">
                <canvas id="pathballCanvas"></canvas>

                <!-- Nakładka końca rundy / meczu -->
                <div id="roundOverlay" class="hidden absolute inset-0 bg-slate-950/88 backdrop-blur-md flex flex-col items-center justify-center p-6 text-center z-10">
                    <span id="matchBadge" class="hidden px-3.5 py-1 mb-3 rounded-full text-[11px] font-black uppercase tracking-widest bg-gradient-to-r from-amber-400 to-orange-500 text-slate-950 shadow-lg">
                        🏆 Koniec Meczu (3 pkt)
                    </span>
                    <h2 id="roundTitle" class="text-3xl font-black text-white mb-2 tracking-tight">GOOOL!</h2>
                    <p id="roundDesc" class="text-sm text-slate-300 mb-6 max-w-xs leading-relaxed">Punkt zdobyty!</p>
                    <div class="flex flex-wrap items-center justify-center gap-3">
                        <button id="nextRoundBtn" class="px-6 py-3 rounded-xl bg-emerald-500 hover:bg-emerald-400 text-slate-950 font-extrabold text-sm shadow-lg shadow-emerald-950/50 cursor-pointer transition">
                            Następna runda
                        </button>
                        <button id="overlayMenuBtn" data-i18n="changeModeBtn" class="px-4 py-3 rounded-xl bg-slate-800 hover:bg-slate-700 border border-slate-700 text-slate-200 font-bold text-sm cursor-pointer transition">
                            Zmień tryb
                        </button>
                    </div>
                </div>
            </div>
        </div>

        <!-- PRAWA KOLUMNA (5/12 na Desktop): Panel sterowania, wyniki i zasady -->
        <aside class="lg:col-span-5 flex flex-col gap-4">
            
            <!-- Karta wyniku meczu -->
            <div class="glass-panel p-5 sm:p-6 rounded-3xl">
                <div class="flex items-center justify-between mb-4">
                    <span class="text-xs font-extrabold text-slate-400 uppercase tracking-widest" data-i18n="scoreboardTitle">Tablica Wyników</span>
                    <span class="px-2.5 py-0.5 rounded-full bg-slate-800 border border-slate-700 text-[11px] font-bold text-emerald-400" data-i18n="firstToThree">Do 3 goli</span>
                </div>

                <div class="grid grid-cols-3 items-center bg-slate-950/80 p-4 rounded-2xl border border-slate-800/90">
                    <!-- Gracz 1 -->
                    <div class="flex flex-col items-center text-center">
                        <div class="w-11 h-11 rounded-2xl bg-gradient-to-br from-blue-500 to-blue-700 flex items-center justify-center font-black text-white shadow-lg shadow-blue-950/50 mb-1.5">
                            P1
                        </div>
                        <div id="p1Label" class="text-xs font-extrabold text-blue-400 uppercase">TY</div>
                        <div data-i18n="attacksDown" class="text-[10px] text-slate-500 mt-0.5">Atakuje dół ↓</div>
                    </div>

                    <!-- Licznik -->
                    <div class="flex items-center justify-center gap-2.5">
                        <span id="scoreP1" class="text-4xl font-black text-blue-400">0</span>
                        <span class="text-slate-600 font-black text-2xl">:</span>
                        <span id="scoreP2" class="text-4xl font-black text-rose-400">0</span>
                    </div>

                    <!-- Gracz 2 / Bot -->
                    <div class="flex flex-col items-center text-center">
                        <div class="w-11 h-11 rounded-2xl bg-gradient-to-br from-rose-500 to-red-700 flex items-center justify-center font-black text-white shadow-lg shadow-rose-950/50 mb-1.5">
                            P2
                        </div>
                        <div id="p2Label" class="text-xs font-extrabold text-rose-400 uppercase">BOT AI</div>
                        <div data-i18n="attacksUp" class="text-[10px] text-slate-500 mt-0.5">Atakuje górę ↑</div>
                    </div>
                </div>

                <!-- Status aktywnej tury -->
                <div class="mt-4 flex flex-col gap-2">
                    <div id="turnIndicator" class="w-full py-2.5 px-4 rounded-xl text-xs font-extrabold text-center bg-blue-600 text-white shadow-md">
                        Tura: TWÓJ RUCH
                    </div>
                    <div id="comboIndicator" class="w-full py-2 px-3 rounded-xl text-xs font-extrabold text-center bg-amber-500/20 border border-amber-500/40 text-amber-300 hidden">
                        ⚡ Odbicie! Dodatkowy ruch w tej turze
                    </div>
                </div>
            </div>

            <!-- Karta legendy i zasad (widoczna szczególnie dobrze na Desktopie) -->
            <div class="glass-panel p-5 rounded-3xl space-y-3">
                <div class="text-xs font-extrabold text-slate-400 uppercase tracking-widest" data-i18n="legendTitle">Oznaczenia na boisku</div>
                
                <div class="flex items-center gap-3 bg-slate-900/60 p-3 rounded-xl border border-slate-800/80">
                    <span class="w-3.5 h-3.5 rounded-full bg-emerald-500/40 border-2 border-emerald-500 shrink-0"></span>
                    <div>
                        <div class="text-xs font-bold text-white" data-i18n="legendMoveTitle">Wolna kropka (Ruch)</div>
                        <div class="text-[11px] text-slate-400" data-i18n="legendMoveDesc">Kończy Twoją turę po przesunięciu piłki.</div>
                    </div>
                </div>

                <div class="flex items-center gap-3 bg-slate-900/60 p-3 rounded-xl border border-slate-800/80">
                    <span class="w-3.5 h-3.5 rounded-full bg-amber-500/40 border-2 border-amber-500 shrink-0"></span>
                    <div>
                        <div class="text-xs font-bold text-amber-300" data-i18n="legendBounceTitle">Odbicie (+1 Ruch gratis)</div>
                        <div class="text-[11px] text-slate-400" data-i18n="legendBounceDesc">Wejście na bandę lub odwiedzony punkt daje kolejny ruch!</div>
                    </div>
                </div>
            </div>

            <!-- Przyciski nawigacji -->
            <div class="grid grid-cols-2 gap-3">
                <button id="resetMatchBtn" data-i18n="restartBtn" class="py-3.5 px-4 rounded-2xl glass-panel hover:bg-slate-800/90 text-slate-200 font-extrabold text-xs uppercase tracking-wider cursor-pointer transition text-center">
                    ↺ Od nowa
                </button>
                <button id="backToMenuBtn" data-i18n="menuBtn" class="py-3.5 px-4 rounded-2xl glass-panel hover:bg-slate-800/90 text-emerald-400 font-extrabold text-xs uppercase tracking-wider cursor-pointer transition text-center">
                    ☰ Menu główne
                </button>
            </div>

        </aside>
    </div>

    <script>
        window.onload = function () {
            const canvas = document.getElementById('pathballCanvas');
            const ctx = canvas.getContext('2d');
            const wrapper = document.getElementById('boardWrapper');

            const COLS = 8;
            const ROWS = 10;
            const WIN_SCORE = 3;

            // === SŁOWNIK TŁUMACZEŃ (PL / EN) ===
            const translations = {
                pl: {
                    badge: 'Edycja Turniejowa • Do 3 Goli',
                    subtitle: 'Klasyczne piłkarzyki na kartce w nowoczesnym wydaniu. Odbijaj się od band i istniejących linii, aby budować zabójcze akcje.',
                    selectModeLabel: 'Wybierz tryb meczu',
                    modePveTitle: '🤖 vs Bot AI',
                    modePveDesc: 'Pojedynek ze sztuczną inteligencją',
                    modePvpTitle: '⚔️ 2 Graczy',
                    modePvpDesc: 'Gra 1 na 1 na jednym urządzeniu',
                    selectDiffLabel: 'Poziom trudności Bota',
                    diffEasy: 'Prosty',
                    diffEasySub: 'Rekreacyjny',
                    diffMedium: 'Średni',
                    diffMediumSub: 'Taktyczny',
                    diffExpert: 'Ekspert',
                    diffExpertSub: 'Bezlitosny',
                    startBtn: 'Wejdź na boisko →',
                    scoreboardTitle: 'Tablica Wyników',
                    firstToThree: 'Do 3 goli',
                    attacksDown: 'Atakuje dół ↓',
                    attacksUp: 'Atakuje górę ↑',
                    legendTitle: 'Oznaczenia na boisku',
                    legendMoveTitle: 'Wolna kropka (Ruch)',
                    legendMoveDesc: 'Kończy Twoją turę po przesunięciu piłki.',
                    legendBounceTitle: 'Odbicie (+1 Ruch gratis)',
                    legendBounceDesc: 'Wejście na bandę lub odwiedzony punkt daje kolejny ruch!',
                    restartBtn: '↺ Od nowa',
                    menuBtn: '☰ Menu główne',
                    changeModeBtn: 'Zmień tryb',
                    comboAlert: '⚡ Odbicie! Dodatkowy ruch w tej turze',
                    p1Short: 'TY',
                    p1Pvp: 'GRACZ 1',
                    p2Pvp: 'GRACZ 2',
                    turnHuman: 'Tura: TWÓJ RUCH',
                    turnP1: 'Tura: GRACZ 1 (Niebieski)',
                    turnP2: 'Tura: GRACZ 2 (Czerwony)',
                    turnBot: 'Tura: BOT AI MYŚLI...',
                    matchEndBadge: '🏆 Koniec Meczu (3 pkt)',
                    nextRound: 'Następna runda',
                    playRematch: 'Zagraj rewanż',
                    goalP1Title: 'GOOOL DLA CIEBIE!',
                    goalP1PvpTitle: 'GOL DLA GRACZA 1!',
                    goalP2Title: 'GOL DLA BOTA AI!',
                    goalP2PvpTitle: 'GOL DLA GRACZA 2!',
                    winMatchHuman: 'ZWYCIĘSTWO W MECZU!',
                    winMatchP1: 'GRACZ 1 WYGRYWA MECZ!',
                    winMatchBot: 'BOT AI WYGRYWA MECZ!',
                    winMatchP2: 'GRACZ 2 WYGRYWA MECZ!',
                    goalP1Desc: 'Piękny strzał! Zdobywasz bramkę!',
                    goalP1PvpDesc: 'Gracz 1 umieszcza piłkę w siatce!',
                    goalP2Desc: 'Bot AI przełamał obronę i zdobył gola.',
                    goalP2PvpDesc: 'Gracz 2 umieszcza piłkę w siatce!',
                    trapP1Desc: 'Zaklinowałeś się! Brak wolnych ścieżek – punkt dla Bota.',
                    trapP1PvpDesc: 'Gracz 1 zaklinowany bez wyjścia! Punkt dla Gracza 2.',
                    trapP2Desc: 'Znakomicie! Zaklinowałeś Bota AI – punkt dla Ciebie!',
                    trapP2PvpDesc: 'Gracz 2 zaklinowany bez wyjścia! Punkt dla Gracza 1.',
                    finalScorePrefix: 'Wynik końcowy'
                },
                en: {
                    badge: 'Tournament Edition • First to 3 Goals',
                    subtitle: 'Classic paper soccer reimagined. Bounce off the walls and visited intersections to chain unstoppable multi-move combos.',
                    selectModeLabel: 'Select Match Mode',
                    modePveTitle: '🤖 vs AI Bot',
                    modePveDesc: 'Challenge the artificial intelligence',
                    modePvpTitle: '⚔️ 2 Players',
                    modePvpDesc: 'Local 1v1 match on one screen',
                    selectDiffLabel: 'AI Bot Difficulty',
                    diffEasy: 'Easy',
                    diffEasySub: 'Casual',
                    diffMedium: 'Medium',
                    diffMediumSub: 'Tactical',
                    diffExpert: 'Expert',
                    diffExpertSub: 'Ruthless',
                    startBtn: 'Enter Pitch →',
                    scoreboardTitle: 'Scoreboard',
                    firstToThree: 'First to 3',
                    attacksDown: 'Attacks down ↓',
                    attacksUp: 'Attacks up ↑',
                    legendTitle: 'Pitch Indicators',
                    legendMoveTitle: 'Open Dot (Standard Move)',
                    legendMoveDesc: 'Ends your turn after moving the ball.',
                    legendBounceTitle: 'Bounce (+1 Free Move)',
                    legendBounceDesc: 'Hitting a wall or visited dot grants an extra move!',
                    restartBtn: '↺ Restart',
                    menuBtn: '☰ Main Menu',
                    changeModeBtn: 'Change Mode',
                    comboAlert: '⚡ Bounce! Extra move in this turn',
                    p1Short: 'YOU',
                    p1Pvp: 'PLAYER 1',
                    p2Pvp: 'PLAYER 2',
                    turnHuman: 'Turn: YOUR MOVE',
                    turnP1: 'Turn: PLAYER 1 (Blue)',
                    turnP2: 'Turn: PLAYER 2 (Red)',
                    turnBot: 'Turn: AI BOT THINKING...',
                    matchEndBadge: '🏆 Match Over (3 pts)',
                    nextRound: 'Next Round',
                    playRematch: 'Play Rematch',
                    goalP1Title: 'GOAL FOR YOU!',
                    goalP1PvpTitle: 'GOAL FOR PLAYER 1!',
                    goalP2Title: 'AI BOT SCORES!',
                    goalP2PvpTitle: 'GOAL FOR PLAYER 2!',
                    winMatchHuman: 'MATCH VICTORY!',
                    winMatchP1: 'PLAYER 1 WINS THE MATCH!',
                    winMatchBot: 'AI BOT WINS THE MATCH!',
                    winMatchP2: 'PLAYER 2 WINS THE MATCH!',
                    goalP1Desc: 'Great strike! You found the back of the net!',
                    goalP1PvpDesc: 'Player 1 puts the ball into the net!',
                    goalP2Desc: 'The AI Bot broke through and scored.',
                    goalP2PvpDesc: 'Player 2 puts the ball into the net!',
                    trapP1Desc: 'You got trapped! No moves left – point for AI Bot.',
                    trapP1PvpDesc: 'Player 1 is trapped! Point for Player 2.',
                    trapP2Desc: 'Brilliant! You trapped the AI Bot – point for you!',
                    trapP2PvpDesc: 'Player 2 is trapped! Point for Player 1.',
                    finalScorePrefix: 'Final score'
                }
            };

            const state = {
                lang: 'pl',
                ball: { x: 4, y: 5 },
                edges: new Set(),
                edgeColors: new Map(),
                visited: new Set(),
                turn: 'p1',
                scores: { p1: 0, p2: 0 },
                mode: 'pve',            // 'pve' | 'pvp'
                difficulty: 3,          // 1 | 2 | 3
                roundOver: false,
                matchOver: false,
                botThinking: false,
                hoverNode: null,
                lastEndReason: null     // { winner, type: 'goal'|'trap', actor }
            };

            function t(key) {
                return translations[state.lang][key] || key;
            }

            function applyTranslations() {
                document.documentElement.lang = state.lang;
                document.querySelectorAll('[data-i18n]').forEach(el => {
                    const key = el.getAttribute('data-i18n');
                    if (translations[state.lang][key]) {
                        el.textContent = translations[state.lang][key];
                    }
                });
                document.getElementById('comboIndicator').textContent = t('comboAlert');
                updateUI();
                if (state.roundOver && state.lastEndReason) {
                    renderRoundOverlay();
                }
            }

            // Obsługa przycisków języka PL / EN
            const langButtons = document.querySelectorAll('.lang-btn');
            langButtons.forEach(btn => {
                btn.addEventListener('click', () => {
                    state.lang = btn.dataset.lang;
                    langButtons.forEach(b => {
                        b.classList.remove('bg-emerald-500', 'text-slate-950');
                        b.classList.add('text-slate-300');
                    });
                    btn.classList.add('bg-emerald-500', 'text-slate-950');
                    btn.classList.remove('text-slate-300');
                    applyTranslations();
                });
            });

            // === EKRAN STARTOWY ===
            const modeButtons = document.querySelectorAll('.mode-option');
            const diffButtons = document.querySelectorAll('.diff-option');
            const startBotSection = document.getElementById('startBotSection');

            function highlightSelected(buttons, activeBtn) {
                buttons.forEach(btn => {
                    btn.classList.remove('border-emerald-500', 'bg-emerald-500/15', 'shadow-lg');
                    btn.classList.add('border-slate-800', 'bg-slate-900/80');
                });
                activeBtn.classList.remove('border-slate-800', 'bg-slate-900/80');
                activeBtn.classList.add('border-emerald-500', 'bg-emerald-500/15', 'shadow-lg');
            }

            modeButtons.forEach(btn => {
                btn.addEventListener('click', () => {
                    state.mode = btn.dataset.mode;
                    highlightSelected(modeButtons, btn);
                    if (state.mode === 'pvp') {
                        startBotSection.classList.add('opacity-35', 'pointer-events-none');
                    } else {
                        startBotSection.classList.remove('opacity-35', 'pointer-events-none');
                    }
                });
            });

            diffButtons.forEach(btn => {
                btn.addEventListener('click', () => {
                    state.difficulty = parseInt(btn.dataset.diff, 10);
                    highlightSelected(diffButtons, btn);
                });
            });

            document.getElementById('startGameBtn').addEventListener('click', () => {
                document.getElementById('startScreen').classList.add('hidden');
                document.getElementById('gameContainer').classList.remove('hidden');
                resizeCanvas();
                initRound(true);
            });

            function openStartMenu() {
                document.getElementById('gameContainer').classList.add('hidden');
                document.getElementById('roundOverlay').classList.add('hidden');
                document.getElementById('startScreen').classList.remove('hidden');
            }

            document.getElementById('backToMenuBtn').addEventListener('click', openStartMenu);
            document.getElementById('overlayMenuBtn').addEventListener('click', openStartMenu);
            document.getElementById('resetMatchBtn').addEventListener('click', () => initRound(true));

            // === LOGIKA GRY PATHBALL ===
            function nodeKey(x, y) {
                return `${x},${y}`;
            }

            function edgeKey(x1, y1, x2, y2) {
                if (x1 < x2 || (x1 === x2 && y1 < y2)) {
                    return `${x1},${y1}-${x2},${y2}`;
                }
                return `${x2},${y2}-${x1},${y1}`;
            }

            function isValidNode(x, y) {
                if (y === -1 && (x >= 3 && x <= 5)) return true;
                if (y === ROWS + 1 && (x >= 3 && x <= 5)) return true;
                return x >= 0 && x <= COLS && y >= 0 && y <= ROWS;
            }

            function isBoundaryEdge(x1, y1, x2, y2) {
                if (x1 === 0 && x2 === 0) return true;
                if (x1 === COLS && x2 === COLS) return true;
                if (y1 === 0 && y2 === 0 && !(Math.min(x1, x2) >= 3 && Math.max(x1, x2) <= 5)) return true;
                if (y1 === ROWS && y2 === ROWS && !(Math.min(x1, x2) >= 3 && Math.max(x1, x2) <= 5)) return true;
                if ((y1 === -1 || y2 === -1) && ((x1 === 3 && x2 === 3) || (x1 === 5 && x2 === 5))) return true;
                if ((y1 === ROWS + 1 || y2 === ROWS + 1) && ((x1 === 3 && x2 === 3) || (x1 === 5 && x2 === 5))) return true;
                return false;
            }

            function isBoundaryNode(x, y) {
                if (x === 0 || x === COLS) return true;
                if ((y === 0 || y === ROWS) && (x <= 3 || x >= 5)) return true;
                return false;
            }

            function getValidMoves(bx, by, edgesSet) {
                const moves = [];
                for (let dx = -1; dx <= 1; dx++) {
                    for (let dy = -1; dy <= 1; dy++) {
                        if (dx === 0 && dy === 0) continue;
                        const nx = bx + dx;
                        const ny = by + dy;
                        if (!isValidNode(nx, ny)) continue;

                        if ((by === 0 && ny === -1 && ((bx <= 2 && nx === 3) || (bx >= 6 && nx === 5))) ||
                            (by === ROWS && ny === ROWS + 1 && ((bx <= 2 && nx === 3) || (bx >= 6 && nx === 5)))) {
                            continue;
                        }

                        const eKey = edgeKey(bx, by, nx, ny);
                        if (edgesSet.has(eKey)) continue;
                        if (isBoundaryEdge(bx, by, nx, ny)) continue;

                        moves.push({ x: nx, y: ny, eKey });
                    }
                }
                return moves;
            }

            function initRound(resetMatch = false) {
                if (resetMatch) {
                    state.scores = { p1: 0, p2: 0 };
                    state.matchOver = false;
                    document.getElementById('scoreP1').textContent = '0';
                    document.getElementById('scoreP2').textContent = '0';
                }

                state.ball = { x: 4, y: 5 };
                state.edges.clear();
                state.edgeColors.clear();
                state.visited.clear();
                state.visited.add(nodeKey(4, 5));
                state.turn = 'p1';
                state.roundOver = false;
                state.botThinking = false;
                state.lastEndReason = null;

                document.getElementById('roundOverlay').classList.add('hidden');
                document.getElementById('matchBadge').classList.add('hidden');
                document.getElementById('comboIndicator').classList.add('hidden');
                updateUI();
                drawBoard();
            }

            function updateUI() {
                const ind = document.getElementById('turnIndicator');
                const diffKeys = { 1: 'diffEasy', 2: 'diffMedium', 3: 'diffExpert' };

                document.getElementById('p1Label').textContent = state.mode === 'pvp' ? t('p1Pvp') : t('p1Short');
                document.getElementById('p2Label').textContent = state.mode === 'pvp' ? t('p2Pvp') : `BOT (${t(diffKeys[state.difficulty])})`;

                if (state.turn === 'p1') {
                    ind.textContent = state.mode === 'pvp' ? t('turnP1') : t('turnHuman');
                    ind.className = 'w-full py-2.5 px-4 rounded-xl text-xs font-extrabold text-center bg-blue-600 text-white shadow-md shadow-blue-950/50';
                } else {
                    ind.textContent = state.mode === 'pvp' ? t('turnP2') : t('turnBot');
                    ind.className = `w-full py-2.5 px-4 rounded-xl text-xs font-extrabold text-center bg-rose-600 text-white shadow-md shadow-rose-950/50 ${state.mode === 'pve' ? 'animate-pulse' : ''}`;
                }
            }

            function makeStep(nx, ny, actor) {
                if (state.roundOver || state.matchOver) return false;
                const moves = getValidMoves(state.ball.x, state.ball.y, state.edges);
                const chosen = moves.find(m => m.x === nx && m.y === ny);
                if (!chosen) return false;

                const wasVisited = state.visited.has(nodeKey(nx, ny)) || isBoundaryNode(nx, ny);

                state.edges.add(chosen.eKey);
                state.edgeColors.set(chosen.eKey, actor);
                state.visited.add(nodeKey(nx, ny));
                state.ball = { x: nx, y: ny };

                if (ny === ROWS + 1) {
                    finishRound('p1', 'goal', actor);
                    return true;
                }
                if (ny === -1) {
                    finishRound('p2', 'goal', actor);
                    return true;
                }

                const nextMoves = getValidMoves(nx, ny, state.edges);
                if (nextMoves.length === 0) {
                    const winner = actor === 'p1' ? 'p2' : 'p1';
                    finishRound(winner, 'trap', actor);
                    return true;
                }

                const comboEl = document.getElementById('comboIndicator');
                if (wasVisited) {
                    comboEl.classList.remove('hidden');
                    drawBoard();
                    return 'bounce';
                } else {
                    comboEl.classList.add('hidden');
                    state.turn = actor === 'p1' ? 'p2' : 'p1';
                    updateUI();
                    drawBoard();

                    if (state.mode === 'pve' && state.turn === 'p2') {
                        triggerBotTurn();
                    }
                    return 'end_turn';
                }
            }

            function renderRoundOverlay() {
                const { winner, type, actor } = state.lastEndReason;
                const overlay = document.getElementById('roundOverlay');
                const title = document.getElementById('roundTitle');
                const desc = document.getElementById('roundDesc');
                const btn = document.getElementById('nextRoundBtn');
                const badge = document.getElementById('matchBadge');

                let message = '';
                if (type === 'goal') {
                    if (winner === 'p1') {
                        message = state.mode === 'pvp' ? t('goalP1PvpDesc') : t('goalP1Desc');
                    } else {
                        message = state.mode === 'pvp' ? t('goalP2PvpDesc') : t('goalP2Desc');
                    }
                } else {
                    if (actor === 'p1') {
                        message = state.mode === 'pvp' ? t('trapP1PvpDesc') : t('trapP1Desc');
                    } else {
                        message = state.mode === 'pvp' ? t('trapP2PvpDesc') : t('trapP2Desc');
                    }
                }

                if (state.matchOver) {
                    badge.textContent = t('matchEndBadge');
                    badge.classList.remove('hidden');
                    if (winner === 'p1') {
                        title.textContent = state.mode === 'pvp' ? t('winMatchP1') : t('winMatchHuman');
                        title.className = 'text-2xl sm:text-3xl font-black text-blue-400 mb-2';
                    } else {
                        title.textContent = state.mode === 'pvp' ? t('winMatchP2') : t('winMatchBot');
                        title.className = 'text-2xl sm:text-3xl font-black text-rose-400 mb-2';
                    }
                    desc.textContent = `${t('finalScorePrefix')} ${state.scores.p1} : ${state.scores.p2}. ${message}`;
                    btn.textContent = t('playRematch');
                } else {
                    badge.classList.add('hidden');
                    title.textContent = winner === 'p1'
                        ? (state.mode === 'pvp' ? t('goalP1PvpTitle') : t('goalP1Title'))
                        : (state.mode === 'pvp' ? t('goalP2PvpTitle') : t('goalP2Title'));
                    title.className = winner === 'p1'
                        ? 'text-2xl sm:text-3xl font-black text-blue-400 mb-2'
                        : 'text-2xl sm:text-3xl font-black text-rose-400 mb-2';
                    desc.textContent = message;
                    btn.textContent = t('nextRound');
                }

                overlay.classList.remove('hidden');
            }

            function finishRound(winner, type, actor) {
                state.roundOver = true;
                state.scores[winner]++;
                document.getElementById('scoreP1').textContent = state.scores.p1;
                document.getElementById('scoreP2').textContent = state.scores.p2;

                state.matchOver = state.scores[winner] >= WIN_SCORE;
                state.lastEndReason = { winner, type, actor };

                renderRoundOverlay();
                drawBoard();
            }

            // === SILNIK AI ===
            function findBestTurnSequence(forActor) {
                const difficulty = state.difficulty;
                const maxNodesExplored = difficulty === 1 ? 80 : (difficulty === 2 ? 450 : 2000);
                let exploredCount = 0;

                function generateTurnSequences(startX, startY, startEdges, startVisited, actor, limit) {
                    const results = [];
                    const targetGoalY = actor === 'p2' ? -1 : ROWS + 1;

                    function dfs(bx, by, edgesSet, visitedSet, seq) {
                        if (results.length >= limit || exploredCount++ > maxNodesExplored) return;

                        const moves = getValidMoves(bx, by, edgesSet);
                        moves.sort((a, b) => Math.abs(targetGoalY - a.y) - Math.abs(targetGoalY - b.y));

                        for (const m of moves) {
                            const newEdges = new Set(edgesSet);
                            newEdges.add(m.eKey);

                            const willBounce = visitedSet.has(nodeKey(m.x, m.y)) || isBoundaryNode(m.x, m.y);
                            const newVisited = new Set(visitedSet);
                            newVisited.add(nodeKey(m.x, m.y));

                            const newSeq = [...seq, { x: m.x, y: m.y }];
                            const isGoal = (m.y === -1 || m.y === ROWS + 1);
                            const furtherMoves = getValidMoves(m.x, m.y, newEdges);

                            if (isGoal || furtherMoves.length === 0 || !willBounce || newSeq.length >= 14) {
                                results.push({
                                    sequence: newSeq,
                                    endPos: { x: m.x, y: m.y },
                                    edges: newEdges,
                                    visited: newVisited
                                });
                            } else {
                                dfs(m.x, m.y, newEdges, newVisited, newSeq);
                            }
                        }
                    }

                    dfs(startX, startY, startEdges, startVisited, []);
                    return results;
                }

                function scoreBoard(bx, by, edgesSet, actor, seqLen) {
                    const myGoal = actor === 'p2' ? -1 : ROWS + 1;
                    const oppGoal = actor === 'p2' ? ROWS + 1 : -1;

                    if (by === myGoal) return 10000 - seqLen;
                    if (by === oppGoal) return -10000 + seqLen;

                    const nextMoves = getValidMoves(bx, by, edgesSet);
                    if (nextMoves.length === 0) return -9000;

                    const distY = Math.abs(myGoal - by);
                    const centerBias = -Math.abs(4 - bx) * 1.5;
                    const mobilityBonus = nextMoves.length * 1.2;
                    return (12 - distY) * 15 + centerBias + mobilityBonus;
                }

                const myTurns = generateTurnSequences(state.ball.x, state.ball.y, state.edges, state.visited, forActor, 45);
                let bestSequence = myTurns[0]?.sequence || [];
                let bestScore = -Infinity;
                const opponent = forActor === 'p2' ? 'p1' : 'p2';

                for (const turn of myTurns) {
                    let score = scoreBoard(turn.endPos.x, turn.endPos.y, turn.edges, forActor, turn.sequence.length);

                    if (difficulty === 3 && Math.abs(score) < 8000) {
                        const oppTurns = generateTurnSequences(turn.endPos.x, turn.endPos.y, turn.edges, turn.visited, opponent, 16);
                        let worstReplyPenalty = 0;

                        for (const opp of oppTurns) {
                            const oppScore = scoreBoard(opp.endPos.x, opp.endPos.y, opp.edges, opponent, opp.sequence.length);
                            if (oppScore > 8000) {
                                worstReplyPenalty = -8500;
                                break;
                            }
                            worstReplyPenalty = Math.min(worstReplyPenalty, -oppScore * 0.45);
                        }
                        score += worstReplyPenalty;
                    }

                    if (score > bestScore) {
                        bestScore = score;
                        bestSequence = turn.sequence;
                    }
                }

                return bestSequence;
            }

            function triggerBotTurn() {
                if (state.botThinking || state.roundOver || state.matchOver) return;
                state.botThinking = true;

                setTimeout(() => {
                    const sequence = findBestTurnSequence('p2');
                    let stepIndex = 0;

                    function playNextBotStep() {
                        if (state.roundOver || state.matchOver || stepIndex >= sequence.length) {
                            state.botThinking = false;
                            return;
                        }
                        const step = sequence[stepIndex++];
                        const status = makeStep(step.x, step.y, 'p2');
                        if (status === 'bounce') {
                            setTimeout(playNextBotStep, 240);
                        } else {
                            state.botThinking = false;
                        }
                    }
                    playNextBotStep();
                }, 300);
            }

            document.getElementById('nextRoundBtn').addEventListener('click', () => {
                initRound(state.matchOver);
            });

            // === RYSOWANIE PLANSZY ===
            function getGeometry() {
                const w = canvas.width;
                const h = canvas.height;
                const padX = w * 0.11;
                const padY = h * 0.12;
                const cellW = (w - padX * 2) / COLS;
                const cellH = (h - padY * 2) / ROWS;

                return {
                    w, h, padX, padY, cellW, cellH,
                    toPxX: (gx) => padX + gx * cellW,
                    toPxY: (gy) => padY + gy * cellH
                };
            }

            function drawBoard() {
                const g = getGeometry();
                ctx.clearRect(0, 0, g.w, g.h);

                const bgGrad = ctx.createLinearGradient(0, 0, 0, g.h);
                bgGrad.addColorStop(0, '#f8fafc');
                bgGrad.addColorStop(0.5, '#ffffff');
                bgGrad.addColorStop(1, '#f1f5f9');
                ctx.fillStyle = bgGrad;
                ctx.fillRect(0, 0, g.w, g.h);

                // Kratka zeszytowa
                ctx.strokeStyle = '#e2e8f0';
                ctx.lineWidth = 1.2;
                for (let x = 0; x <= COLS; x++) {
                    ctx.beginPath();
                    ctx.moveTo(g.toPxX(x), g.toPxY(0));
                    ctx.lineTo(g.toPxX(x), g.toPxY(ROWS));
                    ctx.stroke();
                }
                for (let y = 0; y <= ROWS; y++) {
                    ctx.beginPath();
                    ctx.moveTo(g.toPxX(0), g.toPxY(y));
                    ctx.lineTo(g.toPxX(COLS), g.toPxY(y));
                    ctx.stroke();
                }

                // Bramki
                ctx.fillStyle = 'rgba(244, 63, 94, 0.14)';
                ctx.fillRect(g.toPxX(3), g.toPxY(-1), g.cellW * 2, g.cellH);

                ctx.fillStyle = 'rgba(37, 99, 235, 0.14)';
                ctx.fillRect(g.toPxX(3), g.toPxY(ROWS), g.cellW * 2, g.cellH);

                // Linia środkowa i koło
                ctx.strokeStyle = '#cbd5e1';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(g.toPxX(0), g.toPxY(ROWS / 2));
                ctx.lineTo(g.toPxX(COLS), g.toPxY(ROWS / 2));
                ctx.stroke();

                ctx.beginPath();
                ctx.arc(g.toPxX(COLS / 2), g.toPxY(ROWS / 2), g.cellW * 1.15, 0, Math.PI * 2);
                ctx.stroke();

                // Obrys boiska
                ctx.strokeStyle = '#0f172a';
                ctx.lineWidth = 4;
                ctx.lineJoin = 'round';
                ctx.beginPath();
                ctx.moveTo(g.toPxX(3), g.toPxY(0));
                ctx.lineTo(g.toPxX(0), g.toPxY(0));
                ctx.lineTo(g.toPxX(0), g.toPxY(ROWS));
                ctx.lineTo(g.toPxX(3), g.toPxY(ROWS));
                ctx.lineTo(g.toPxX(3), g.toPxY(ROWS + 1));
                ctx.lineTo(g.toPxX(5), g.toPxY(ROWS + 1));
                ctx.lineTo(g.toPxX(5), g.toPxY(ROWS));
                ctx.lineTo(g.toPxX(COLS), g.toPxY(ROWS));
                ctx.lineTo(g.toPxX(COLS), g.toPxY(0));
                ctx.lineTo(g.toPxX(5), g.toPxY(0));
                ctx.lineTo(g.toPxX(5), g.toPxY(-1));
                ctx.lineTo(g.toPxX(3), g.toPxY(-1));
                ctx.lineTo(g.toPxX(3), g.toPxY(0));
                ctx.stroke();

                // Kropki siatki
                for (let x = 0; x <= COLS; x++) {
                    for (let y = -1; y <= ROWS + 1; y++) {
                        if (!isValidNode(x, y)) continue;
                        const isVis = state.visited.has(nodeKey(x, y));
                        ctx.beginPath();
                        ctx.arc(g.toPxX(x), g.toPxY(y), isVis ? 4.2 : 2.8, 0, Math.PI * 2);
                        ctx.fillStyle = isVis ? '#334155' : '#94a3b8';
                        ctx.fill();
                    }
                }

                // Narysowane linie
                state.edges.forEach((eKey) => {
                    const [p1, p2] = eKey.split('-');
                    const [x1, y1] = p1.split(',').map(Number);
                    const [x2, y2] = p2.split(',').map(Number);
                    const owner = state.edgeColors.get(eKey);

                    ctx.beginPath();
                    ctx.moveTo(g.toPxX(x1), g.toPxY(y1));
                    ctx.lineTo(g.toPxX(x2), g.toPxY(y2));
                    ctx.strokeStyle = owner === 'p1' ? '#2563eb' : '#e11d48';
                    ctx.lineWidth = 4;
                    ctx.lineCap = 'round';
                    ctx.stroke();
                });

                // Podgląd linii po najechaniu myszką
                const isHumanTurn = state.mode === 'pvp' || state.turn === 'p1';
                if (isHumanTurn && !state.roundOver && state.hoverNode) {
                    const validMoves = getValidMoves(state.ball.x, state.ball.y, state.edges);
                    const targetMove = validMoves.find(m => m.x === state.hoverNode.x && m.y === state.hoverNode.y);
                    if (targetMove) {
                        ctx.save();
                        ctx.beginPath();
                        ctx.moveTo(g.toPxX(state.ball.x), g.toPxY(state.ball.y));
                        ctx.lineTo(g.toPxX(targetMove.x), g.toPxY(targetMove.y));
                        ctx.strokeStyle = state.turn === 'p1' ? 'rgba(37, 99, 235, 0.45)' : 'rgba(225, 29, 72, 0.45)';
                        ctx.lineWidth = 3.5;
                        ctx.setLineDash([5, 5]);
                        ctx.stroke();
                        ctx.restore();
                    }
                }

                // Zawsze widoczne dostępne ruchy
                if (isHumanTurn && !state.roundOver) {
                    const validMoves = getValidMoves(state.ball.x, state.ball.y, state.edges);
                    validMoves.forEach(m => {
                        const isBounce = state.visited.has(nodeKey(m.x, m.y)) || isBoundaryNode(m.x, m.y);
                        const isHovered = state.hoverNode && state.hoverNode.x === m.x && state.hoverNode.y === m.y;

                        ctx.beginPath();
                        ctx.arc(g.toPxX(m.x), g.toPxY(m.y), isHovered ? 10.5 : 7.5, 0, Math.PI * 2);
                        ctx.fillStyle = isBounce ? 'rgba(245, 158, 11, 0.35)' : 'rgba(16, 185, 129, 0.32)';
                        ctx.fill();
                        ctx.lineWidth = 2.2;
                        ctx.strokeStyle = isBounce ? '#d97706' : '#059669';
                        ctx.stroke();
                    });
                }

                // Piłka
                const bx = g.toPxX(state.ball.x);
                const by = g.toPxY(state.ball.y);
                ctx.save();
                ctx.shadowColor = state.turn === 'p1' ? 'rgba(37, 99, 235, 0.65)' : 'rgba(225, 29, 72, 0.65)';
                ctx.shadowBlur = 14;
                ctx.beginPath();
                ctx.arc(bx, by, 10.5, 0, Math.PI * 2);
                ctx.fillStyle = state.turn === 'p1' ? '#2563eb' : '#e11d48';
                ctx.fill();
                ctx.lineWidth = 3;
                ctx.strokeStyle = '#ffffff';
                ctx.stroke();
                ctx.restore();
            }

            function getGridFromEvent(clientX, clientY) {
                const rect = canvas.getBoundingClientRect();
                const dpr = canvas.width / rect.width;
                const px = (clientX - rect.left) * dpr;
                const py = (clientY - rect.top) * dpr;
                const g = getGeometry();

                const gx = Math.round((px - g.padX) / g.cellW);
                const gy = Math.round((py - g.padY) / g.cellH);
                const dist = Math.hypot(px - g.toPxX(gx), py - g.toPxY(gy));

                if (dist <= g.cellW * 0.45 && isValidNode(gx, gy)) {
                    return { x: gx, y: gy };
                }
                return null;
            }

            canvas.addEventListener('mousemove', (e) => {
                if (state.roundOver || (state.mode === 'pve' && state.turn === 'p2')) return;
                state.hoverNode = getGridFromEvent(e.clientX, e.clientY);
                drawBoard();
            });

            function handleBoardInput(clientX, clientY) {
                if (state.roundOver || state.matchOver || state.botThinking) return;
                if (state.mode === 'pve' && state.turn === 'p2') return;

                const target = getGridFromEvent(clientX, clientY);
                if (target) {
                    makeStep(target.x, target.y, state.turn);
                }
            }

            canvas.addEventListener('click', (e) => handleBoardInput(e.clientX, e.clientY));
            canvas.addEventListener('touchstart', (e) => {
                e.preventDefault();
                const t = e.changedTouches[0];
                handleBoardInput(t.clientX, t.clientY);
            }, { passive: false });

            function resizeCanvas() {
                const rect = wrapper.getBoundingClientRect();
                if (rect.width === 0) return;
                const dpr = Math.min(window.devicePixelRatio || 1, 2);
                canvas.width = rect.width * dpr;
                canvas.height = rect.height * dpr;
                drawBoard();
            }

            window.addEventListener('resize', resizeCanvas);
        };
    </script>
</body>
</html>
























