<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Erick Ortiz | IT & Cybersecurity Portfolio</title>

    <meta name="description"
          content="Erick Ortiz - IT Support, Networking, Systems Administration and Cybersecurity Portfolio">

    <style>

        /* =========================
           GLOBAL
        ========================= */

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family:
                Inter,
                -apple-system,
                BlinkMacSystemFont,
                "Segoe UI",
                Arial,
                sans-serif;

            background:
                radial-gradient(
                    circle at top right,
                    rgba(0, 119, 255, 0.12),
                    transparent 35%
                ),
                #05070a;

            color: #e6edf3;
            line-height: 1.7;
        }

        a {
            color: inherit;
        }

        .container {
            width: min(1150px, 92%);
            margin: auto;
        }


        /* =========================
           NAVIGATION
        ========================= */

        nav {
            position: sticky;
            top: 0;
            z-index: 1000;

            background: rgba(5, 7, 10, 0.85);
            backdrop-filter: blur(14px);

            border-bottom: 1px solid rgba(255,255,255,0.08);
        }

        .nav-container {
            max-width: 1150px;
            margin: auto;

            padding: 18px 4%;

            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.1rem;
            font-weight: 700;
            color: #ffffff;
        }

        .logo span {
            color: #3da9ff;
        }

        .nav-links {
            display: flex;
            gap: 25px;
            list-style: none;
        }

        .nav-links a {
            color: #9aa7b4;
            text-decoration: none;
            font-size: 0.9rem;
            transition: 0.25s;
        }

        .nav-links a:hover {
            color: #4db5ff;
        }


        /* =========================
           HERO
        ========================= */

        .hero {
            min-height: 80vh;

            display: flex;
            align-items: center;

            padding: 90px 0 70px;

            position: relative;
        }

        .hero-content {
            max-width: 800px;
        }

        .status {
            display: inline-flex;
            align-items: center;
            gap: 8px;

            padding: 7px 13px;

            border-radius: 30px;

            background: rgba(0, 190, 255, 0.08);
            border: 1px solid rgba(0, 190, 255, 0.25);

            color: #6bc7ff;

            font-size: 0.85rem;

            margin-bottom: 25px;
        }

        .status-dot {
            width: 8px;
            height: 8px;

            background: #28d17c;
            border-radius: 50%;

            box-shadow: 0 0 10px #28d17c;
        }

        .hero h1 {
            font-size: clamp(3rem, 8vw, 5.5rem);
            line-height: 1.05;

            margin-bottom: 20px;

            color: #ffffff;
            letter-spacing: -3px;
        }

        .hero h1 span {
            color: #3da9ff;
        }

        .hero-subtitle {
            font-size: 1.35rem;
            color: #aab6c3;

            margin-bottom: 25px;
        }

        .hero-description {
            max-width: 720px;

            color: #8d9aa7;
            font-size: 1.05rem;

            margin-bottom: 35px;
        }


        /* =========================
           BUTTONS
        ========================= */

        .buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .button {
            display: inline-block;

            padding: 12px 20px;

            border-radius: 8px;

            text-decoration: none;
            font-weight: 600;

            transition: 0.25s;
        }

        .button-primary {
            background: #1683e6;
            color: white;

            box-shadow:
                0 8px 30px rgba(22,131,230,0.25);
        }

        .button-primary:hover {
            background: #2b98f5;
            transform: translateY(-2px);
        }

        .button-secondary {
            border: 1px solid #2b3742;
            background: #0d1117;

            color: #d9e2ea;
        }

        .button-secondary:hover {
            border-color: #1683e6;
            color: #4db5ff;
        }


        /* =========================
           SECTIONS
        ========================= */

        section {
            padding: 90px 0;
        }

        .section-header {
            margin-bottom: 40px;
        }

        .section-label {
            color: #3da9ff;

            text-transform: uppercase;
            letter-spacing: 2px;

            font-size: 0.75rem;
            font-weight: 700;

            margin-bottom: 8px;
        }

        h2 {
            font-size: 2.2rem;
            color: white;
        }

        .section-description {
            color: #8996a3;
            max-width: 700px;
            margin-top: 10px;
        }


        /* =========================
           ABOUT
        ========================= */

        .about-grid {
            display: grid;

            grid-template-columns:
                repeat(2, 1fr);

            gap: 25px;
        }

        .card {
            background:
                linear-gradient(
                    145deg,
                    rgba(255,255,255,0.045),
                    rgba(255,255,255,0.015)
                );

            border: 1px solid rgba(255,255,255,0.08);

            border-radius: 14px;

            padding: 28px;

            transition: 0.3s;
        }

        .card:hover {
            border-color: rgba(61,169,255,0.35);

            transform: translateY(-4px);

            box-shadow:
                0 15px 40px rgba(0,0,0,0.25);
        }

        .card h3 {
            color: #ffffff;
            margin-bottom: 12px;
        }

        .card p {
            color: #9aa7b4;
        }


        /* =========================
           PROJECTS
        ========================= */

        .projects {
            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 20px;
        }

        .project {
            display: flex;
            flex-direction: column;

            min-height: 330px;
        }

        .project-icon {
            width: 48px;
            height: 48px;

            display: flex;
            align-items: center;
            justify-content: center;

            border-radius: 10px;

            background: rgba(22,131,230,0.12);

            color: #4db5ff;

            font-size: 1.4rem;

            margin-bottom: 20px;
        }

        .project h3 {
            font-size: 1.2rem;
            margin-bottom: 8px;
        }

        .project p {
            margin-bottom: 20px;
        }

        .tags {
            display: flex;
            flex-wrap: wrap;

            gap: 7px;

            margin-top: auto;
        }

        .tag {
            background: #111820;

            border: 1px solid #263442;

            color: #9eb0c0;

            padding: 5px 9px;

            border-radius: 5px;

            font-size: 0.75rem;
        }

        .project-link {
            margin-top: 20px;

            color: #4db5ff;

            text-decoration: none;

            font-size: 0.9rem;
            font-weight: 600;
        }

        .project-link:hover {
            text-decoration: underline;
        }


        /* =========================
           SKILLS
        ========================= */

        .skills {
            display: flex;
            flex-wrap: wrap;

            gap: 10px;
        }

        .skill {
            padding: 10px 15px;

            border-radius: 8px;

            background: #0d1319;

            border: 1px solid #263442;

            color: #c7d2dc;

            transition: 0.2s;
        }

        .skill:hover {
            border-color: #1683e6;
            color: #4db5ff;
        }


        /* =========================
           EXPERIENCE
        ========================= */

        .timeline {
            border-left: 2px solid #1c354a;

            padding-left: 30px;
        }

        .timeline-item {
            position: relative;

            margin-bottom: 40px;
        }

        .timeline-item::before {
            content: "";

            position: absolute;

            left: -38px;
            top: 7px;

            width: 12px;
            height: 12px;

            background: #1683e6;

            border-radius: 50%;

            box-shadow:
                0 0 15px rgba(22,131,230,0.7);
        }

        .timeline-date {
            color: #4db5ff;

            font-size: 0.85rem;

            margin-bottom: 5px;
        }

        .timeline h3 {
            color: white;

            margin-bottom: 10px;
        }

        .timeline ul {
            padding-left: 20px;
            color: #9aa7b4;
        }

        .timeline li {
            margin-bottom: 7px;
        }


        /* =========================
           CERTIFICATIONS
        ========================= */

        .certifications {
            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 20px;
        }

        .cert {
            padding: 25px;

            background: #0b1015;

            border: 1px solid #202d38;

            border-radius: 12px;
        }

        .cert h3 {
            color: white;

            margin-bottom: 8px;
        }

        .cert p {
            color: #8493a1;

            font-size: 0.9rem;
        }

        .cert-status {
            display: inline-block;

            margin-top: 15px;

            padding: 4px 8px;

            border-radius: 5px;

            font-size: 0.75rem;

            background: rgba(40,209,124,0.1);
            color: #45d98c;
        }

        .cert-progress {
            background: rgba(255,255,255,0.08);

            color: #ffca66;
        }


        /* =========================
           EDUCATION
        ========================= */

        .education {
            max-width: 700px;
        }

        .education h3 {
            color: white;
            margin-bottom: 5px;
        }

        .education .school {
            color: #4db5ff;
            margin-bottom: 10px;
        }


        /* =========================
           CONTACT
        ========================= */

        .contact {
            text-align: center;

            padding: 60px 30px;

            background:
                radial-gradient(
                    circle at center,
                    rgba(22,131,230,0.12),
                    transparent 60%
                );

            border: 1px solid rgba(61,169,255,0.15);

            border-radius: 18px;
        }

        .contact h2 {
            margin-bottom: 15px;
        }

        .contact p {
            color: #8996a3;

            max-width: 600px;

            margin: 0 auto 25px;
        }

        .contact-links {
            display: flex;

            justify-content: center;

            gap: 20px;

            flex-wrap: wrap;
        }

        .contact-links a {
            color: #4db5ff;

            text-decoration: none;

            font-weight: 600;
        }

        .contact-links a:hover {
            text-decoration: underline;
        }


        /* =========================
           FOOTER
        ========================= */

        footer {
            border-top: 1px solid #1c252d;

            padding: 30px 0;

            text-align: center;

            color: #687581;

            font-size: 0.85rem;
        }


        /* =========================
           MOBILE
        ========================= */

        @media (max-width: 850px) {

            .projects,
            .certifications {
                grid-template-columns: 1fr;
            }

            .about-grid {
                grid-template-columns: 1fr;
            }

            .nav-links {
                display: none;
            }

            .hero {
                min-height: auto;

                padding: 80px 0;
            }

            .hero h1 {
                letter-spacing: -2px;
            }
        }

        @media (max-width: 600px) {

            section {
                padding: 65px 0;
            }

            .hero h1 {
                font-size: 3rem;
            }

            .hero-subtitle {
                font-size: 1.1rem;
            }

            .card {
                padding: 22px;
            }
        }

    </style>
