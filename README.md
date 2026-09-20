<!DOCTYPE html>
<html lang="en">

<head>

    <!-- =========================================================
         BASIC INFORMATION
    ========================================================== -->

    <meta charset="UTF-8">

    <meta name="viewport"
          content="width=device-width, initial-scale=1.0">

    <meta name="description"
          content="Sandesh Gandhgule — 3D Architectural Visualizer and 3D Artist.">

    <title>Sandesh Gandhgule | 3D Architectural Visualizer</title>


    <!-- =========================================================
         FONTS
    ========================================================== -->

    <link rel="preconnect" href="https://fonts.googleapis.com">

    <link rel="preconnect"
          href="https://fonts.gstatic.com"
          crossorigin>

    <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=Playfair+Display:wght@500;600&family=Poppins:wght@300;400;500;600&display=swap"
          rel="stylesheet">


    <!-- =========================================================
         STYLE
    ========================================================== -->

    <style>

        /* -------------------------------------------------------
           BASIC SETTINGS
        ------------------------------------------------------- */

        :root {

            --gold: #d4af37;

            --black: #080808;

            --dark: #101010;

            --dark-2: #151515;

            --white: #ffffff;

            --grey: #aaa;

            --line: rgba(255,255,255,0.12);

        }


        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }


        html {
            scroll-behavior: smooth;
        }


        body {

            background: var(--black);

            color: var(--white);

            font-family: Poppins, sans-serif;

            line-height: 1.6;

        }


        img {

            width: 100%;

            display: block;

        }


        a {

            color: inherit;

            text-decoration: none;

        }


        button {

            font-family: inherit;

        }



        /* -------------------------------------------------------
           HEADER
        ------------------------------------------------------- */

        header {

            position: fixed;

            top: 0;

            left: 0;

            width: 100%;

            z-index: 1000;

            padding: 22px 6%;

            display: flex;

            align-items: center;

            justify-content: space-between;

            transition: 0.3s;

        }


        header.scrolled {

            background: rgba(8,8,8,0.94);

            backdrop-filter: blur(15px);

            padding: 15px 6%;

            border-bottom: 1px solid var(--line);

        }


        .logo {

            font-family: "Playfair Display", serif;

            font-size: 24px;

            letter-spacing: 3px;

            color: var(--gold);

        }


        nav {

            display: flex;

            gap: 28px;

        }


        nav a {

            font-size: 11px;

            text-transform: uppercase;

            letter-spacing: 1.5px;

            color: #ccc;

            transition: 0.3s;

        }


        nav a:hover {

            color: var(--gold);

        }



        /* -------------------------------------------------------
           HERO
        ------------------------------------------------------- */

        .hero {

            min-height: 100vh;

            position: relative;

            display: flex;

            align-items: flex-end;

            overflow: hidden;

        }


        .hero-image {

            position: absolute;

            inset: 0;

        }


        .hero-image img {

            width: 100%;

            height: 100%;

            object-fit: cover;

            filter: brightness(0.55);

        }


        .hero-image::after {

            content: "";

            position: absolute;

            inset: 0;

            background:

                linear-gradient(

                    to top,

                    rgba(0,0,0,0.95),

                    rgba(0,0,0,0.15),

                    rgba(0,0,0,0.35)

                );

        }


        .hero-content {

            position: relative;

            z-index: 2;

            width: 88%;

            max-width: 1400px;

            margin: auto;

            padding-bottom: 100px;

        }


        .small-title {

            color: var(--gold);

            font-size: 11px;

            letter-spacing: 3px;

            text-transform: uppercase;

        }


        .hero h1 {

            font-family: "Playfair Display", serif;

            font-weight: 500;

            font-size: clamp(50px, 8vw, 105px);

            line-height: 0.95;

            margin: 20px 0;

            max-width: 1000px;

        }


        .hero h1 span {

            color: var(--gold);

        }


        .hero-description {

            max-width: 650px;

            color: #ccc;

            font-size: 14px;

            line-height: 1.9;

        }


        .buttons {

            display: flex;

            gap: 12px;

            flex-wrap: wrap;

            margin-top: 30px;

        }


        .button {

            display: inline-block;

            padding: 14px 23px;

            border: 1px solid var(--line);

            font-size: 10px;

            letter-spacing: 1.5px;

            text-transform: uppercase;

            transition: 0.3s;

        }


        .button.gold {

            background: var(--gold);

            border-color: var(--gold);

            color: #000;

        }


        .button:hover {

            transform: translateY(-3px);

            border-color: var(--gold);

        }



        /* -------------------------------------------------------
           GENERAL SECTIONS
        ------------------------------------------------------- */

        section {

            padding: 110px 7%;

        }


        .dark-section {

            background: var(--dark);

        }


        .section-number {

            color: var(--gold);

            font-size: 10px;

            letter-spacing: 3px;

            text-transform: uppercase;

        }


        .section-title {

            font-family: "Playfair Display", serif;

            font-size: clamp(42px, 6vw, 72px);

            font-weight: 500;

            line-height: 1;

            margin: 12px 0 25px;

        }


        .section-intro {

            max-width: 650px;

            color: var(--grey);

            font-size: 13px;

            line-height: 1.9;

            margin-bottom: 50px;

        }



        /* -------------------------------------------------------
           SHOWREEL
        ------------------------------------------------------- */

        .showreel {

            padding: 0;

            position: relative;

            background: #000;

        }


        .showreel video {

            width: 100%;

            height: 75vh;

            object-fit: cover;

            display: block;

            filter: brightness(0.55);

        }


        .showreel-content {

            position: absolute;

            inset: 0;

            display: flex;

            flex-direction: column;

            justify-content: center;

            align-items: center;

            text-align: center;

            padding: 30px;

        }


        .showreel-content h2 {

            font-family: "Playfair Display", serif;

            font-size: clamp(45px, 7vw, 90px);

            font-weight: 500;

            line-height: 0.95;

            max-width: 900px;

            margin: 15px 0 30px;

        }



        /* -------------------------------------------------------
           WORK / PROJECTS
        ------------------------------------------------------- */

        .projects {

            display: grid;

            grid-template-columns: repeat(2, 1fr);

            gap: 25px;

        }


        .project {

            position: relative;

            overflow: hidden;

            background: var(--dark-2);

            cursor: pointer;

        }


        .project.large {

            grid-column: span 2;

        }


        .project-image {

            position: relative;

            overflow: hidden;

        }


        .project-image img {

            aspect-ratio: 16 / 10;

            object-fit: cover;

            transition: 0.7s;

        }


        .project.large .project-image img {

            aspect-ratio: 21 / 10;

        }


        .project:hover img {

            transform: scale(1.04);

        }


        .project-overlay {

            position: absolute;

            inset: 0;

            display: flex;

            flex-direction: column;

            justify-content: flex-end;

            padding: 35px;

            background:

                linear-gradient(

                    transparent 35%,

                    rgba(0,0,0,0.9)

                );

        }


        .project-category {

            color: var(--gold);

            font-size: 9px;

            letter-spacing: 2px;

            text-transform: uppercase;

        }


        .project-title {

            font-family: "Playfair Display", serif;

            font-size: 30px;

            font-weight: 500;

            margin: 5px 0;

        }


        .project-description {

            color: #bbb;

            font-size: 11px;

        }


        .project-arrow {

            color: var(--gold);

            font-size: 11px;

            margin-top: 10px;

        }



        /* -------------------------------------------------------
           PROJECT POPUP
        ------------------------------------------------------- */

        .popup {

            position: fixed;

            inset: 0;

            background: rgba(0,0,0,0.96);

            z-index: 2000;

            display: none;

            overflow-y: auto;

            padding: 80px 6%;

        }


        .popup.active {

            display: block;

        }


        .popup-header {

            display: flex;

            justify-content: space-between;

            align-items: flex-start;

            gap: 30px;

            margin-bottom: 40px;

        }


        .popup-title {

            font-family: "Playfair Display", serif;

            font-size: clamp(40px, 6vw, 75px);

            line-height: 1;

            margin: 10px 0;

        }


        .popup-description {

            color: var(--grey);

            max-width: 700px;

            font-size: 13px;

        }


        .close-popup {

            background: none;

            border: 1px solid var(--line);

            color: var(--gold);

            font-size: 28px;

            width: 45px;

            height: 45px;

            cursor: pointer;

            flex-shrink: 0;

        }


        .close-popup:hover {

            background: var(--gold);

            color: #000;

        }


        .popup-gallery {

            display: grid;

            grid-template-columns: repeat(2, 1fr);

            gap: 15px;

        }


        .popup-gallery img {

            width: 100%;

            aspect-ratio: 16 / 10;

            object-fit: cover;

            cursor: pointer;

        }


        .popup-gallery img:hover {

            opacity: 0.8;

        }



        /* -------------------------------------------------------
           FULLSCREEN IMAGE VIEWER
        ------------------------------------------------------- */

        .image-viewer {

            position: fixed;

            inset: 0;

            background: rgba(0,0,0,0.98);

            z-index: 3000;

            display: none;

            align-items: center;

            justify-content: center;

            padding: 30px;

        }


        .image-viewer.active {

            display: flex;

        }


        .image-viewer img {

            max-width: 95%;

            max-height: 90vh;

            object-fit: contain;

        }


        .viewer-close {

            position: absolute;

            top: 25px;

            right: 35px;

            color: var(--gold);

            font-size: 40px;

            cursor: pointer;

        }



        /* -------------------------------------------------------
           SERVICES
        ------------------------------------------------------- */

        .services {

            display: grid;

            grid-template-columns: repeat(4, 1fr);

            border-top: 1px solid var(--line);

            border-left: 1px solid var(--line);

        }


        .service {

            min-height: 250px;

            padding: 30px;

            border-right: 1px solid var(--line);

            border-bottom: 1px solid var(--line);

            transition: 0.3s;

        }


        .service:hover {

            background: #161616;

        }


        .service-number {

            color: var(--gold);

            font-size: 10px;

            letter-spacing: 2px;

        }


        .service h3 {

            font-family: "Playfair Display", serif;

            font-size: 25px;

            font-weight: 500;

            margin: 60px 0 10px;

        }


        .service p {

            color: var(--grey);

            font-size: 11px;

            line-height: 1.8;

        }



        /* -------------------------------------------------------
           ABOUT / RESUME
        ------------------------------------------------------- */

        .about {

            display: grid;

            grid-template-columns: 0.8fr 1.2fr;

            gap: 100px;

        }


        .about-heading {

            font-family: "Playfair Display", serif;

            font-size: clamp(40px, 5vw, 65px);

            line-height: 1;

        }


        .about-heading span {

            color: var(--gold);

        }


        .about-text {

            color: var(--grey);

            font-size: 13px;

            line-height: 1.9;

        }


        .about-text p {

            margin-bottom: 20px;

        }


        .skills {

            display: flex;

            flex-wrap: wrap;

            gap: 8px;

            margin-top: 25px;

        }


        .skill {

            border: 1px solid var(--line);

            padding: 9px 12px;

            color: #aaa;

            font-size: 9px;

            text-transform: uppercase;

            letter-spacing: 1px;

        }


        .resume-button {

            margin-top: 30px;

        }



        /* -------------------------------------------------------
           WORKFLOW
        ------------------------------------------------------- */

        .workflow {

            display: grid;

            grid-template-columns: repeat(5, 1fr);

            border-top: 1px solid var(--line);

        }


        .step {

            padding: 30px 20px;

            border-right: 1px solid var(--line);

        }


        .step-number {

            color: var(--gold);

            font-size: 10px;

            letter-spacing: 2px;

        }


        .step h3 {

            font-family: "Playfair Display", serif;

            font-size: 22px;

            margin: 30px 0 10px;

            font-weight: 500;

        }


        .step p {

            color: var(--grey);

            font-size: 11px;

            line-height: 1.8;

        }



        /* -------------------------------------------------------
           CONTACT
        ------------------------------------------------------- */

        .contact {

            text-align: center;

            padding: 150px 7%;

            background:

                radial-gradient(

                    circle,

                    rgba(212,175,55,0.09),

                    transparent 35%

                );

        }


        .contact h2 {

            font-family: "Playfair Display", serif;

            font-size: clamp(45px, 7vw, 90px);

            font-weight: 500;

            line-height: 0.95;

            margin: 15px auto 25px;

            max-width: 1000px;

        }


        .contact p {

            max-width: 600px;

            margin: auto;

            color: var(--grey);

            font-size: 13px;

        }


        .contact .buttons {

            justify-content: center;

        }



        /* -------------------------------------------------------
           FOOTER
        ------------------------------------------------------- */

        footer {

            padding: 30px;

            text-align: center;

            color: #666;

            font-size: 10px;

            background: #050505;

        }



        /* -------------------------------------------------------
           WHATSAPP BUTTON
        ------------------------------------------------------- */

        .whatsapp {

            position: fixed;

            right: 20px;

            bottom: 20px;

            width: 52px;

            height: 52px;

            border-radius: 50%;

            background: #25d366;

            display: flex;

            align-items: center;

            justify-content: center;

            font-size: 22px;

            z-index: 1000;

        }



        /* -------------------------------------------------------
           MOBILE
        ------------------------------------------------------- */

        @media (max-width: 900px) {

            nav {

                gap: 12px;

            }


            nav a {

                font-size: 9px;

            }


            .projects {

                grid-template-columns: 1fr;

            }


            .project.large {

                grid-column: auto;

            }


            .services {

                grid-template-columns: repeat(2, 1fr);

            }


            .workflow {

                grid-template-columns: repeat(2, 1fr);

            }


            .about {

                grid-template-columns: 1fr;

                gap: 45px;

            }

        }



        @media (max-width: 600px) {

            header {

                padding: 18px 5%;

            }


            .logo {

                font-size: 19px;

            }


            nav {

                gap: 10px;

            }


            nav a {

                font-size: 8px;

                letter-spacing: 0.5px;

            }


            section {

                padding: 80px 5%;

            }


            .hero-content {

                width: 90%;

                padding-bottom: 70px;

            }


            .hero h1 {

                font-size: 50px;

            }


            .showreel video {

                height: 60vh;

            }


            .projects {

                grid-template-columns: 1fr;

            }


            .project.large {

                grid-column: auto;

            }


            .project-title {

                font-size: 25px;

            }


            .project-overlay {

                padding: 25px;

            }


            .popup {

                padding: 80px 5% 40px;

            }


            .popup-header {

                gap: 15px;

            }


            .popup-gallery {

                grid-template-columns: 1fr;

            }


            .services {

                grid-template-columns: 1fr;

            }


            .workflow {

                grid-template-columns: 1fr;

            }


            .step {

                border-right: 0;

                border-bottom: 1px solid var(--line);

            }


            .contact {

                padding: 110px 5%;

            }

        }

    </style>

