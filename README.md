<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hasindu Geemina · better UI</title>
    <!-- Font Awesome Icons (free) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Google Font (Inter) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #f9fafb;
            color: #111827;
            padding: 2rem 1.5rem;
            display: flex;
            justify-content: center;
            min-height: 100vh;
        }

        .card {
            max-width: 1100px;
            width: 100%;
            background: white;
            border-radius: 2.5rem;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.15);
            padding: 2.5rem 2.5rem 2rem;
            transition: all 0.2s ease;
        }

        /* header */
        .header {
            text-align: center;
            margin-bottom: 2rem;
        }

        .header h1 {
            font-size: 2.6rem;
            font-weight: 700;
            background: linear-gradient(145deg, #0b1120, #1f2a3f);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: -0.02em;
            margin-bottom: 0.25rem;
        }

        .header h1 i {
            -webkit-text-fill-color: #2563eb;
            background: none;
            margin-right: 6px;
        }

        .header .subhead {
            font-size: 1.2rem;
            font-weight: 400;
            color: #4b5563;
            background: #eef2ff;
            display: inline-block;
            padding: 0.35rem 1.6rem;
            border-radius: 40px;
            letter-spacing: -0.01em;
            border: 1px solid #dbeafe;
            backdrop-filter: blur(2px);
        }

        .profile-stats {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1.2rem 2rem;
            margin-top: 1.2rem;
            font-size: 0.95rem;
            color: #1e293b;
        }

        .profile-stats a {
            color: #1e293b;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            background: #f1f5f9;
            padding: 0.2rem 1rem;
            border-radius: 30px;
            transition: 0.2s;
            font-weight: 500;
        }

        .profile-stats a i {
            color: #2563eb;
            font-size: 1rem;
        }

        .profile-stats a:hover {
            background: #dbeafe;
            color: #1e3a8a;
            transform: translateY(-2px);
        }

        .trophy-wrapper {
            display: flex;
            justify-content: center;
            margin: 1.8rem 0 1.2rem;
        }

        .trophy-wrapper img {
            max-width: 100%;
            height: auto;
            border-radius: 1rem;
            box-shadow: 0 8px 20px rgba(0,0,0,0.02);
            background: #f8fafc;
            padding: 6px 12px;
        }

        .section-title {
            font-weight: 600;
            font-size: 1.3rem;
            margin: 2rem 0 1.2rem;
            color: #0f172a;
            display: flex;
            align-items: center;
            gap: 8px;
            border-bottom: 2px solid #e9edf2;
            padding-bottom: 0.6rem;
        }

        .section-title i {
            color: #2563eb;
            font-size: 1.3rem;
        }

        .connect-links {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem 1.2rem;
            margin-bottom: 0.5rem;
        }

        .connect-links a {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: #f1f5f9;
            padding: 0.6rem 1.5rem;
            border-radius: 60px;
            color: #0b1120;
            text-decoration: none;
            font-weight: 500;
            transition: 0.2s;
            border: 1px solid transparent;
        }

        .connect-links a i {
            font-size: 1.4rem;
            color: #2563eb;
        }

        .connect-links a:hover {
            background: #e0e7ff;
            border-color: #93b4fc;
            transform: scale(1.02);
            box-shadow: 0 4px 10px rgba(37, 99, 235, 0.08);
        }

        .lang-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem 1rem;
            margin: 0.5rem 0 0.2rem;
        }

        .lang-item {
            background: #f8fafc;
            border-radius: 40px;
            padding: 0.4rem 1rem 0.4rem 0.8rem;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            border: 1px solid #e9edf2;
            transition: 0.15s;
            font-weight: 450;
            font-size: 0.9rem;
            box-shadow: 0 1px 2px rgba(0,0,0,0.02);
        }

        .lang-item img {
            width: 28px;
            height: 28px;
            object-fit: contain;
        }

        .lang-item:hover {
            background: white;
            border-color: #b9c8f0;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.02);
        }

        .support-row {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 1.2rem 2.5rem;
            background: #fafcff;
            padding: 1rem 1.6rem;
            border-radius: 60px;
            margin-top: 1rem;
            border: 1px solid #e4e9f2;
        }

        .support-row a {
            display: inline-block;
            transition: 0.2s;
        }

        .support-row a:hover {
            transform: scale(1.02) translateY(-2px);
            filter: brightness(1.02);
        }

        .support-row img {
            height: 44px;
            width: auto;
        }

        .top-langs {
            margin: 2rem 0 0.4rem;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 1.8rem;
            background: #fcfdff;
            border-radius: 2rem;
            padding: 1.2rem 1.8rem;
            border: 1px solid #e9edf2;
        }

        .top-langs img {
            max-width: 100%;
            height: auto;
            border-radius: 14px;
            box-shadow: 0 6px 14px rgba(0,0,0,0.02);
        }

        .top-langs .stats-text {
            font-weight: 500;
            color: #1f2937;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .top-langs .stats-text i {
            color: #2563eb;
        }

        hr {
            border: none;
            border-top: 2px dashed #dce2ec;
            margin: 1.6rem 0 0.8rem;
        }

        .footer-meta {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            font-size: 0.85rem;
            color: #64748b;
            margin-top: 1.4rem;
        }

        .badge-pill {
            background: #eef2ff;
            padding: 0.2rem 1rem;
            border-radius: 30px;
            color: #1e3a8a;
            font-weight: 500;
            font-size: 0.8rem;
            display: inline-flex;
            align-items: center;
            gap: 6px;
        }

        /* responsive */
        @media (max-width: 700px) {
            .card { padding: 1.5rem; }
            .header h1 { font-size: 2rem; }
            .lang-grid { gap: 0.5rem; }
            .support-row { flex-direction: column; align-items: flex-start; border-radius: 28px; }
            .top-langs { flex-direction: column; align-items: stretch; }
        }

        /* custom scroll */
        ::-webkit-scrollbar { width: 6px; }
        ::-webkit-scrollbar-track { background: #f1f5f9; }
        ::-webkit-scrollbar-thumb { background: #bbc8e0; border-radius: 10px; }
    </style>
</head>
<body>
<div class="card">

    <!-- HEADER -->
    <div class="header">
        <h1>
            <i class="fas fa-code"></i> Hi 👋, I'm Hasindu Geemina Wijeweera
        </h1>
        <div class="subhead">
            <i class="fas fa-laptop-code" style="margin-right: 8px;"></i> passionate frontend fullstack developer · Sri Lanka
        </div>

        <!-- profile views & trophy shortcut -->
        <div class="profile-stats">
            <a href="#"><i class="fas fa-eye"></i> Profile views: 1.2k</a>
            <a href="#"><i class="fas fa-trophy"></i> GitHub trophies</a>
            <a href="#"><i class="fas fa-comment-dots"></i> Ask me about <strong>student</strong></a>
        </div>
    </div>

    <!-- TROPHY (replaces the original trophy image) -->
    <div class="trophy-wrapper">
        <img src="https://github-profile-trophy.vercel.app/?username=hasidu0023&theme=flat&no-frame=true&margin-w=8" alt="trophies" />
    </div>

    <!-- CONNECT WITH ME -->
    <div class="section-title">
        <i class="fas fa-share-alt"></i> Connect with me
    </div>
    <div class="connect-links">
        <a href="#" target="_blank"><i class="fab fa-youtube"></i> YouTube · Hasindu Geemina</a>
        <a href="#"><i class="fab fa-github"></i> GitHub</a>
        <a href="#"><i class="fab fa-linkedin"></i> LinkedIn</a>
        <a href="#"><i class="fab fa-twitter"></i> Twitter</a>
        <a href="#"><i class="fab fa-dev"></i> Dev.to</a>
    </div>

    <!-- LANGUAGES & TOOLS (better grid) -->
    <div class="section-title" style="margin-top: 2.2rem;">
        <i class="fas fa-cogs"></i> Languages & Tools
    </div>
    <div class="lang-grid">
        <!-- using inline SVG / icon replacement for a cleaner look – we use original icons but with a nicer display -->
        <span class="lang-item"><img src="https://docs.amplify.aws/assets/logo-dark.svg" width="28" alt="amplify"> Amplify</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/android/android-original-wordmark.svg" width="28" alt="android"> Android</span>
        <span class="lang-item"><img src="https://angular.io/assets/images/logos/angular/angular.svg" width="28" alt="angular"> Angular</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/angularjs/angularjs-original-wordmark.svg" width="28" alt="angularjs"> AngularJS</span>
        <span class="lang-item"><img src="https://cdn.worldvectorlogo.com/logos/arduino-1.svg" width="28" alt="arduino"> Arduino</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" width="28" alt="aws"> AWS</span>
        <span class="lang-item"><img src="https://download.blender.org/branding/community/blender_community_badge_white.svg" width="28" alt="blender"> Blender</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bootstrap/bootstrap-plain-wordmark.svg" width="28" alt="bootstrap"> Bootstrap</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" width="28" alt="c"> C</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/coffeescript/coffeescript-original-wordmark.svg" width="28" alt="coffee"> CoffeeScript</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" width="28" alt="cpp"> C++</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg" width="28" alt="csharp"> C#</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" width="28" alt="css3"> CSS3</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/d3js/d3js-original.svg" width="28" alt="d3"> D3</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/dartlang/dartlang-icon.svg" width="28" alt="dart"> Dart</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" width="28" alt="docker"> Docker</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/dot-net/dot-net-original-wordmark.svg" width="28" alt="dotnet"> .NET</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/electron/electron-original.svg" width="28" alt="electron"> Electron</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original-wordmark.svg" width="28" alt="express"> Express</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/figma/figma-icon.svg" width="28" alt="figma"> Figma</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg" width="28" alt="firebase"> Firebase</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/flutterio/flutterio-icon.svg" width="28" alt="flutter"> Flutter</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/framer/framer-icon.svg" width="28" alt="framer"> Framer</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/gatsbyjs/gatsbyjs-icon.svg" width="28" alt="gatsby"> Gatsby</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/google_cloud/google_cloud-icon.svg" width="28" alt="gcp"> GCP</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" width="28" alt="git"> Git</span>
        <span class="lang-item"><img src="https://upload.wikimedia.org/wikipedia/commons/1/1c/Haskell-Logo.svg" width="28" alt="haskell"> Haskell</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/hexoio/hexoio-icon.svg" width="28" alt="hexo"> Hexo</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/apache_hive/apache_hive-icon.svg" width="28" alt="hive"> Hive</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" width="28" alt="html5"> HTML5</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/adobe_illustrator/adobe_illustrator-icon.svg" width="28" alt="illustrator"> Illustrator</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/invisionapp/invisionapp-icon.svg" width="28" alt="invision"> InVision</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/jasmine/jasmine-icon.svg" width="28" alt="jasmine"> Jasmine</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" width="28" alt="java"> Java</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" width="28" alt="javascript"> JS</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/jestjsio/jestjsio-icon.svg" width="28" alt="jest"> Jest</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/apache_kafka/apache_kafka-icon.svg" width="28" alt="kafka"> Kafka</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/elasticco_kibana/elasticco_kibana-icon.svg" width="28" alt="kibana"> Kibana</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/kotlinlang/kotlinlang-icon.svg" width="28" alt="kotlin"> Kotlin</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/kubernetes/kubernetes-icon.svg" width="28" alt="kubernetes"> K8s</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/laravel/laravel-plain-wordmark.svg" width="28" alt="laravel"> Laravel</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" width="28" alt="linux"> Linux</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/mariadb/mariadb-icon.svg" width="28" alt="mariadb"> MariaDB</span>
        <span class="lang-item"><img src="https://upload.wikimedia.org/wikipedia/commons/2/21/Matlab_Logo.png" width="28" alt="matlab"> Matlab</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/mochajs/mochajs-icon.svg" width="28" alt="mocha"> Mocha</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" width="28" alt="mongodb"> MongoDB</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" width="28" alt="mysql"> MySQL</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nginx/nginx-original.svg" width="28" alt="nginx"> Nginx</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" width="28" alt="nodejs"> Node.js</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/nuxtjs/nuxtjs-icon.svg" width="28" alt="nuxtjs"> Nuxt</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/opencv/opencv-icon.svg" width="28" alt="opencv"> OpenCV</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/oracle/oracle-original.svg" width="28" alt="oracle"> Oracle</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" width="28" alt="pandas"> Pandas</span>
        <span class="lang-item"><img src="https://api.iconify.design/logos-perl.svg" width="28" alt="perl"> Perl</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/photoshop/photoshop-line.svg" width="28" alt="ps"> Photoshop</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg" width="28" alt="php"> PHP</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" width="28" alt="postgres"> PostgreSQL</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/getpostman/getpostman-icon.svg" width="28" alt="postman"> Postman</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" width="28" alt="python"> Python</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" width="28" alt="react"> React</span>
        <span class="lang-item"><img src="https://reactnative.dev/img/header_logo.svg" width="28" alt="reactnative"> React Native</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/redis/redis-original-wordmark.svg" width="28" alt="redis"> Redis</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/scala/scala-original.svg" width="28" alt="scala"> Scala</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/scullyio/scully/main/assets/logos/SVG/scullyio-icon.svg" width="28" alt="scully"> Scully</span>
        <span class="lang-item"><img src="https://gist.githubusercontent.com/vivek32ta/c7f7bf583c1fb1c58d89301ea40f37fd/raw/1782aef8672484698c0dd407f900c4a329ed5bc4/sculpin.svg" width="28" alt="sculpin"> Sculpin</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/sketchapp/sketchapp-icon.svg" width="28" alt="sketch"> Sketch</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/springio/springio-icon.svg" width="28" alt="spring"> Spring</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/sqlite/sqlite-icon.svg" width="28" alt="sqlite"> SQLite</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/swift/swift-original.svg" width="28" alt="swift"> Swift</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/unity3d/unity3d-icon.svg" width="28" alt="unity"> Unity</span>
        <span class="lang-item"><img src="https://www.vectorlogo.zone/logos/vagrantup/vagrantup-icon.svg" width="28" alt="vagrant"> Vagrant</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vuejs/vuejs-original-wordmark.svg" width="28" alt="vuejs"> Vue</span>
        <span class="lang-item"><img src="https://raw.githubusercontent.com/detain/svg-logos/780f25886640cef088af994181646db2f6b1a3f8/svg/xamarin.svg" width="28" alt="xamarin"> Xamarin</span>
    </div>

    <!-- SUPPORT -->
    <div class="section-title" style="margin-top: 2rem;">
        <i class="fas fa-hand-holding-heart"></i> Support
    </div>
    <div class="support-row">
        <a href="#"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy me a coffee" style="height:46px;"></a>
        <a href="#"><img src="https://cdn.ko-fi.com/cdn/kofi3.png?v=3" alt="Ko-fi" style="height:46px;"></a>
        <span class="badge-pill"><i class="fas fa-heart" style="color:#ef4444;"></i> Hasidu0023 · 456666</span>
    </div>

    <!-- TOP LANGUAGES -->
    <div class="top-langs">
        <div class="stats-text">
            <i class="fas fa-chart-pie"></i> Most used languages
        </div>
        <img src="https://github-readme-stats.vercel.app/api/top-langs?username=hasidu0023&show_icons=true&locale=en&layout=compact&hide_border=true&bg_color=fcfdff&title_color=1f2a3f&text_color=334155" alt="top languages" style="max-width:100%;">
    </div>

    <hr>

    <div class="footer-meta">
        <span><i class="far fa-calendar-alt"></i> 2026 · crafted with <i class="fas fa-heart" style="color:#dc2626;"></i></span>
        <span><i class="fas fa-code-branch"></i> hasindu0023 / README</span>
    </div>

</div>
</body>
</html>
