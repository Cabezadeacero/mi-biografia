<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Mi Biografía</title>
    <style>
        body {
            background: linear-gradient(135deg, #BDB76B, #4682B4);
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 40px 20px;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .contenedor-principal {
            background-color: white;
            max-width: 700px;
            width: 100%;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 0 30px rgba(0,0,0,0.15);
            box-sizing: border-box;
        }

        h1 {
            color: #2c3e50;
            text-align: center;
            font-size: 36px;
            margin-top: 0;
        }

        h2 {
            color: #4682B4;
            border-bottom: 5px solid #4682B4;
            padding-bottom: 8px;
            margin-top: 30px;
        }

        p, h4 {
            color: #34495e;
            font-weight: normal;
            line-height: 1.6;
        }

        img {
            display: block;
            margin: 20px auto;
            border-radius: 50%;
            border: 4px solid #3498db;
            width: 200px;
            height: 200px;
            object-fit: cover;
        }

        ul {
            background-color: #ecf0f1;
            padding: 20px 40px;
            border-radius: 12px;
            list-style: disc;
        }

        ul li {
            padding: 8px 0;
            border-bottom: 1px solid #bdc3c7;
            color: #2c3e50;
        }

        ul li:last-child {
            border-bottom: none;
        }

        a {
            color: #e74c3c;
            text-decoration: none;
            font-weight: bold;
        }

        a:hover {
            text-decoration: underline;
            color: #4682B4;
        }

        #boton-continuar {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
            font-size: 14px;
            font-weight: bold;
            transition: background 0.3s;
        }

        #boton-continuar:hover {
            background-color: #2980b9;
        }

        /* --- Estilos de la Sección de Música --- */
        .seccion-musica {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-bottom: 30px;
        }

        .tarjeta-cancion {
            background-color: #f8f9fa;
            border-left: 5px solid #e74c3c;
            padding: 15px 20px;
            border-radius: 8px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }

        .info-cancion {
            display: flex;
            flex-direction: column;
        }

        .titulo-cancion {
            font-weight: bold;
            color: #2c3e50;
            font-size: 16px;
        }

        .artista-cancion {
            color: #7f8c8d;
            font-size: 14px;
            margin-top: 4px;
        }

        .boton-youtube {
            background-color: #e74c3c;
            color: white !important;
            padding: 8px 14px;
            border-radius: 20px;
            font-size: 13px;
            text-decoration: none;
            transition: background-color 0.3s, transform 0.2s;
        }

        .boton-youtube:hover {
            background-color: #c0392b;
            text-decoration: none !important;
            transform: scale(1.05);
        }
    </style>
</head>
<body>

<div class="contenedor-principal">
    <h1>¡Hola! Soy Ezequias Elal</h1>
    <p style="text-align: center; font-style: italic; color: #7f8c8d;">
        Esta es mi primera página web. Por lo tanto no es perfecta.
    </p>
    
    <h2>Sobre mí</h2>
    <p>
        Yo nací en Córdoba, Córdoba, Argentina el 3 de noviembre de 2011.
        <span id="texto-efecto"></span>
    </p>
    <button id="boton-continuar">Continuar</button>

    <img src="foto.jpg" alt="Mi foto">

    <h2>Mis gustos</h2>
    <ul>
        <li>Me gusta hacer origamis</li>
        <li>Hice taekwondo</li>
        <li>Y me gusta resolver cubos de Rubik</li>
    </ul>

    <!-- SECCIÓN DE MÚSICA FAVORITA -->
    <h2>Mi música favorita</h2>
    <div class="seccion-musica">
        <!-- Canción 1 -->
        <div class="tarjeta-cancion">
            <div class="info-cancion">
                <span class="titulo-cancion">Christmas Truce</span>
                <span class="artista-cancion">Sabaton</span>
            </div>
            <a href="https://www.youtube.com/watch?v=RkR1Mn2X6_M" target="_blank" class="boton-youtube">
                Escuchar en YouTube
            </a>
        </div>

        <!-- Canción 2 -->
        <div class="tarjeta-cancion">
            <div class="info-cancion">
                <span class="titulo-cancion">Bismarck</span>
                <span class="artista-cancion">Sabaton</span>
            </div>
            <a href="https://youtube.com" target="_blank" class="boton-youtube">
                Escuchar en YouTube
            </a>
        </div>

        <!-- Canción 3 -->
        <div class="tarjeta-cancion">
            <div class="info-cancion">
                <span class="titulo-cancion">Thunderstruck</span>
                <span class="artista-cancion">AC/DC</span>
            </div>
            <a href="https://youtube.com" target="_blank" class="boton-youtube">
                Escuchar en YouTube
            </a>
        </div>
    </div>

    <h2>Mi futuro</h2>
    <p>Yo en 5 años me veo estudiando para la facu y trabajando para tener mi propio sueldo.</p>
    
    <p>Mi Instagram: <a href="https://instagram.com" target="_blank">@hola_chau</a></p>
    <!-- es el instagram de mi hermana porque yo no uso redes sociales -->
</div>

<script>
    const textoCompleto = "\n\nMe crié con mi familia, esta está compuesta por mi papá, mi mamá y mis dos hermanas.\nCuando tenía unos 13 años nació mi hermanito menor llamado Adán.";
    const boton = document.getElementById('boton-continuar');
    const contenedor = document.getElementById('texto-efecto');
    let indice = 0;

    function escribirLetra() {
        if (indice < textoCompleto.length) {
            let letraActual = textoCompleto.charAt(indice);
            if (letraActual === "\n") {
                contenedor.innerHTML += "<br>";
            } else {
                contenedor.innerHTML += letraActual;
            }
            indice++;
            setTimeout(escribirLetra, 40);
        }
    }

    boton.addEventListener('click', function() {
        boton.style.display = 'none';
        escribirLetra();
    });
</script>

</body>
</html>

