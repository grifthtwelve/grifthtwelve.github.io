<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@200..700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@200..700&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
    <style>
        html {
            scroll-behavior: smooth;
        }

        /* Estilos CSS para el contenedor principal */
        .portfolio-container {
            position: relative;
            text-align: center;
            margin: 0;
            padding: 0;
            min-height: 100vh;
        }

        /* Estilos CSS para el texto CONTACT */
        .staytunned {
            position: absolute;
            top: 351.5%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #fff;
            font-size: 160px;
            font-family: 'Oswald';
            z-index: 3;
            font-weight: 350; /* Puedes ajustar el peso de la fuente según tus necesidades */
        }

        /* Estilos CSS para el texto principal (MARIO OLAYA) */
        .portfolio-text {
            position: absolute;
            top: 28.5%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #fff;
            font-size: 176px;
            font-family: 'Oswald'; /* Usar 'Oswald' como la fuente */
            z-index: 1;
            letter-spacing: 6px;
            font-weight: 400; /* Puedes ajustar el peso de la fuente según tus necesidades */
        }

        /* Estilos CSS para el texto adicional (PROGRAMMER - GAME DEVELOPER - WEB DEVELOPER) */
        .developer-text {
            position: absolute;
            top: 58.5%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #fff;
            font-size: 20px;
            font-family: 'Poppins';
            z-index: 1;
            font-weight: 400; /* Puedes ajustar el peso de la fuente según tus necesidades */
        }

        /* Estilos CSS para el texto dentro de About Me */
        .developer-text2 {
            position: absolute;
            top: 120.5%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #fff;
            font-size: 20px;
            font-family: 'Poppins';
            z-index: 3;
            font-weight: 400; /* Puedes ajustar el peso de la fuente según tus necesidades */
        }

        /* Estilos CSS para las imágenes */
        .portfolio-image, .additional-image, .overlay-image, .vv-image, .settings-image, .close-image {
            user-drag: none;
            -webkit-user-drag: none;
        }

        .portfolio-image {
            display: block;
            margin: 0;
            padding: 0;
            width: 100vw;
            height: 100vh;
            object-fit: cover;
            clip-path: polygon(0 0, 100% 0, 100% 85%, 0 85%);
            top: 0;
            z-index: 0;
        }

        /* Estilo para la imagen backgru3.jpg */
        .portfolio-image-2 {
            display: block;
            margin: 0;
            padding: 0;
            width: 100vw;
            height: 100vh;
            object-fit: cover;
            position: absolute;
            clip-path: polygon(0 0, 100% 0, 100% 85%, 0 85%);
            top: 170%; /* Ajusta esta propiedad según tus necesidades */
            z-index: 0;
        }

        /* Estilo para la imagen backgru4.jpg */
        .portfolio-image-3 {
            display: block;
            margin: 0;
            padding: 0;
            width: 100vw;
            height: 100vh;
            object-fit: cover;
            position: absolute;
            clip-path: polygon(0 0, 100% 0, 100% 85%, 0 85%);
            top: 255%; /* Ajusta esta propiedad según tus necesidades */
            z-index: 0;
        }

        /* Estilo para la imagen de fondo adicional */
        .additional-image {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            object-fit: cover;
            z-index: -1;
        }

        /* Estilos CSS para la imagen vv.png */
        .vv-image {
            position: absolute;
            top: 66.5%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 2;
            width: 13px;
            height: auto;
            cursor: pointer;
        }

        /* Estilos CSS para el rectángulo gris */
        .gray-rectangle {
            position: fixed;
            top: -23.33%;
            left: 0;
            width: 100%;
            height: 23.33%;
            background-color: rgb(25, 25, 25);
            z-index: 4;
            transition: top 0.5s ease-in-out;
        }

        .gray-rectangle.show {
            top: 0;
        }

        /* Estilos CSS para las palabras */
        .nav-words {
            position: absolute;
            bottom: 75px;
            width: 100%;
            text-align: center;
            color: white;
            font-family: 'Poppins';
            font-size: 24px;
            z-index: 4;
            font-weight: 300; /* Puedes ajustar el peso de la fuente según tus necesidades */
        }

                /* Estilos CSS para las palabras sociales */
                .nav-wordssocial {
            position: absolute;
            top: 370%;
            width: 100%;
            text-align: center;
            color: white;
            font-family: 'Poppins';
            font-size: 30px;
            z-index: 5;
            font-weight: 300; /* Puedes ajustar el peso de la fuente según tus necesidades */
        }

