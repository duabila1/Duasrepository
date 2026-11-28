
<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        scroll-behavior: smooth;
    }

    /* PROFESSIONAL ANIMATED BACKGROUND */

    body {
        font-family: Arial, sans-serif;
        background: linear-gradient(
            -45deg,
            #07111f,
            #0b1d35,
            #102d50,
            #08172b,
            #0b1220
        );
        background-size: 400% 400%;
        animation: gradientMove 15s ease infinite;
        color: white;
        line-height: 1.7;
        position: relative;
        overflow-x: hidden;
    }

    @keyframes gradientMove {
        0% { background-position: 0% 50%; }
        50% { background-position: 100% 50%; }
        100% { background-position: 0% 50%; }
    }

    /* SOFT BLUE GLOW EFFECT */

    body::before {
        content: "";
        position: fixed;
        width: 450px;
        height: 450px;
        top: 15%;
        left: -180px;
        background: #168bd0;
        opacity: 0.12;
        filter: blur(130px);
        border-radius: 50%;
        pointer-events: none;
        z-index: 0;
        animation: glowMove 10s ease-in-out infinite alternate;
    }

    body::after {
        content: "";
        position: fixed;
        width: 400px;
        height: 400px;
        bottom: 5%;
        right: -180px;
        background: #55c2ff;
        opacity: 0.10;
        filter: blur(130px);
        border-radius: 50%;
        pointer-events: none;
        z-index: 0;
        animation: glowMove 12s ease-in-out infinite alternate-reverse;
    }

    @keyframes glowMove {
        from { transform: translate(0, 0); }
        to { transform: translate(220px, 120px); }
    }

    /* KEEP CONTENT ABOVE BACKGROUND */

    header, section, footer {
        position: relative;
        z-index: 1;
    }

    header {
        background: rgba(17, 28, 48, 0.90);
        backdrop-filter: blur(12px);
        padding: 20px 8%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        border-bottom: 1px solid rgba(85, 194, 255, 0.15);
    }

    header h2 {
        color: #55c2ff;
    }

    nav a {
        color: white;
        text-decoration: none;
        margin: 10px;
        transition: 0.3s;
    }

    nav a:hover {
        color: #55c2ff;
    }

    section {
        padding: 65px 10%;
        animation: fadeUp 1s ease both;
    }

    /* SECTION ENTRANCE ANIMATION */

    @keyframes fadeUp {
        from {
            opacity: 0;
            transform: translateY(20px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    .home {
        min-height: 75vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .home h1 {
        font-size: 42px;
        margin-bottom: 10px;
    }

    .home h1 span {
        color: #55c2ff;
    }

    h2 {
        color: #55c2ff;
        margin-bottom: 20px;
    }

    .card {
        background: rgba(21, 36, 58, 0.88);
        backdrop-filter: blur(8px);
        padding: 22px;
        border-radius: 12px;
        margin: 15px 0;
        border: 1px solid rgba(85, 194, 255, 0.10);
    }

    .card h3 {
        color: #55c2ff;
    }

    /* PROJECT SECTION */

    .projects-container {
        display: grid;
        grid-template-columns: repeat(
            auto-fit,
            minmax(230px, 1fr)
        );
        gap: 22px;
        margin-top: 20px;
    }

    .project-card {
        background: rgba(21, 36, 58, 0.90);
        backdrop-filter: blur(8px);
        padding: 25px;
        border-radius: 12px;
        border: 1px solid #263d59;
        transition: 0.3s ease;
        overflow: hidden;
    }

    .project-card:hover {
        transform: translateY(-7px);
        border-color: #55c2ff;
        box-shadow: 0 10px 30px rgba(22, 139, 208, 0.18);
    }

    /* PROJECT IMAGE STYLING - ALL PROJECTS */

    .project-card img {
        width: 100%;
        height: 220px;
        object-fit: cover;
        object-position: top center;
        border-radius: 10px;
        margin-bottom: 15px;
        display: block;
        transition: transform 0.4s ease;
    }

    /* FIRST PROJECT - SHOES IMAGE */

    .project-card:nth-child(1) img {
        object-position: center top;
    }

    /* SECOND PROJECT - CLOTHING IMAGE */

    .project-card:nth-child(2) img {
        object-position: center top;
    }

    /* IMAGE HOVER ANIMATION */

    .project-card:hover img {
        transform: scale(1.03);
    }

    .project-card h3 {
        color: #55c2ff;
        margin-bottom: 12px;
    }

    .project-card p {
        margin-bottom: 18px;
        color: #d1dbe8;
    }

    .project-button {
        display: inline-block;
        background: #168bd0;
        color: white;
        padding: 9px 17px;
        border-radius: 6px;
        text-decoration: none;
        margin-top: 8px;
        margin-right: 5px;
        transition: 0.3s;
    }

    .project-button:hover {
        background: #55c2ff;
        color: #0b1220;
        transform: translateY(-2px);
    }

    footer {
        text-align: center;
        padding: 25px;
        background: rgba(17, 28, 48, 0.90);
        border-top: 1px solid rgba(85, 194, 255, 0.15);
    }

    .button {
        display: inline-block;
        background: #168bd0;
        color: white;
        padding: 10px 22px;
        border-radius: 6px;
        text-decoration: none;
        margin-top: 20px;
        transition: 0.3s;
    }

    .button:hover {
        background: #55c2ff;
        color: #0b1220;
        transform: translateY(-3px);
    }

    /* MOBILE RESPONSIVE DESIGN */

    @media (max-width: 600px) {
        header {
            flex-direction: column;
            gap: 12px;
        }

        nav {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }

        .home h1 {
            font-size: 32px;
        }

        section {
            padding: 45px 7%;
        }

        .project-card img {
            height: 190px;
        }
    }

    /* ACCESSIBILITY */

    @media (prefers-reduced-motion: reduce) {
        *,
        *::before,
        *::after {
            animation: none !important;
            scroll-behavior: auto !important;
            transition: none !important;
        }
    }

</style>

