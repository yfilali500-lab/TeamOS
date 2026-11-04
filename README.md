
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TeamOS Aurora</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: "Segoe UI", Arial, sans-serif;
    color: white;
    background: #080b17;
    overflow-x: hidden;
}

/* Aurora Background */

body::before {
    content: "";
    position: fixed;
    inset: -30%;
    z-index: -1;
    background:
        radial-gradient(circle at 20% 20%, #5145d9, transparent 35%),
        radial-gradient(circle at 80% 20%, #087eae, transparent 30%),
        radial-gradient(circle at 60% 80%, #8139cb, transparent 35%),
        #080b17;
    animation: aurora 15s infinite alternate;
}

@keyframes aurora {
    to {
        transform: translate(3%, -3%) rotate(8deg);
        filter: hue-rotate(35deg);
    }
}

/* Navigation */

nav {
    position: sticky;
    top: 15px;
    z-index: 10;
    width: 92%;
    max-width: 1100px;
    margin: 15px auto;
    padding: 15px 20px;

    display: flex;
    justify-content: space-between;
    align-items: center;

    background: rgba(255,255,255,0.07);
    border: 1px solid rgba(255,255,255,0.15);
    border-radius: 20px;

    backdrop-filter: blur(25px);
}

.logo {
    font-size: 23px;
    font-weight: 900;
    color: white;
}

nav a {
    color: #b9c1df;
    text-decoration: none;
    margin-left: 20px;
    transition: 0.3s;
}

nav a:hover {
    color: white;
}

/* Hero */

.container {
    width: 92%;
    max-width: 1100px;
    margin: auto;
}

.hero {
    min-height: 80vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    gap: 40px;
}

.tag {
    display: inline-block;
    padding: 10px 15px;
    border: 1px solid #8b9cff55;
    background: #8b9cff15;
    border-radius: 50px;
    color: #cbd5ff;
    font-size: 12px;
    letter-spacing: 2px;
}

h1 {
    font-size: clamp(48px, 7vw, 82px);
    line-height: 1;
    letter-spacing: -4px;
    margin: 25px 0;

    background: linear-gradient(
        100deg,
        white,
        #c6d0ff,
        #a8f0ff,
        #d8b4fe
    );

    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
}

.hero p {
    color: #b9c1df;
    font-size: 17px;
    line-height: 1.8;
}

.buttons {
    margin-top: 30px;
    display: flex;
    gap: 15px;
    flex-wrap: wrap;
}

.btn {
    display: inline-block;
    padding: 14px 22px;
    border-radius: 15px;
    text-decoration: none;
    color: white;
    font-weight: bold;

    border: 1px solid #ffffff30;
    background: #ffffff10;

    transition: 0.3s;
}

.btn:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 30px #7b70ff50;
}

.primary {
    border: none;
    background: linear-gradient(135deg, #7888ff, #9b67f7);
}

/* Glass Preview */

.preview {
    position: relative;
    animation: floating 6s ease-in-out infinite;
}

@keyframes floating {
    50% {
        transform: translateY(-15px);
    }
}

.screen {
    aspect-ratio: 4 / 3;
    border-radius: 25px;
    overflow: hidden;

    border: 1px solid #ffffff40;

    background:
        radial-gradient(circle at 50% 70%, #8065ff70, transparent 45%),
        radial-gradient(circle at 70% 20%, #40d9ff55, transparent 40%),
        linear-gradient(140deg, #10152d, #1b2450);

    box-shadow: 0 35px 90px #0008;
}

.screen::before {
    content: "T";
    display: grid;
    place-items: center;
    height: 100%;

    font-size: 180px;
    font-weight: 900;
    color: #ffffff20;
}

/* Features */

section {
    padding: 70px 0;
}

.heading {
    text-align: center;
    margin-bottom: 40px;
}

.heading h2 {
    font-size: 42px;
    margin-bottom: 15px;
}

.heading p {
    color: #b9c1df;
}

.features {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

.glass {
    background: rgba(255,255,255,0.07);
    border: 1px solid rgba(255,255,255,0.15);
    border-radius: 25px;
    padding: 25px;

    backdrop-filter: blur(25px);
    box-shadow: 0 20px 60px #0003;

    transition: 0.3s;
}

.glass:hover {
    transform: translateY(-7px);
    border-color: #a5b4fc70;
}

.glass h3 {
    margin-bottom: 12px;
}

.glass p {
    color: #b9c1df;
    line-height: 1.7;
}

/* Download */

.download {
    text-align: center;
    padding: 60px 25px;
}

.download h2 {
    font-size: 40px;
    margin-bottom: 20px;
}

.download p {
    color: #b9c1df;
    margin-bottom: 25px;
}

/* Footer */

footer {
    text-align: center;
    padding: 30px;
    color: #8993b2;
    border-top: 1px solid #ffffff15;
}

/* Responsive */

@media (max-width: 800px) {
    .hero {
        grid-template-columns: 1fr;
        padding: 50px 0;
    }

    .features {
        grid-template-columns: 1fr 1fr;
    }
}

@media (max-width: 550px) {
    .features {
        grid-template-columns: 1fr;
    }

    h1 {
        letter-spacing: -2px;
    }

    nav a {
        margin-left: 10px;
        font-size: 12px;
    }
}
</style>
</head>

<body>

<nav>
    <div class="logo">✦ TeamOS</div>

    <div>
        <a href="#features">Features</a>
        <a href="#about">About</a>
        <a href="#download">Download</a>
    </div>
</nav>

<main class="container">

    <!-- HERO -->

    <div class="hero">

        <div>
            <span class="tag">TEAMOS DESKTOP · AURORA 1.0</span>

            <h1>
                A new feel<br>
                for your desktop.
            </h1>

            <p>
                Meet TeamOS — a modern desktop experience
                wrapped in beautiful glass, fluid motion,
                and a fresh design made for everyday computing.
            </p>

            <div class="buttons">
                <a href="#download" class="btn primary">
                    Get TeamOS ↗
                </a>

                <a href="#features" class="btn">
                    Discover features
                </a>
            </div>
        </div>

        <div class="preview">
            <div class="screen"></div>
        </div>

    </div>

    <!-- FEATURES -->

    <section id="features">

        <div class="heading">
            <h2>Designed to feel different.</h2>
            <p>
                Every detail brings clarity, style, and a little magic.
            </p>
        </div>

        <div class="features">

            <div class="glass">
                <h3>◇ Glass UI</h3>
                <p>
                    Layered translucent surfaces, subtle borders,
                    and soft lighting.
                </p>
            </div>

            <div class="glass">
                <h3>✧ Fluid Animations</h3>
                <p>
                    Elegant motion and ambient aurora effects
                    bring the interface to life.
                </p>
            </div>

            <div class="glass">
                <h3>◐ Modern Experience</h3>
                <p>
                    A clean visual language designed
                    for calm and focused work.
                </p>
            </div>

            <div class="glass">
                <h3>⌘ Desktop Ready</h3>
                <p>
                    A responsive website for desktop,
                    laptop, tablet, and phone screens.
                </p>
            </div>

            <div class="glass">
                <h3>☼ Aurora Atmosphere</h3>
                <p>
                    Midnight colors, glowing gradients,
                    and an animated background.
                </p>
            </div>

            <div class="glass">
                <h3>⚙ Your TeamOS</h3>
                <p>
                    An independent operating system project,
                    evolving with every release.
                </p>
            </div>

        </div>
    </section>

    <!-- ABOUT -->

    <section id="about">

        <div class="glass download">

            <h2>
                Built for everyone.<br>
                Designed for the future.
            </h2>

            <p>
                TeamOS Desktop is an independent
                operating system project.
            </p>

        </div>

    </section>

    <!-- DOWNLOAD -->

    <section id="download">

        <div class="glass download">

            <h2>Download TeamOS Aurora</h2>

            <p>
                TeamOS Aurora 1.0 · x86_64 ISO
            </p>

            <a
                href="./teamos-1.0-aurora-x86_64.iso"
                download="TeamOS-Aurora-1.0-x86_64.iso"
                class="btn primary"
            >
                ⬇ Download TeamOS ISO
            </a>

        </div>

    </section>

</main>

<footer>
    © 2026 TeamOS Desktop · Built for Everyone. Designed for the Future.
</footer>

</body>
</html>