.nav-wordssocial span {
    margin: 0 45px; /* 30px total separation between words */
}

        .nav-word {
            cursor: pointer;
            margin: 0 25px;
        }

        /* Añadir un margen al cuerpo */
        body {
            margin: 0;
            background-color: black;
            overflow-x: hidden; /* Evita la barra de desplazamiento horizontal */
        }

        /* Estilos CSS para la imagen de ajustes y la equis */
        .settings-image, .close-image {
            position: fixed;
            top: 4%;
            right: 6%;
            z-index: 8;
            width: 33px;
            height: auto;
            cursor: pointer;
            transition: opacity 0.5s ease-in-out;
        }

        .close-image {
            display: none;
        }

        /* Estilos CSS para la imagen sobrepuesta Drawing.png */
        .overlay-image {
            position: absolute;
            bottom: 18%;
            right: 0;
            z-index: 2;
            width: 125px;
            height: 100px;
        }

        /* Estilos CSS para el texto (ABOUT) */
        .About-text {
            position: absolute;
            top: 110.5%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #fff;
            font-size: 170px;
            font-family: 'Oswald';
            z-index: 1;
            transition: opacity 0.5s ease-in-out;
            font-weight: 400; /* Puedes ajustar el peso de la fuente según tus necesidades */
        }

        /* Estilos CSS para el texto (GALLERY) */
        .Gallery-text {
            position: absolute;
            top: 189.8%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #fff;
            font-size: 170px;
            font-family: 'Oswald';
            z-index: 1;
            transition: opacity 0.5s ease-in-out;
            font-weight: 400; /* Puedes ajustar el peso de la fuente según tus necesidades */
        }

        /* Estilos CSS para el texto (PROJECTS) */
        .Projects-text {
            position: absolute;
            top: 269.1%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #fff;
            font-size: 170px;
            font-family: 'Oswald';
            z-index: 1;
            transition: opacity 0.5s ease-in-out;
            font-weight: 400; /* Puedes ajustar el peso de la fuente según tus necesidades */
        }

        /* Estilos CSS para la imagen plus.png */
        .plus-image {
            position: absolute;
            top: 144.5%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 3;
            width: 40px;
            height: auto;
            cursor: pointer;
            transition: opacity 0.3s ease-in-out;
        }

        /* Estilos CSS para la imagen circle.png */
        .circle-image {
            position: absolute;
            top: 144.5%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 3;
            width: 40px;
            height: auto;
            cursor: pointer;
            transition: opacity 0.3s ease-in-out;
            opacity: 0; /* Ocultar inicialmente */
        }

        /* Estilos CSS para la imagen plus.png debajo de GALLERY */
        .plus-image-gallery {
            position: absolute;
            top: 229.5%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 3;
            width: 40px;
            height: auto;
            cursor: pointer;
            transition: opacity 0.3s ease-in-out;
        }

        /* Estilos CSS para la imagen circle.png debajo de GALLERY */
        .circle-image-gallery {
            position: absolute;
            top: 229.5%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 3;
            width: 40px;
            height: auto;
            cursor: pointer;
            transition: opacity 0.3s ease-in-out;
            opacity: 0; /* Ocultar inicialmente */
        }

        /* Estilos CSS para la imagen plus.png debajo de PROJECTS */
        .plus-image-projects {
            position: absolute;
            top: 314.5%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 3;
            width: 40px;
            height: auto;
            cursor: pointer;
            transition: opacity 0.3s ease-in-out;
        }

        /* Estilos CSS para la imagen circle.png debajo de PROJECTS */
        .circle-image-projects {
            position: absolute;
            top: 314.5%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 3;
            width: 40px;
            height: auto;
            cursor: pointer;
            transition: opacity 0.3s ease-in-out;
            opacity: 0; /* Ocultar inicialmente */
        }

        /* Estilos CSS para el rectángulo gris adicional */
        .additional-gray-rectangle {
            position: absolute;
            top: 85%;
            left: 0;
            width: 100%;
            height: 85%;
            background-color: rgba(25, 25, 25, 0.7);
            z-index: 2;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
        }

        .additional-gray-rectangle.show {
            opacity: 1;
        }

        /* Estilos CSS para el rectángulo gris adicional debajo de GALLERY */
        .additional-gray-rectangle-gallery {
            position: absolute;
            top: 170%;
            left: 0;
            width: 100%;
            height: 85%;
            background-color: rgba(25, 25, 25, 0.7);
            z-index: 2;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
        }

        .additional-gray-rectangle-gallery.show {
            opacity: 1;
        }

        /* Estilos CSS para el rectángulo gris adicional debajo de PROJECTS */
        .additional-gray-rectangle-projects {
            position: absolute;
            top: 255%;
            left: 0;
            width: 100%;
            height: 85%;
            background-color: rgba(25, 25, 25, 0.7);
            z-index: 2;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
        }

        .additional-gray-rectangle-projects.show {
            opacity: 1;
        }

        /* Estilos CSS para el rectángulo gris de contact */
        .additional-gray-rectangle-contact {
            position: absolute;
            top: 340%;
            left: 0;
            width: 100%;
            height: 40%;
            background-color: rgba(25, 25, 25);
            z-index: 2;
            opacity: 1;
        }

        /* Estilos CSS para la linea de contact */
        .contactline {
        position: absolute;
         top: 365%;
         left: 0;
         width: 100%;
         height: 0.1%;
         background-color: rgb(255, 255, 255);
         z-index: 4;
         opacity: 1;
        }

        /* Media Queries para ajustar el diseño en diferentes tamaños de pantalla */
        @media (max-width: 768px) {
            .portfolio-text {
                font-size: 24vw;
            }

            .Gallery-text {
                font-size: 30vw;
            }

            .Projects-text {
                font-size: 26.5vw;
            }

            .developer-text {
                font-size: 3vw;
            }

            .settings-image {
                width: 1vw;
            }

            .nav-words {
                font-size: 4vw;
            }

            .nav-wordssocial {
                font-size: 4vw;
            }

            .nav-word {
                margin: 0 10px;
            }

            .vv-image {
                width: 3vw;
            }

            .settings-image {
                width: 6vw;
            }
            .close-image {
                width: 4vw;
            }

            .overlay-image {
                width: 20vw;
            }
            .gray-rectangle {
                height: 35vw;
            }
            .staytunned {
                font-size: 25vw;
            }

        }
    </style>
