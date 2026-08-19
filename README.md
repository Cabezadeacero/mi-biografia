<!DOCTYPE html> 
 <html> 
<head>
 <meta charset="UTF-8"> <title>Mi Biografía</title>
<style> body{
background: linear-gradient(135deg,#BDB76B,#4682B4); 
    font-family: Arial, sans-serif;
    max-width: 700px;
    margin: 40px auto;
    padding: 30px;
    background-color: white;}
{ background-color: #90EE90; font-family: Arial, sans-serif; max-width: 700px; margin: 40px auto; padding: 30px; background-color: white; border-radius: 20px; box-shadow: 0 0 30px rgba(0,0,0,0.1); } h1 { color: #2c3e50; text-align: center; font-size: 36px; } h2 { color: #90EE90; border-bottom: 5px solid #90EE90; padding-bottom: 8px; } img { display: block; margin: 20px auto; border-radius: 50%; border: 4px solid #3498db; width: 200px; height: 200px; object-fit: cover; } 
ul { background-color: #ecf0f1; padding: 20px 30px; border-radius: 12px; list-style: none; } ul li { padding: 8px 0; border-bottom: 1px solid #bdc3c7; } ul li:last-child { border-bottom: none; }
a { color: #e74c3c; text-decoration: none; font-weight: bold; } a:hover { text-decoration: underline; color: #4682B4; }

#texto-extra {
  display: none;
}


#boton-continuar {
  background-color: #3498db;
  color: white;
  border: none;
  padding: 8px 15px;
  border-radius: 5px;
  cursor: pointer;
  margin-top: 10px;
}

</style>

</head>
    <h1>¡Hola! Soy Ezequias Elal</h1> 
  <em><p>Esta es mi primera página web.Por lo tanto no es perfecta</p></em>
    <h2>Sobre mi</h2> 
 <h4>
  <p>
    Yo naci en Cordoba, Cordoba, Argentina el 3 de noviembre de 2011.
    
  
    <span id="texto-efecto"></span>
  </p>
  
 
  <button id="boton-continuar">Continuar</button>
</h4>
 <img src="foto.jpg" alt="Mi foto" width="200">
 <h2>Mis gustos</h2>
<ul><li>Me gusta hacer origamis</li>
    <li>Hice taekwondo</li>
    <li>Y me gusta resolver cubos de rubik</li>
</ul>
<h2>Mi futuro</h2>
<p>yo en 5 años me veo estudiando para la facu y trabajando para tener mi propio sueldo.</p>
<p>Mi Instagram: <a href="https://instagram.com/hola_chau">@hola_chau</a></p><!--es el instagram de mi hermana porque yo no uso redes sociales -->
<script>
  // 1. Guardamos el texto completo que queremos que se escriba solo
  // Usamos \n para los saltos de línea (que luego convertiremos en <br>)
  const textoCompleto = "\n Me crie con mi famila, esta está compuesta por mi papá, mi mamá y mis dos hermanas.\n Cuando tenia unos 13 años nacio mi hermanito menor llamado Ádan.";

  // 2. Seleccionamos los elementos del HTML
  const boton = document.getElementById('boton-continuar');
  const contenedor = document.getElementById('texto-efecto');

  let indice = 0; // Lleva la cuenta de qué letra toca escribir

  // 3. Esta función se ejecuta repetidamente para escribir letra por letra
  function escribirLetra() {
    if (indice < textoCompleto.length) {
      let letraActual = textoCompleto.charAt(indice);

      // Si encuentra un salto de línea (\n), lo convierte en una etiqueta <br> para el HTML
      if (letraActual === "\n") {
        contenedor.innerHTML += "<br>";
      } else {
        contenedor.innerHTML += letraActual;
      }

      indice++;
      // Velocidad: Ejecuta la función de nuevo en 40 milisegundos (puedes cambiar este número)
      setTimeout(escribirLetra, 40); 
    }
  }

  // 4. Escuchamos el clic del botón para iniciar el efecto
  boton.addEventListener('click', function() {
    boton.style.display = 'none'; // Esconde el botón inmediatamente
    escribirLetra();              // Arranca la animación de escritura
  });
</script>

</body>
</html> 
