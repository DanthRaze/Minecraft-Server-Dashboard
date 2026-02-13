<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MC Server Dashboard v1.0</title>
    <style>
        :root {
            --bg-color: #0f172a;
            --sidebar-color: #1e293b;
            --accent-color: #38bdf8;
            --text-main: #f8fafc;
            --text-dim: #94a3b8;
            --card-bg: #1e293b;
            --success: #22c55e;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            margin: 0;
            display: flex;
            min-height: 100vh;
        }

        /* Sidebar Navigation */
        nav {
            width: 240px;
            background-color: var(--sidebar-color);
            border-right: 1px solid #334155;
            padding: 2rem 1rem;
            flex-shrink: 0;
        }

        .logo {
            font-size: 1.25rem;
            font-weight: bold;
            color: var(--accent-color);
            margin-bottom: 2rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .nav-links {
            list-style: none;
            padding: 0;
        }

        .nav-links li {
            padding: 12px 15px;
            margin-bottom: 8px;
            border-radius: 8px;
            cursor: pointer;
            transition: 0.2s;
            color: var(--text-dim);
        }

        .nav-links li:hover, .nav-links li.active {
            background-color: #334155;
            color: var(--text-main);
        }

        /* Main Content */
        main {
            flex-grow: 1;
            padding: 2rem 3rem;
            max-width: 1000px;
        }

        header {
            border-bottom: 1px solid #334155;
            margin-bottom: 2rem;
            padding-bottom: 1rem;
        }

        h1 { margin: 0; font-size: 2rem; }
        .version { font-size: 0.9rem; color: var(--accent-color); }

        /* Setup Steps */
        .setup-section {
            display: flex;
            flex-direction: column;
            gap: 2.5rem;
        }

        .step-card {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 1.5rem;
            border: 1px solid #334155;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }

        .step-number {
            background: var(--accent-color);
            color: var(--bg-color);
            width: 28px;
            height: 28px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            font-weight: bold;
            margin-right: 10px;
        }

        h3 { margin-top: 0; color: var(--accent-color); text-transform: uppercase; letter-spacing: 1px; }

        .image-container {
            margin-top: 1rem;
            border-radius: 8px;
            overflow: hidden;
            border: 2px solid #334155;
        }

        img {
            width: 100%;
            height: auto;
            display: block;
        }

        .info-box {
            border-left: 4px solid var(--accent-color);
            background: #1e293b;
            padding: 1rem;
            margin: 1rem 0;
            font-style: italic;
        }

        footer {
            margin-top: 4rem;
            padding: 2rem 0;
            color: var(--text-dim);
            font-size: 0.9rem;
            border-top: 1px solid #334155;
        }

        code {
            background: #0f172a;
            padding: 2px 6px;
            border-radius: 4px;
            color: var(--accent-color);
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo">⛏️ MC Dash</div>
        <ul class="nav-links">
            <li class="active" onclick="alert('Dashboard Loaded')">Dashboard</li>
            <li onclick="alert('Console Loaded')">Console</li>
            <li onclick="alert('Player List Loaded')">Players</li>
            <li onclick="alert('File Manager Loaded')">File Manager</li>
            <li onclick="alert('Settings Loaded')">Settings</li>
        </ul>
    </nav>

    <main>
        <header>
            <h1>Minecraft Server Dashboard</h1>
            <span class="version">Version 1.0 Stable</span>
        </header>

        <section class="setup-section">
            <h3>Setting Up Your Server</h3>

            <div class="step-card">
                <p><span class="step-number">1</span> Click <strong>"Select Server Folder"</strong> and navigate to your Minecraft server directory:</p>
                <div class="image-container">
                    <img src="https://github.com/user-attachments/assets/21ba42ec-f2dd-4f65-acd4-b86b791968f1" alt="Setup Wizard">
                </div>
            </div>

            <div class="step-card">
                <p><span class="step-number">2</span> If you have multiple jars, select your preferred engine (e.g., <code>paper.jar</code>) and allocate RAM (e.g., <code>4GB</code>). Click the <strong>white button</strong> to proceed.</p>
                <div class="image-container">
                    <img src="https://github.com/user-attachments/assets/397dce5b-0f9d-438a-afff-6710e279393f" alt="Setup Options">
                </div>
            </div>

            <div class="info-box">
                You will now be greeted with the main dashboard. Control is at your fingertips!
            </div>

            <div class="step-card">
                <div class="image-container">
                    <img src="https://github.com/user-attachments/assets/b731d13c-44f0-4747-84ba-fa94143d1620" alt="Dashboard View">
                </div>
                <p style="margin-top: 1.5rem;">
                    From here, management is simple. <strong>Start</strong> will launch your server immediately. Use the <strong>Live Console</strong> to send and receive commands in real-time.
                </p>
            </div>
        </section>

        <footer>
            <p>Note: As this is an early stage release, you may encounter minor glitches. We are working hard to polish the experience. Enjoy!</p>
        </footer>
    </main>

    <script>
        // Simple script to handle navigation highlighting
        const links = document.querySelectorAll('.nav-links li');
        links.forEach(link => {
            link.addEventListener('click', () => {
                links.forEach(l => l.classList.remove('active'));
                link.classList.add('active');
            });
        });
    </script>
</body>
</html>