</head>

<body>


<!-- =========================
     NAVIGATION
========================= -->

<nav>

    <div class="nav-container">

        <div class="logo">
            Erick<span>Ortiz</span>
        </div>

        <ul class="nav-links">

            <li>
                <a href="#about">About</a>
            </li>

            <li>
                <a href="#projects">Projects</a>
            </li>

            <li>
                <a href="#skills">Skills</a>
            </li>

            <li>
                <a href="#experience">Experience</a>
            </li>

            <li>
                <a href="#certifications">Certifications</a>
            </li>

            <li>
                <a href="#contact">Contact</a>
            </li>

        </ul>

    </div>

</nav>


<main>


<!-- =========================
     HERO
========================= -->

<section class="hero">

    <div class="container">

        <div class="hero-content">

            <div class="status">

                <span class="status-dot"></span>

                Building experience in IT & Cybersecurity

            </div>


            <h1>
                Erick <span>Ortiz</span>
            </h1>


            <p class="hero-subtitle">
                IT Support • Networking • Systems Administration • Cybersecurity
            </p>


            <p class="hero-description">

                Computer Information Systems student and CompTIA Network+
                certified IT professional building hands-on experience in
                technical support, networking, Windows Server, Active Directory,
                PowerShell, and cybersecurity.

            </p>


            <div class="buttons">

                <a
                    class="button button-primary"
                    href="#projects">
                    View My Projects
                </a>

                <a
                    class="button button-secondary"
                    href="https://www.linkedin.com/in/erick-ortiz-1b1046336/"
                    target="_blank">
                    LinkedIn
                </a>

            </div>

        </div>

    </div>

