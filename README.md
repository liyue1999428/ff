<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>X-STREAM | MUSK TERMINAL 2026</title>
    <style>
        :root {
            --neon-green: #00ff41;
            --deep-space: #050505;
            --neural-gray: #1a1a1a;
            --star-white: #ffffff;
            --warning-amber: #ffb000;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; cursor: crosshair; }

        body {
            background-color: var(--deep-space);
            color: var(--neon-green);
            font-family: 'JetBrains Mono', 'Fira Code', monospace;
            overflow-x: hidden;
            background-image: 
                radial-gradient(circle at 2px 2px, rgba(0, 255, 65, 0.05) 1px, transparent 0);
            background-size: 40px 40px;
        }

        /* Glitch Effect Animation */
        @keyframes glitch {
            0% { transform: translate(0); }
            20% { transform: translate(-2px, 2px); }
            40% { transform: translate(-2px, -2px); }
            60% { transform: translate(2px, 2px); }
            80% { transform: translate(2px, -2px); }
            100% { transform: translate(0); }
        }

        header {
            border-bottom: 1px solid var(--neon-green);
            padding: 1.5rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            backdrop-filter: blur(10px);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            letter-spacing: 5px;
            animation: glitch 1s infinite;
        }

        .system-specs {
            font-size: 0.7rem;
            text-align: right;
            line-height: 1;
        }

        .container {
            display: grid;
            grid-template-columns: 300px 1fr 350px;
            gap: 1px;
            background: var(--neon-green); /* Border effect */
            min-height: calc(100vh - 80px);
        }

        .panel {
            background: var(--deep-space);
            padding: 1.5rem;
            overflow-y: auto;
        }

        /* Sidebar: Mission Progress */
        .mission-status {
            font-size: 0.8rem;
        }

        .progress-bar {
            width: 100%;
            height: 4px;
            background: #111;
            margin: 10px 0 20px 0;
            position: relative;
        }

        .progress-fill {
            height: 100%;
            background: var(--neon-green);
            box-shadow: 0 0 10px var(--neon-green);
        }

        /* Main Feed: The News */
        .news-item {
            border: 1px solid #333;
            margin-bottom: 2rem;
            padding: 1.5rem;
            position: relative;
            transition: 0.2s;
        }

        .news-item:hover {
            border-color: var(--neon-green);
            box-shadow: inset 0 0 15px rgba(0, 255, 65, 0.1);
        }

        .category {
            font-size: 0.7rem;
            padding: 2px 8px;
            border: 1px solid var(--neon-green);
            display: inline-block;
            margin-bottom: 1rem;
        }

        h2 { font-size: 1.8rem; margin-bottom: 1rem; color: var(--star-white); }
        p { color: #888; margin-bottom: 1.5rem; font-size: 0.95rem; }

        /* Right Panel: X-Live Stream */
        .x-post {
            background: var(--neural-gray);
            padding: 1rem;
            border-radius: 4px;
            margin-bottom: 1rem;
            font-size: 0.85rem;
            color: #ccc;
        }

        .x-post span { color: var(--warning-amber); }

        /* Scrolling Text Footer */
        footer {
            background: var(--neon-green);
            color: black;
            padding: 5px;
            font-weight: bold;
            font-size: 0.8rem;
            position: fixed;
            bottom: 0;
            width: 100%;
        }

        marquee { width: 100%; }

        ::-webkit-scrollbar { width: 4px; }
        ::-webkit-scrollbar-thumb { background: var(--neon-green); }
    </style>
</head>
<body>

    <header>
        <div class="logo">𝕏 OCCUPY MARS</div>
        <div class="system-specs">
            CPU: NEURALINK v7.2 // STARLINK LATENCY: 12ms<br>
            LOCAL_TIME: <span id="clock">--:--:--</span>
        </div>
    </header>

    <div class="container">
        <aside class="panel">
            <h3 style="margin-bottom: 2rem;">ASSET_TRACKING</h3>
            
            <div class="mission-status">
                <p>STARSHIP HLS (LUNAR)</p>
                <div class="progress-bar"><div class="progress-fill" style="width: 85%;"></div></div>
                
                <p>OPTIMUS GEN-3 DEPLOYMENT</p>
                <div class="progress-bar"><div class="progress-fill" style="width: 42%;"></div></div>
                
                <p>GROK-4 TRAINING FLOPs</p>
                <div class="progress-bar"><div class="progress-fill" style="width: 99%;"></div></div>
                
                <p style="color: var(--warning-amber);">MARS WINDOW 2026: OPENING</p>
            </div>
        </aside>

        <main class="panel" style="border-left: 1px solid var(--neon-green); border-right: 1px solid var(--neon-green);">
            <div class="news-item">
                <span class="category">SPACEX</span>
                <h2>星舰 18 号成功完成“筷子”二次回收，马斯克称其为“文明的胜利”</h2>
                <p>德克萨斯州博卡奇卡：发射台巨大的机械臂再次精准捕获火箭。马斯克随后发推称，第一批火星殖民地所需的 100 万吨物资运输成本已降低 90%。</p>
                <div style="font-size: 0.7rem;">FILE_ID: SX_2026_0316</div>
            </div>

            <div class="news-item">
                <span class="category">NEURALINK</span>
                <h2>首位 Neuralink 盲人用户恢复 20/20 视力</h2>
                <p>由于“盲视 (Blindsight)”芯片的成功植入，医学界正在重新定义人类感官极限。马斯克评论道：“这仅仅是人类向半机械文明进化的第一步。”</p>
            </div>

            <div class="news-item">
                <span class="category">TESLA</span>
                <h2>特斯拉发布“CyberPod”：没有方向盘的移动起居室</h2>
                <p>这款售价 1.9 万美元的完全自动驾驶汽车旨在彻底消灭城市私家车所有权。首批 50,000 台已在旧金山作为无人出租车队上线。</p>
            </div>
        </main>

        <aside class="panel">
            <h3 style="margin-bottom: 2rem;">X_INTEL_STREAM</h3>
            <div class="x-post">
                <span>@elonmusk:</span> 只有通过这种方式，我们才能确保意识的火焰在黑暗中延续。🔥
            </div>
            <div class="x-post">
                <span>@elonmusk:</span> 很快，你的工作就是告诉 AI 你想要什么，剩下的交给 Optimus。
            </div>
            <div class="x-post">
                <span>@doge_official:</span> 难道我们真的要在火星上用 Dogecoin 支付吗？🤯
            </div>
            <div class="x-post">
                <span>@elonmusk:</span> <span>(Replying to @doge_official)</span> 当然。
            </div>
        </aside>
    </div>

    <footer>
        <marquee scrollamount="10">
            DOGE: $1.42 (+12.4%) | TSLA: $420.69 (+0.0%) | MARS DISTANCE: 140M KM | OXYGEN LEVELS: NOMINAL | STARSHIP-24 PREPARING FOR T-MINUS 12 HOURS
        </marquee>
    </footer>

    <script>
        function updateClock() {
            const now = new Date();
            document.getElementById('clock').innerText = now.toTimeString().split(' ')[0];
        }
        setInterval(updateClock, 1000);
        updateClock();
    </script>
</body>
</html>