</head>
<body>
    <img class="additional-image" src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/Backgru2.jpg" draggable="false">
    <div class="portfolio-container">
        <h0 class="staytunned">CONTACT</h0>
        <h1 class="portfolio-text">MARIO OLAYA</h1>
        <h2 class="developer-text">PROGRAMMER - GAME DEVELOPER - WEB DEVELOPER</h2>
        <h3 id="aboutSection" class="About-text">ABOUT</h3>
        <h4 id="GallerySection" class="Gallery-text">GALLERY</h4>
        <h5 id="ProjectsSection" class="Projects-text">PROJECTS</h5>
        <h6 class="developer-text2" id="developerText2" style="max-width: 100%; opacity: 0; transition: opacity 0.5s;"><strong>About Me</strong><br><br>Hello! I am Mario, someone passionate and creative with a great taste for web design, programming and graphic design. Since I began to delve into this world, I felt identified with it, because it is quite interesting and offers us many possibilities to expand our knowledge about our businesses and ideas through the digital world.<br><br><strong>What I do?</strong><br>Web Development: I specialize in creating responsive, visually appealing websites that provide the best user experience. I want to include on this page a variety of projects, from personal to complex commerce platforms, and thus show my clients examples and a clear and realistic vision of how their page could look.<br><br>Thank you for being interested in knowing more about me, I hope you have a good experience with me. :)</h6>
        <img class="portfolio-image" src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/Backgru.jpg"  draggable="false">
        <img class="portfolio-image-2" src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/Backgru3.jpg"  draggable="false">
        <img class="portfolio-image-3" src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/Backgru5.jpg" draggable="false">
        <img class="overlay-image" src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/Drawing.png" draggable="false">
        <img class="vv-image" src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/vv.png" alt="Imagen vv" onclick="scrollToAbout()" draggable="false">
        <img class="circle-image" src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/Circle.png" alt="Imagen circle" id="circleImage" draggable="false">
        <img class="plus-image" src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/plus.png" alt="Imagen plus" id="plusImage" onclick="toggleAdditionalGrayRectangle()" draggable="false">
        <img class="circle-image-gallery" src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/Circle.png" alt="Imagen circle" id="circleImageGallery" draggable="false">
        <img class="plus-image-gallery" src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/plus.png" alt="Imagen plus" id="plusImageGallery" onclick="toggleAdditionalGrayRectangleGallery()" draggable="false">
        <img class="circle-image-projects" src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/Circle.png" alt="Imagen circle" id="circleImageProjects" draggable="false">
        <img class="plus-image-projects" src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/plus.png" alt="Imagen plus" id="plusImageProjects" onclick="toggleAdditionalGrayRectangleProjects()" draggable="false">
        <img class="settings-image" src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/SettingsWeb.png" alt="Imagen de ajustes" onclick="toggleRectangle()" draggable="false">
        <img class="close-image" src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/equis.png" alt="Imagen de cerrar" onclick="toggleRectangle()" draggable="false">
        <div class="additional-gray-rectangle" id="additionalGrayRectangle"></div>
        <div class="additional-gray-rectangle-gallery" id="additionalGrayRectangleGallery"></div>
        <div class="additional-gray-rectangle-projects" id="additionalGrayRectangleProjects"></div>
        <div class="additional-gray-rectangle-contact" id="additionalGrayRectanglecontact"></div>
        <div class="contactline"></div>
        <div class="gray-rectangle" id="grayRectangle">
            <div class="nav-words">
                <span class="nav-word" onclick="scrollToTop()">HOME</span>
                <span class="nav-word about" onclick="scrollToAbout()">ABOUT</span>
                <span class="nav-word gallery" onclick="scrollToGallery()">GALLERY</span>
                <span class="nav-word projects" onclick="scrollToProjects()">PROJECTS</span>
                <span class="nav-word" onclick="scrollToContact()">CONTACT</span>
            </div>
        </div>
    </div>
    <div class="nav-wordssocial">
        <span class="nav-word" onclick="window.open('https://www.instagram.com/grifthcode/', '_blank')">
            <img src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/instagram.png" alt="Instagram" style="vertical-align: middle; width: 30px; height: 30px; margin-right: 10px;" draggable="false">
            INSTAGRAM
        </span>
        <span class="nav-word" onclick="window.open('https://www.facebook.com/profile.php?id=61561032840288', '_blank')">
            <img src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/facebook.png" alt="Facebook" style="vertical-align: middle; width: 45px; height: 45px; margin-right: 10px;" draggable="false">
            FACEBOOK
        </span>
        <span class="nav-word" onclick="window.open('https://x.com/GrifthCode', '_blank')">
            <img src="https://raw.githubusercontent.com/grifthtwelve/Repository/main/gmail.png" alt="Gmail" style="vertical-align: middle; width: 30px; height: 30px; margin-right: 10px;" draggable="false">
            TWITTER
        </span>
    </div>
    <script>
        function toggleRectangle() {
            var rectangle = document.getElementById('grayRectangle');
            var settingsImage = document.querySelector('.settings-image');
            var closeImage = document.querySelector('.close-image');

            rectangle.classList.toggle('show');
            if (rectangle.classList.contains('show')) {
                settingsImage.style.opacity = '0';
                closeImage.style.opacity = '1';
                setTimeout(function() {
                    settingsImage.style.display = 'none';
                    closeImage.style.display = 'block';
                }, 250);
            } else {
                closeImage.style.opacity = '0';
                settingsImage.style.opacity = '1';
                setTimeout(function() {
                    closeImage.style.display = 'none';
                    settingsImage.style.display = 'block';
                }, 250);
            }
        }

        function showCircle() {
            var circleImage = document.querySelector('.circle-image');
            var plusImage = document.querySelector('.plus-image');
            circleImage.style.opacity = '1';
            plusImage.style.opacity = '1';
        }

        function hideCircle() {
            var circleImage = document.querySelector('.circle-image');
            var plusImage = document.querySelector('.plus-image');
            circleImage.style.opacity = '0';
            plusImage.style.opacity = '1';
        }

        function showCircleGallery() {
            var circleImageGallery = document.querySelector('.circle-image-gallery');
            var plusImageGallery = document.querySelector('.plus-image-gallery');
            circleImageGallery.style.opacity = '1';
            plusImageGallery.style.opacity = '1';
        }

        function hideCircleGallery() {
            var circleImageGallery = document.querySelector('.circle-image-gallery');
            var plusImageGallery = document.querySelector('.plus-image-gallery');
            circleImageGallery.style.opacity = '0';
            plusImageGallery.style.opacity = '1';
        }

        function showCircleProjects() {
            var circleImageProjects = document.querySelector('.circle-image-projects');
            var plusImageProjects = document.querySelector('.plus-image-projects');
            circleImageProjects.style.opacity = '1';
            plusImageProjects.style.opacity = '1';
        }

        function hideCircleProjects() {
            var circleImageProjects = document.querySelector('.circle-image-projects');
            var plusImageProjects = document.querySelector('.plus-image-projects');
            circleImageProjects.style.opacity = '0';
            plusImageProjects.style.opacity = '1';
        }

        function scrollToTop() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        }

        function scrollToAbout() {
            var aboutSection = document.getElementById('aboutSection');
            var aboutPosition = aboutSection.offsetTop - (window.innerHeight / 1.7) + (aboutSection.offsetHeight / 1.7);
            window.scrollTo({
                top: aboutPosition,
                behavior: 'smooth'
            });
        }

        function scrollToGallery() {
            var gallerySection = document.getElementById('GallerySection');
            var galleryPosition = gallerySection.offsetTop - (window.innerHeight / 1.7) + (gallerySection.offsetHeight / 1.7);
            window.scrollTo({
                top: galleryPosition,
                behavior: 'smooth'
            });
        }

        function scrollToProjects() {
            var projectsSection = document.getElementById('ProjectsSection');
            var projectsPosition = projectsSection.offsetTop - (window.innerHeight / 1.7) + (projectsSection.offsetHeight / 1.7);
            window.scrollTo({
                top: projectsPosition,
                behavior: 'smooth'
            });
        }

        function scrollToContact() {
            window.scrollTo({
                top: document.body.scrollHeight,
                behavior: 'smooth'
            });
        }

        document.addEventListener('DOMContentLoaded', function() {
            var plusImage = document.querySelector('.plus-image');
            plusImage.addEventListener('mouseover', showCircle);
            plusImage.addEventListener('mouseout', hideCircle);

            var plusImageGallery = document.querySelector('.plus-image-gallery');
            plusImageGallery.addEventListener('mouseover', showCircleGallery);
            plusImageGallery.addEventListener('mouseout', hideCircleGallery);

            var plusImageProjects = document.querySelector('.plus-image-projects');
            plusImageProjects.addEventListener('mouseover', showCircleProjects);
            plusImageProjects.addEventListener('mouseout', hideCircleProjects);
        });

        const aboutText = document.getElementById('aboutSection');
        const developerText2 = document.getElementById('developerText2');
        function toggleAdditionalGrayRectangle() {
            var grayRectangle = document.getElementById('additionalGrayRectangle');
            var circleImage = document.getElementById('circleImage');
            var plusImage = document.getElementById('plusImage');
            if (grayRectangle.classList.contains('show')) {
                grayRectangle.classList.remove('show');
                circleImage.style.opacity = 0;
                aboutText.style.opacity = 1;
                developerText2.style.opacity = 0;
                circleImage.style.transition = 'transform 0.5s';
                plusImage.style.transition = 'transform 0.5s';
                circleImage.style.transform = 'translateY(0) translateX(-50%)';
                plusImage.style.transform = 'translateY(0) translateX(-50%)';
                circleImage.src = 'https://raw.githubusercontent.com/grifthtwelve/Repository/main/Circle.png';
                plusImage.src = 'https://raw.githubusercontent.com/grifthtwelve/Repository/main/plus.png';
            } else {
                grayRectangle.classList.add('show');
                circleImage.style.opacity = 1;
                aboutText.style.opacity = 0;
                developerText2.style.opacity = 1;
                circleImage.style.transition = 'transform 0.5s';
                plusImage.style.transition = 'transform 0.5s';
                circleImage.style.transform = 'translateY(60px) translateX(-50%)';
                plusImage.style.transform = 'translateY(60px) translateX(-50%)';
                circleImage.src = 'https://raw.githubusercontent.com/grifthtwelve/Repository/main/Circle2.png';
                plusImage.src = 'https://raw.githubusercontent.com/grifthtwelve/Repository/main/minus.png';
            }
        }

        const galleryText = document.getElementById('GallerySection');
        function toggleAdditionalGrayRectangleGallery() {
            var grayRectangleGallery = document.getElementById('additionalGrayRectangleGallery');
            var circleImageGallery = document.getElementById('circleImageGallery');
            var plusImageGallery = document.getElementById('plusImageGallery');
            if (grayRectangleGallery.classList.contains('show')) {
                grayRectangleGallery.classList.remove('show');
                circleImageGallery.style.opacity = 0;
                galleryText.style.opacity = 1;
                circleImageGallery.style.transition = 'transform 0.5s';
                plusImageGallery.style.transition = 'transform 0.5s';
                circleImageGallery.style.transform = 'translateY(0) translateX(-50%)';
                plusImageGallery.style.transform = 'translateY(0) translateX(-50%)';
                circleImageGallery.src = 'https://raw.githubusercontent.com/grifthtwelve/Repository/main/Circle.png';
                plusImageGallery.src = 'https://raw.githubusercontent.com/grifthtwelve/Repository/main/plus.png';
            } else {
                grayRectangleGallery.classList.add('show');
                circleImageGallery.style.opacity = 1;
                galleryText.style.opacity = 0;
                circleImageGallery.style.transition = 'transform 0.5s';
                plusImageGallery.style.transition = 'transform 0.5s';
                circleImageGallery.style.transform = 'translateY(60px) translateX(-50%)';
                plusImageGallery.style.transform = 'translateY(60px) translateX(-50%)';
                circleImageGallery.src = 'https://raw.githubusercontent.com/grifthtwelve/Repository/main/Circle2.png';
                plusImageGallery.src = 'https://raw.githubusercontent.com/grifthtwelve/Repository/main/minus.png';
            }
        }

        const projectsText = document.getElementById('ProjectsSection');
        function toggleAdditionalGrayRectangleProjects() {
            var grayRectangleProjects = document.getElementById('additionalGrayRectangleProjects');
            var circleImageProjects = document.getElementById('circleImageProjects');
            var plusImageProjects = document.getElementById('plusImageProjects');
            if (grayRectangleProjects.classList.contains('show')) {
                grayRectangleProjects.classList.remove('show');
                circleImageProjects.style.opacity = 0;
                projectsText.style.opacity = 1;
                circleImageProjects.style.transition = 'transform 0.5s';
                plusImageProjects.style.transition = 'transform 0.5s';
                circleImageProjects.style.transform = 'translateY(0) translateX(-50%)';
                plusImageProjects.style.transform = 'translateY(0) translateX(-50%)';
                circleImageProjects.src = 'https://raw.githubusercontent.com/grifthtwelve/Repository/main/Circle.png';
                plusImageProjects.src = 'https://raw.githubusercontent.com/grifthtwelve/Repository/main/plus.png';
            } else {
                grayRectangleProjects.classList.add('show');
                circleImageProjects.style.opacity = 1;
                projectsText.style.opacity = 0;
                circleImageProjects.style.transition = 'transform 0.5s';
                plusImageProjects.style.transition = 'transform 0.5s';
                circleImageProjects.style.transform = 'translateY(60px) translateX(-50%)';
                plusImageProjects.style.transform = 'translateY(60px) translateX(-50%)';
                circleImageProjects.src = 'https://raw.githubusercontent.com/grifthtwelve/Repository/main/Circle2.png';
                plusImageProjects.src = 'https://raw.githubusercontent.com/grifthtwelve/Repository/main/minus.png';
            }
        }
        document.getElementById('plusImage').addEventListener('mouseover', function() {
        });

        document.getElementById('plusImage').addEventListener('mouseout', function() {
            if (!document.getElementById('additionalGrayRectangle').classList.contains('show')) {
            }
        });

        document.getElementById('plusImageGallery').addEventListener('mouseover', function() {
        });

        document.getElementById('plusImageGallery').addEventListener('mouseout', function() {
            if (!document.getElementById('additionalGrayRectangleGallery').classList.contains('show')) {
            }
        });
    </script>
</body>
</html>