</section>


<!-- =========================
     ABOUT
========================= -->

<section id="about">

    <div class="container">

        <div class="section-header">

            <div class="section-label">
                About Me
            </div>

            <h2>
                Building practical IT experience.
            </h2>

            <p class="section-description">

                My background combines military communications,
                technical troubleshooting, customer support, and
                hands-on IT training.

            </p>

        </div>


        <div class="about-grid">


            <div class="card">

                <h3>
                    Technical Focus
                </h3>

                <p>

                    I am currently developing skills in help desk support,
                    desktop support, networking, systems administration,
                    Active Directory, Windows Server, PowerShell, and
                    cybersecurity.

                </p>

            </div>


            <div class="card">

                <h3>
                    Career Goal
                </h3>

                <p>

                    My goal is to build a strong technical foundation and
                    transition into professional IT roles involving
                    infrastructure, systems administration, networking,
                    and cybersecurity.

                </p>

            </div>


        </div>

    </div>

</section>


<!-- =========================
     PROJECTS
========================= -->

<section id="projects">

    <div class="container">

        <div class="section-header">

            <div class="section-label">
                Projects
            </div>

            <h2>
                Hands-on IT Labs
            </h2>

            <p class="section-description">

                Practical projects demonstrating my technical development
                and understanding of enterprise IT environments.

            </p>

        </div>


        <div class="projects">


            <!-- PROJECT 1 -->

            <div class="card project">

                <div class="project-icon">
                    AD
                </div>

                <h3>
                    Active Directory Enterprise Lab
                </h3>

                <p>

                    Designed and deployed a virtualized Windows domain
                    environment to simulate an enterprise IT infrastructure.

                </p>


                <div class="tags">

                    <span class="tag">Windows Server</span>
                    <span class="tag">Active Directory</span>
                    <span class="tag">DNS</span>
                    <span class="tag">GPO</span>
                    <span class="tag">PowerShell</span>
                    <span class="tag">Hyper-V</span>

                </div>


                <a
                    href="#"
                    class="project-link">

                    View Project →

                </a>

            </div>


            <!-- PROJECT 2 -->

            <div class="card project">

                <div class="project-icon">
                    IT
                </div>

                <h3>
                    Help Desk & IT Support Lab
                </h3>

                <p>

                    Simulated common help desk scenarios including
                    account issues, network connectivity problems,
                    Windows troubleshooting, and system configuration.

                </p>


                <div class="tags">

                    <span class="tag">Windows</span>
                    <span class="tag">Networking</span>
                    <span class="tag">Troubleshooting</span>
                    <span class="tag">Support</span>

                </div>


                <a
                    href="#"
                    class="project-link">

                    Coming Soon →

                </a>

            </div>


            <!-- PROJECT 3 -->

            <div class="card project">

                <div class="project-icon">
                    CY
                </div>

                <h3>
                    Cybersecurity Labs
                </h3>

                <p>

                    Future networking and cybersecurity projects
                    demonstrating security concepts, system hardening,
                    monitoring, and troubleshooting.

                </p>


                <div class="tags">

                    <span class="tag">Cybersecurity</span>
                    <span class="tag">Networking</span>
                    <span class="tag">Security+</span>

                </div>


                <a
                    href="#"
                    class="project-link">

                    More Coming Soon →

                </a>

            </div>


        </div>

    </div>