</head>



<body>


    <!-- =========================================================
         HEADER
    ========================================================== -->

    <header id="header">

        <div class="logo">

            <a href="#home">SANDESH G.</a>

        </div>


        <nav>

            <a href="#work">Work</a>

            <a href="#showreel">Showreel</a>

            <a href="#about">Resume</a>

            <a href="#contact">Contact</a>

        </nav>

    </header>



    <!-- =========================================================
         HERO
    ========================================================== -->

    <section class="hero" id="home">

        <div class="hero-image">

            <!-- CHANGE YOUR MAIN HERO IMAGE HERE -->

            <img src="RE_01_NB.png"
                 alt="3D Architectural Visualization">

        </div>


        <div class="hero-content">

            <div class="small-title">

                3D Architectural Visualizer

            </div>


            <h1>

                I Create Spaces<br>

                <span>Before They Exist.</span>

            </h1>


            <p class="hero-description">

                I create photorealistic architectural visualizations,

                interior and exterior renders, cinematic walkthroughs,

                and presentation-ready 3D experiences.

            </p>


            <div class="buttons">

                <a href="#work"
                   class="button gold">

                    View My Work

                </a>


                <a href="#showreel"
                   class="button">

                    Watch Showreel

                </a>


                <!-- CHANGE resume.pdf TO YOUR ACTUAL RESUME FILE -->

                <a href="resume.pdf"
                   class="button"
                   target="_blank">

                    View Resume

                </a>

            </div>

        </div>

    </section>



    <!-- =========================================================
         SHOWREEL
    ========================================================== -->

    <section class="showreel" id="showreel">

        <!-- CHANGE vi.mp4 TO YOUR SHOWREEL -->

        <video

            src="vi.mp4"

            autoplay

            muted

            loop

            playsinline>

        </video>


        <div class="showreel-content">

            <div class="small-title">

                Selected Motion Work

            </div>


            <h2>

                Spaces That Move<br>

                Before They Are Built.

            </h2>


            <a href="#work"
               class="button gold">

                Explore My Work

            </a>

        </div>

    </section>



    <!-- =========================================================
         PORTFOLIO
    ========================================================== -->

    <section id="work">

        <div class="section-number">

            01 / Selected Work

        </div>


        <h2 class="section-title">

            Visual Portfolio

        </h2>


        <p class="section-intro">

            A selection of architectural visualization,

            exterior elevations, interiors, cinematic walkthroughs

            and architectural presentation work.

        </p>



        <div class="projects">


            <!-- =================================================
                 PROJECT 01
            ================================================== -->

            <article class="project large"
                     onclick="openProject('villa')">

                <div class="project-image">

                    <img src="RE_01_P1.jpg"
                         alt="Residential Villa">

                    <div class="project-overlay">

                        <div class="project-category">

                            Residential Exterior

                        </div>


                        <div class="project-title">

                            Modern Residential Villa

                        </div>


                        <div class="project-description">

                            Exterior 3D Visualization

                        </div>


                        <div class="project-arrow">

                            View Project →

                        </div>

                    </div>

                </div>

            </article>



            <!-- =================================================
                 PROJECT 02
            ================================================== -->

            <article class="project"
                     onclick="openProject('commercial')">

                <div class="project-image">

                    <img src="CR1.jpg"
                         alt="Commercial Architecture">

                    <div class="project-overlay">

                        <div class="project-category">

                            Commercial

                        </div>


                        <div class="project-title">

                            Convention Center

                        </div>


                        <div class="project-description">

                            Architectural Visualization

                        </div>


                        <div class="project-arrow">

                            View Project →

                        </div>

                    </div>

                </div>

            </article>



            <!-- =================================================
                 PROJECT 03
            ================================================== -->

            <article class="project"
                     onclick="openProject('interior')">

                <div class="project-image">

                    <img src="IDL_201.jpg"
                         alt="Luxury Interior">

                    <div class="project-overlay">

                        <div class="project-category">

                            Interior

                        </div>


                        <div class="project-title">

                            Modern Indian Interior

                        </div>


                        <div class="project-description">

                            Interior Visualization

                        </div>


                        <div class="project-arrow">

                            View Project →

                        </div>

                    </div>

                </div>

            </article>



            <!-- =================================================
                 PROJECT 04
            ================================================== -->

            <article class="project"
                     onclick="openProject('plans')">

                <div class="project-image">

                    <img src="FLOORP0.jpg"
                         alt="Architectural Floor Plan">

                    <div class="project-overlay">

                        <div class="project-category">

                            Planning

                        </div>


                        <div class="project-title">

                            Architectural Planning

                        </div>


                        <div class="project-description">

                            2D Floor Planning & Elevation

                        </div>


                        <div class="project-arrow">

                            View Project →

                        </div>

                    </div>

                </div>

            </article>



            <!-- =================================================
                 PROJECT 05
            ================================================== -->

            <article class="project"
                     onclick="openProject('walkthrough')">

                <div class="project-image">

                    <video

                        src="vi.mp4"

                        autoplay

                        muted

                        loop

                        playsinline>

                    </video>


                    <div class="project-overlay">

                        <div class="project-category">

                            Walkthrough

                        </div>


                        <div class="project-title">

                            Cinematic Architectural Reel

                        </div>


                        <div class="project-description">

                            Architectural Animation

                        </div>


                        <div class="project-arrow">

                            View Reel →

                        </div>

                    </div>

                </div>

            </article>

        </div>

    </section>



    <!-- =========================================================
         SERVICES
    ========================================================== -->

    <section class="dark-section">

        <div class="section-number">

            02 / What I Do

        </div>


        <h2 class="section-title">

            My Expertise

        </h2>


        <p class="section-intro">

            From architectural modeling to final cinematic output,

            I focus on creating accurate and realistic visual

            experiences.

        </p>


        <div class="services">


            <div class="service">

                <div class="service-number">

                    01

                </div>


                <h3>

                    3D Visualization

                </h3>


                <p>

                    Photorealistic architectural renders for

                    residential and commercial projects.

                </p>

            </div>



            <div class="service">

                <div class="service-number">

                    02

                </div>


                <h3>

                    Exterior Design

                </h3>


                <p>

                    Architectural elevations, facade visualization,

                    lighting and material presentation.

                </p>

            </div>



            <div class="service">

                <div class="service-number">

                    03

                </div>


                <h3>

                    Interior Visualization

                </h3>


                <p>

                    Detailed interior modeling, materials,

                    lighting and presentation renders.

                </p>

            </div>



            <div class="service">

                <div class="service-number">

                    04

                </div>


                <h3>

                    Walkthroughs

                </h3>


                <p>

                    Cinematic architectural animations and

                    immersive project presentation reels.

                </p>

            </div>

        </div>

    </section>



    <!-- =========================================================
         WORKFLOW
    ========================================================== -->

    <section>

        <div class="section-number">

            03 / Workflow

        </div>


        <h2 class="section-title">

            From Model to Reality

        </h2>


        <p class="section-intro">

            A simple visualization workflow focused on accuracy,

            realistic materials, lighting and presentation.

        </p>


        <div class="workflow">


            <div class="step">

                <div class="step-number">

                    01

                </div>


                <h3>

                    Model

                </h3>


                <p>

                    Building accurate 3D architectural geometry.

                </p>

            </div>



            <div class="step">

                <div class="step-number">

                    02

                </div>


                <h3>

                    Materials

                </h3>


                <p>

                    Applying realistic PBR materials and textures.

                </p>

            </div>



            <div class="step">

                <div class="step-number">

                    03

                </div>


                <h3>

                    Lighting

                </h3>


                <p>

                    Creating natural and cinematic lighting setups.

                </p>

            </div>



            <div class="step">

                <div class="step-number">

                    04

                </div>


                <h3>

                    Camera

                </h3>


                <p>

                    Establishing strong architectural compositions.

                </p>

            </div>



            <div class="step">

                <div class="step-number">

                    05

                </div>


                <h3>

                    Final

                </h3>


                <p>

                    Delivering high-quality stills and walkthroughs.

                </p>

            </div>

        </div>

    </section>



    <!-- =========================================================
         ABOUT / RESUME
    ========================================================== -->

    <section class="dark-section"
             id="about">

        <div class="section-number">

            04 / About Me

        </div>


        <div class="about">


            <div>

                <h2 class="about-heading">

                    Sandesh<br>

                    <span>Gandhgule.</span>

                </h2>

            </div>



            <div class="about-text">

                <p>

                    I am a 3D Architectural Visualizer focused on

                    transforming architectural concepts into

                    realistic and compelling visual experiences.

                </p>


                <p>

                    My work combines architectural accuracy,

                    realistic materials, lighting, camera composition

                    and cinematic presentation to communicate

                    spaces before they are built.

                </p>


                <p>

                    I work across residential architecture,

                    commercial architecture, interior visualization,

                    exterior elevations and architectural walkthroughs.

                </p>



                <div class="skills">

                    <div class="skill">

                        3D Modeling

                    </div>


                    <div class="skill">

                        Exterior Visualization

                    </div>


                    <div class="skill">

                        Interior Visualization

                    </div>


                    <div class="skill">

                        Architectural Rendering

                    </div>


                    <div class="skill">

                        V-Ray

                    </div>


                    <div class="skill">

                        3ds Max

                    </div>


                    <div class="skill">

                        PBR Materials

                    </div>


                    <div class="skill">

                        Walkthroughs

                    </div>


                    <div class="skill">

                        8K Rendering

                    </div>

                </div>



                <div class="buttons resume-button">

                    <!-- CHANGE resume.pdf TO YOUR RESUME -->

                    <a href="resume.pdf"
                       class="button gold"
                       target="_blank">

                        View / Download Resume

                    </a>

                </div>

            </div>

        </div>

    </section>



    <!-- =========================================================
         CONTACT
    ========================================================== -->

    <section class="contact"
             id="contact">

        <div class="section-number">

            05 / Contact

        </div>


        <h2>

            Let's Visualize<br>

            Your Next Project.

        </h2>


        <p>

            For architectural visualization, interior and exterior

            renders, walkthroughs or 3D presentation work,

            get in touch.

        </p>


        <div class="buttons">


            <!-- REPLACE WITH YOUR ACTUAL WHATSAPP NUMBER -->

            <a href="https://wa.me/919XXXXXXXXX"
               class="button gold"
               target="_blank">

                WhatsApp

            </a>


            <!-- REPLACE WITH YOUR EMAIL -->

            <a href="mailto:your@email.com"
               class="button">

                Email Me

            </a>


            <!-- REPLACE WITH YOUR INSTAGRAM -->

            <a href="https://instagram.com/YOURUSERNAME"
               class="button"
               target="_blank">

                Instagram

            </a>


            <!-- REPLACE WITH YOUR GITHUB -->

            <a href="https://github.com/YOURUSERNAME"
               class="button"
               target="_blank">

                GitHub

            </a>

        </div>

    </section>



    <!-- =========================================================
         FOOTER
    ========================================================== -->

    <footer>

        © 2026 Sandesh Gandhgule — 3D Architectural Visualizer

    </footer>



    <!-- =========================================================
         WHATSAPP FLOATING BUTTON
    ========================================================== -->

    <a href="https://wa.me/919XXXXXXXXX"
       class="whatsapp"
       target="_blank"
       aria-label="WhatsApp">

        💬

    </a>



    <!-- =========================================================
         PROJECT POPUP
         
         You normally DON'T need to edit this section.
         Edit project images in the JAVASCRIPT at the bottom.
    ========================================================== -->

    <div class="popup"
         id="projectPopup">

        <div class="popup-header">

            <div>

                <div class="section-number"
                     id="popupCategory">

                    PROJECT

                </div>


                <h2 class="popup-title"
                    id="popupTitle">

                    Project

                </h2>


                <p class="popup-description"
                   id="popupDescription">

                </p>

            </div>


            <button class="close-popup"
                    onclick="closeProject()">

                ×

            </button>

        </div>


        <div class="popup-gallery"
             id="popupGallery">

        </div>

    </div>



    <!-- =========================================================
         FULLSCREEN IMAGE VIEWER
    ========================================================== -->

    <div class="image-viewer"
         id="imageViewer"
         onclick="closeImageViewer()">

        <div class="viewer-close">

            ×

        </div>


        <img id="viewerImage"
             src=""
             alt="">

    </div>



    <!-- =========================================================
         SIMPLE JAVASCRIPT
    ========================================================== -->

    <script>


        /* =======================================================
           HEADER SCROLL EFFECT
        ======================================================= */

        const header =
            document.getElementById("header");


        window.addEventListener("scroll", function () {

            if (window.scrollY > 40) {

                header.classList.add("scrolled");

            } else {

                header.classList.remove("scrolled");

            }

        });



        /* =======================================================
           PROJECT DATA

           THIS IS THE MAIN AREA YOU WILL EDIT LATER.

           To add another project:
           1. Copy one project block.
           2. Change the name/category/description.
           3. Add your image filenames.
        ======================================================= */


        const projects = {


            /* ---------------------------------------------------
               RESIDENTIAL PROJECT
            --------------------------------------------------- */

            villa: {

                category: "Residential Exterior",

                title: "Modern Residential Villa",

                description:
                    "Exterior architectural visualization showcasing realistic materials, lighting, landscaping and architectural elevation.",

                images: [

                    "RE_01_P1.jpg",

                    "RE_01_F.png",

                    "RE_01_NB.png"

                ]

            },


            /* ---------------------------------------------------
               COMMERCIAL PROJECT
            --------------------------------------------------- */

            commercial: {

                category: "Commercial Architecture",

                title: "Convention Center Complex",

                description:
                    "High-resolution commercial architectural visualization with multiple perspectives and lighting conditions.",

                images: [

                    "CR1.jpg",

                    "CR2.jpg",

                    "CR2n.jpg"

                ]

            },


            /* ---------------------------------------------------
               INTERIOR PROJECT
            --------------------------------------------------- */

            interior: {

                category: "Interior Visualization",

                title: "Modern Indian Kitchen & Living",

                description:
                    "Interior visualization focusing on material detailing, custom furniture, kitchen design and realistic lighting.",

                images: [

                    "IDL_201.jpg",

                    "IDL_202.jpg",

                    "IDL_203.jpg",

                    "IDL_204.jpg"

                ]

            },


            /* ---------------------------------------------------
               PLANNING PROJECT
            --------------------------------------------------- */

            plans: {

                category: "Planning & Elevation",

                title: "Architectural Planning",

                description:
                    "2D architectural planning and elevation presentation.",

                images: [

                    "FLOORP0.jpg",

                    "FLOORP1.jpg"

                ]

            },


            /* ---------------------------------------------------
               WALKTHROUGH
            --------------------------------------------------- */

            walkthrough: {

                category: "Cinematic Walkthrough",

                title: "Architectural Showreel",

                description:
                    "Cinematic architectural animation created for project presentation.",

                images: [

                    "RE_01_P1.jpg"

                ]

            }

        };



        /* =======================================================
           OPEN PROJECT
        ======================================================= */

        function openProject(projectName) {


            const project =
                projects[projectName];


            if (!project) return;


            document.getElementById("popupCategory")
                .textContent =
                project.category;


            document.getElementById("popupTitle")
                .textContent =
                project.title;


            document.getElementById("popupDescription")
                .textContent =
                project.description;


            const gallery =
                document.getElementById("popupGallery");


            gallery.innerHTML = "";


            project.images.forEach(function (image) {


                const img =
                    document.createElement("img");


                img.src = image;


                img.alt = project.title;


                img.loading = "lazy";


                img.onclick = function (event) {

                    event.stopPropagation();

                    openImageViewer(image);

                };


                gallery.appendChild(img);

            });


            document
                .getElementById("projectPopup")
                .classList.add("active");


            document.body.style.overflow = "hidden";

        }



        /* =======================================================
           CLOSE PROJECT
        ======================================================= */

        function closeProject() {

            document
                .getElementById("projectPopup")
                .classList.remove("active");


            document.body.style.overflow = "";

        }



        /* =======================================================
           FULLSCREEN IMAGE
        ======================================================= */

        function openImageViewer(image) {

            document
                .getElementById("viewerImage")
                .src = image;


            document
                .getElementById("imageViewer")
                .classList.add("active");

        }



        /* =======================================================
           CLOSE FULLSCREEN IMAGE
        ======================================================= */

        function closeImageViewer() {

            document
                .getElementById("imageViewer")
                .classList.remove("active");

        }



        /* =======================================================
           ESCAPE KEY
        ======================================================= */

        document.addEventListener("keydown", function(event) {

            if (event.key === "Escape") {

                closeImageViewer();

                closeProject();

            }

        });


    </script>


</body>

</html>
