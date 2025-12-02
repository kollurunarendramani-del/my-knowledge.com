<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Knowledge - World of Knowledge</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Segoe UI", Arial, sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background: #f4f6f9;
            color: #333;
            line-height: 1.6;
        }

        header {
            background: #4a90e2;
            color: #fff;
            padding: 2rem 1rem 1rem;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            transition: background 0.3s;
        }

        header h1 {
            font-size: 2.5rem;
        }

        nav a {
            color: #fff;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #ffdd57;
        }

        section {
            max-width: 1000px;
            margin: 2rem auto;
            padding: 2rem;
            background: #fff;
            border-radius: 12px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.6s ease;
        }

        section.show {
            opacity: 1;
            transform: translateY(0);
        }

        .projects {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .project-card {
            background: #fff;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            transition: 0.3s;
        }

        .project-card iframe {
            width: 100%;
            height: 200px;
            border: none;
            border-radius: 10px;
        }

        .contact-links a {
            margin: 10px;
            padding: 12px 18px;
            border-radius: 30px;
            background: #4a90e2;
            color: #fff;
            text-decoration: none;
            display: inline-block;
            transition: 0.3s;
        }

        .contact-links a:hover {
            transform: scale(1.08);
        }

        footer {
            text-align: center;
            padding: 1rem;
            background: #eee;
            color: #555;
        }

        .dark-toggle {
            position: fixed;
            top: 15px;
            right: 15px;
            background: #4a90e2;
            color: white;
            padding: 8px 12px;
            border-radius: 5px;
            cursor: pointer;
        }

        #backToTop {
            position: fixed;
            bottom: 25px;
            right: 25px;
            background: #4a90e2;
            color: #fff;
            padding: 10px 15px;
            border-radius: 50px;
            font-size: 18px;
            cursor: pointer;
            display: none;
        }
    </style>
</head>

<body>
    <button class="dark-toggle" onclick="toggleDark()">🌙 Dark Mode</button>
    <div id="backToTop" onclick="scrollToTop()"><i class="fas fa-chevron-up"></i></div>

    <header>
        <h1>My Knowledge</h1>
        <p>World of Knowledge</p>
        <nav>
            <a href="#about">About</a>
            <a href="#projects">Latest Videos</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <section id="about">
        <h2>About Me</h2>
        <p>Hello everyone! Welcome to <strong>My Knowledge</strong> — your place for information, learning, and help in difficult situations.</p>
    </section>

    <section id="projects">
        <h2>Latest Videos</h2>
        <div class="projects" id="video-list">
            <p>Loading videos...</p>
        </div>

        <div class="subscribe-container">
            <!-- YOUR REAL CHANNEL ID INSERTED HERE -->
            <div class="g-ytsubscribe" data-channelid="UCVczVdXDztAmrVnQ7eMwNug" data-layout="default" data-count="default"></div>
        </div>

        <script src="https://apis.google.com/js/platform.js"></script>
    </section>

    <section id="contact">
        <h2>Contact</h2>
        <div class="contact-links">
            <a href="https://youtube.com/@myknowledge-m2y" target="_blank">
                <i class="fab fa-youtube"></i> YouTube Channel
            </a>

            <a href="https://whatsapp.com/channel/0029Vb59PTrD8SDwpQ86bJ1T" target="_blank">
                <i class="fab fa-whatsapp"></i> WhatsApp
            </a>

            <a href="tel:+919381219808">
                <i class="fas fa-phone"></i> +91 9381219808
            </a>
        </div>
    </section>

    <footer>
        <p>2025 My Knowledge. All rights reserved.</p>
    </footer>

    <script>
        function toggleDark() {
            document.body.classList.toggle("dark");
        }

        function scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        window.addEventListener("scroll", () => {
            const btn = document.getElementById("backToTop");
            btn.style.display = window.scrollY > 300 ? "block" : "none";
        });

        const sections = document.querySelectorAll("section");
        window.addEventListener("scroll", () => {
            sections.forEach(sec => {
                const rect = sec.getBoundingClientRect();
                if (rect.top < window.innerHeight - 100) {
                    sec.classList.add("show");
                }
            });
        });
    </script>
</body>
</html>