</section>


<!-- =========================
     SKILLS
========================= -->

<section id="skills">

    <div class="container">

        <div class="section-header">

            <div class="section-label">
                Technical Skills
            </div>

            <h2>
                Technologies & Tools
            </h2>

        </div>


        <div class="skills">

            <span class="skill">Active Directory</span>
            <span class="skill">Windows Server</span>
            <span class="skill">Windows 11</span>
            <span class="skill">Hyper-V</span>
            <span class="skill">DNS</span>
            <span class="skill">Group Policy</span>
            <span class="skill">PowerShell</span>
            <span class="skill">Subnetting</span>
            <span class="skill">Networking</span>
            <span class="skill">Hardware Troubleshooting</span>
            <span class="skill">Technical Support</span>
            <span class="skill">Cable Management</span>
            <span class="skill">C++</span>
            <span class="skill">Python</span>

        </div>

    </div>

</section>


<!-- =========================
     EXPERIENCE
========================= -->

<section id="experience">

    <div class="container">

        <div class="section-header">

            <div class="section-label">
                Experience
            </div>

            <h2>
                Technical Experience
            </h2>

        </div>


        <div class="timeline">


            <div class="timeline-item">

                <div class="timeline-date">
                    October 2023 – Present
                </div>

                <h3>
                    Signal Operations Support Specialist
                </h3>

                <p style="color:#4db5ff; margin-bottom:12px;">
                    Arkansas Army National Guard
                </p>


                <ul>

                    <li>
                        Install, maintain, configure, and troubleshoot
                        military communication systems.
                    </li>

                    <li>
                        Diagnose and resolve hardware and electronic
                        device issues.
                    </li>

                    <li>
                        Configure SATCOM, LOS, and SINCGARS
                        communication equipment.
                    </li>

                    <li>
                        Troubleshoot hardware, software, network
                        connectivity, and system access issues.
                    </li>

                    <li>
                        Follow technical procedures and documentation
                        standards in mission-critical environments.
                    </li>

                </ul>

            </div>


        </div>

    </div>

