<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Umar Shah - GitHub Profile</title>
    <style>
        :root {
            --bg-color: #0d1117;
            --card-bg: #161b22;
            --text-main: #f0f6fc;
            --border-color: #30363d;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-main);
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
            margin: 0;
            padding: 20px;
            overflow-x: hidden;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            padding: 40px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.5);
            animation: fadeIn 1.2s cubic-bezier(0.16, 1, 0.3, 1) forwards;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .header-title {
            text-align: center;
            font-size: 2.8rem;
            font-weight: 800;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #00f0ff, #ff007f, #7928ca);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: colorShift 6s ease infinite;
            background-size: 200% 200%;
        }

        @keyframes colorShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .typing-container {
            text-align: center;
            margin-bottom: 30px;
        }

        .section-title {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 1.5rem;
            border-bottom: 2px solid var(--border-color);
            padding-bottom: 10px;
            margin-top: 40px;
            margin-bottom: 20px;
        }

        .word-transition {
            display: inline-block;
            transition: transform 0.4s ease, color 0.4s ease;
            cursor: default;
        }

        .word-transition:hover {
            transform: translateY(-4px) scale(1.05);
            color: #00f0ff;
            text-shadow: 0 0 12px rgba(0,240,255,0.6);
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            align-items: center;
        }

        .about-text ul {
            list-style: none;
            padding: 0;
            line-height: 1.8;
        }

        .profile-img {
            width: 100%;
            border-radius: 12px;
            box-shadow: 0 8px 25px rgba(0, 240, 255, 0.3);
            transition: transform 0.5s ease, box-shadow 0.5s ease;
        }

        .profile-img:hover {
            transform: scale(1.03);
            box-shadow: 0 12px 35px rgba(255, 0, 127, 0.5);
        }

        .repo-grid, .stats-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .stat-card, .repo-card {
            background: #0d1117;
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 15px;
            text-align: center;
            transition: transform 0.4s ease, border-color 0.4s ease, box-shadow 0.4s ease;
        }

        .stat-card:hover, .repo-card:hover {
            transform: translateY(-6px);
            border-color: #00f0ff;
            box-shadow: 0 8px 25px rgba(0, 240, 255, 0.25);
        }

        .stat-card img, .repo-card img {
            width: 100%;
            border-radius: 8px;
        }

        .tech-stack {
            text-align: center;
            padding: 20px 0;
        }

        .tech-stack img {
            max-width: 100%;
            transition: transform 0.4s ease;
        }

        .tech-stack img:hover {
            transform: scale(1.05);
        }

        .connect-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
        }

        .connect-btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 12px 24px;
            border-radius: 8px;
            font-weight: bold;
            color: #fff;
            text-decoration: none;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .btn-gmail { background-color: #D14836; }
        .btn-github { background-color: #24292e; border: 1px solid var(--border-color); }

        .connect-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 20px rgba(255,255,255,0.2);
        }

        @media(max-width: 768px) {
            .about-grid, .repo-grid, .stats-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

<div class="container">
    <div class="header-title">Umar Shah 🚀</div>
    
    <div class="typing-container">
        <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=700&size=24&pause=1000&color=00F0FF&center=true&vCenter=true&width=750&lines=Data+Science+Student+%7C+Python+Developer;Building+Next-Gen+Web+Apps+%26+Systems;Turning+Raw+Data+Into+Clean+Solutions" alt="Typing SVG" />
    </div>

    <!-- About Me Section -->
    <div class="section-title">
        <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Hand%20Gestures/Waving-Hand.png" width="35" height="35" />
        <span class="word-transition" style="color: #00F0FF;">About</span> 
        <span class="word-transition" style="color: #FF007F;">Me</span>
    </div>
    
    <div class="about-grid">
        <div class="about-text">
            <ul>
                <li>🎯 <span class="word-transition"><b>Major:</b></span> BS Data Science (BSDS 2A)</li>
                <li>📍 <span class="word-transition"><b>Location:</b></span> Lahore, Pakistan</li>
                <li>💻 <span class="word-transition"><b>Core Stack:</b></span> Python, Django, NumPy, C++</li>
                <li>⚡ <span class="word-transition"><b>Passion:</b></span> Building smart tools & backend web architectures</li>
                <li>🤝 <span class="word-transition"><b>Collaboration:</b></span> Open to innovative tech & data projects</li>
            </ul>
        </div>
        <div>
            <img src="https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5?q=80&w=700&auto=format&fit=crop" class="profile-img" alt="Tech Matrix" />
        </div>
    </div>

    <!-- Featured Repositories -->
    <div class="section-title">
        <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Laptop.png" width="35" height="35" />
        <span class="word-transition" style="color: #00F0FF;">Featured</span> 
        <span class="word-transition" style="color: #FF007F;">Repositories</span>
    </div>

    <div class="repo-grid">
        <div class="repo-card">
            <a href="https://github.com/UmarXCode/DjangoEncoder-decoder" target="_blank">
                <img src="https://github-readme-stats.vercel.com/api/pin/?username=UmarXCode&repo=DjangoEncoder-decoder&theme=tokyonight&hide_border=true&bg_color=161b22&title_color=00f0ff&icon_color=ff007f" alt="Repo 1" />
            </a>
        </div>
        <div class="repo-card">
            <a href="https://github.com/UmarXCode/UmarXCode" target="_blank">
                <img src="https://github-readme-stats.vercel.com/api/pin/?username=UmarXCode&repo=UmarXCode&theme=tokyonight&hide_border=true&bg_color=161b22&title_color=00f0ff&icon_color=ff007f" alt="Repo 2" />
            </a>
        </div>
    </div>

    <!-- Tech Stack -->
    <div class="section-title">
        <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Wrench.png" width="35" height="35" />
        <span class="word-transition" style="color: #00F0FF;">Tech</span> 
        <span class="word-transition" style="color: #FF007F;">Stack</span> 
        <span class="word-transition" style="color: #00F0FF;">&</span> 
        <span class="word-transition" style="color: #FF007F;">Tools</span>
    </div>

    <div class="tech-stack">
        <img src="https://skillicons.dev/icons?i=python,django,cpp,git,github,vscode,pycharm,windows,linux" alt="Tech Stack Icons" />
    </div>

    <!-- Analytics & Graphs -->
    <div class="section-title">
        <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Travel%20and%20places/Fire.png" width="35" height="35" />
        <span class="word-transition" style="color: #00F0FF;">Advanced</span> 
        <span class="word-transition" style="color: #FF007F;">Analytics</span> 
        <span class="word-transition" style="color: #00F0FF;">&</span> 
        <span class="word-transition" style="color: #FF007F;">Graphs</span>
    </div>

    <div style="margin-bottom: 20px;">
        <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=UmarXCode&theme=tokyonight" width="100%" style="border-radius: 10px;" />
    </div>

    <div class="stats-grid" style="margin-bottom: 20px;">
        <div class="stat-card">
            <img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=UmarXCode&theme=tokyonight" alt="GitHub Stats" />
        </div>
        <div class="stat-card">
            <img src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=UmarXCode&theme=tokyonight&utcOffset=5" alt="Productive Time" />
        </div>
    </div>

    <div class="stats-grid" style="margin-bottom: 20px;">
        <div class="stat-card">
            <img src="https://github-readme-streak-stats.herokuapp.com/?user=UmarXCode&theme=tokyonight&hide_border=true&background=161b22&ring=00f0ff&fire=ff007f&currStreakNum=ffffff" alt="Streak Stats" />
        </div>
        <div class="stat-card">
            <img src="https://github-readme-stats.vercel.com/api/top-langs/?username=UmarXCode&layout=compact&theme=tokyonight&hide_border=true&bg_color=161b22&title_color=00f0ff" alt="Top Languages" />
        </div>
    </div>

    <div class="stats-grid">
        <div class="stat-card">
            <img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=UmarXCode&theme=tokyonight" alt="Repos per Language" />
        </div>
        <div class="stat-card">
            <img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=UmarXCode&theme=tokyonight" alt="Most Commit Language" />
        </div>
    </div>

    <!-- Let's Connect -->
    <div class="section-title">
        <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Telephoning.png" width="35" height="35" />
        <span class="word-transition" style="color: #00F0FF;">Let's</span> 
        <span class="word-transition" style="color: #FF007F;">Connect</span>
    </div>

    <div class="connect-links">
        <a href="mailto:umarshah.dev@gmail.com" class="connect-btn btn-gmail">📧 Email Me</a>
        <a href="https://github.com/UmarXCode" target="_blank" class="connect-btn btn-github">🐙 GitHub Profile</a>
    </div>
</div>

<script>
    // JavaScript Interactive Color Cycling & Dynamic Hover Effects
    const dynamicWords = document.querySelectorAll('.word-transition');
    const colorPalette = ['#00f0ff', '#ff007f', '#7928ca', '#3b82f6', '#10b981', '#f59e0b'];

    dynamicWords.forEach((word) => {
        word.addEventListener('mouseenter', () => {
            const randomColor = colorPalette[Math.floor(Math.random() * colorPalette.length)];
            word.style.color = randomColor;
            word.style.textShadow = `0 0 15px ${randomColor}`;
        });

        word.addEventListener('mouseleave', () => {
            word.style.textShadow = 'none';
        });
    });

    // Console greeting effect
    console.log("%c🚀 Welcome to Umar Shah's Ultimate GitHub Profile!", "color: #00f0ff; font-size: 16px; font-weight: bold;");
</script>

</body>
</html>