</section>


<!-- =========================
     CERTIFICATIONS
========================= -->

<section id="certifications">

    <div class="container">

        <div class="section-header">

            <div class="section-label">
                Certifications
            </div>

            <h2>
                Professional Development
            </h2>

        </div>


        <div class="certifications">


            <div class="cert">

                <h3>
                    CompTIA Network+
                </h3>

                <p>
                    Networking infrastructure,
                    troubleshooting, and network operations.
                </p>

                <span class="cert-status">
                    Earned August 2026
                </span>

            </div>


            <div class="cert">

                <h3>
                    CompTIA Security+
                </h3>

                <p>
                    Cybersecurity fundamentals,
                    security operations, and risk management.
                </p>

                <span class="cert-status cert-progress">
                    In Progress
                </span>

            </div>


            <div class="cert">

                <h3>
                    Microsoft Office Specialist
                </h3>

                <p>
                    Microsoft Office productivity
                    and professional software skills.
                </p>

                <span class="cert-status">
                    Certified
                </span>

            </div>


        </div>

    </div>

</section>


<!-- =========================
     EDUCATION
========================= -->

<section id="education">

    <div class="container">

        <div class="section-header">

            <div class="section-label">
                Education
            </div>

            <h2>
                Academic Background
            </h2>

        </div>


        <div class="card education">

            <h3>
                Computer Information Systems
            </h3>

            <p class="school">
                Arkansas State University-Beebe
            </p>

            <p>
                Associate of Science
            </p>

            <p>
                Expected May 2027
            </p>

            <br>

            <p>

                Coursework and labs focus on computer hardware,
                software, networking, information systems,
                programming, and technical problem-solving.

            </p>

        </div>

    </div>

</section>


<!-- =========================
     CONTACT
========================= -->

<section id="contact">

    <div class="container">

        <div class="contact">

            <div class="section-label">
                Contact
            </div>

            <h2>
                Let's Connect
            </h2>

            <p>

                I am interested in opportunities involving IT support,
                help desk, desktop support, networking, systems
                administration, and cybersecurity.

            </p>


            <div class="contact-links">

                <a href="mailto:eor.tiz339@outlook.com">
                    Email
                </a>

                <a
                    href="https://www.linkedin.com/in/erick-ortiz-1b1046336/"
                    target="_blank">
                    LinkedIn
                </a>

                <a
                    href="#"
                    target="_blank">
                    GitHub
                </a>

            </div>

        </div>

    </div>

</section>


</main>


<!-- =========================
     FOOTER
========================= -->

<footer>

    <div class="container">

        <p>
            © 2026 Erick Ortiz
        </p>

        <p>
            IT Support • Networking • Cybersecurity
        </p>

    </div>

</footer>


</body>
</html>
