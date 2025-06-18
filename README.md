<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Guía Digital para Adultos Mayores</title>
  <style>
    body {
      background-color: black;
      color: white;
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 50px 20px;
    }

    h1, h3 {
      margin-bottom: 20px;
    }

    .btn {
      font-size: 28px;
      padding: 20px 30px;
      margin: 10px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: transform 0.2s;
      color: white;
      width: 80%;
      max-width: 300px;
    }

    .btn:hover {
      transform: scale(1.05);
    }

    #whatsappBtn { background-color: limegreen; }
    #correoBtn { background-color: dodgerblue; }
    #navegacionBtn { background-color: orange; }

    #output {
      margin-top: 30px;
      font-size: 20px;
      background-color: #222;
      padding: 20px;
      border-radius: 10px;
      white-space: normal;
      text-align: left;
      display: none;
    }

    #speakBtn {
      margin-top: 10px;
      font-size: 18px;
      padding: 10px 20px;
      background-color: #555;
      border: none;
      color: white;
      border-radius: 8px;
      cursor: pointer;
      display: none;
    }

    #speakBtn:hover {
      background-color: #777;
    }

    img.guide-img {
      width: 100%;
      max-width: 300px;
      margin: 10px 0;
      border-radius: 10px;
    }
  </style>
</head>
<body>

  <h1>Guía para aprender a usar herramientas digitales básicas</h1>
  <h3>Seleccione la aplicación que quiere aprender a usar:</h3>

  <button id="whatsappBtn" class="btn">WhatsApp</button><br>
  <button id="correoBtn" class="btn">Correo Electrónico</button><br>
  <button id="navegacionBtn" class="btn">Navegación Web</button>

  <div id="output"></div>
  <button id="speakBtn">🔊 Escuchar</button>

  <script>
    const output = document.getElementById("output");
    const speakBtn = document.getElementById("speakBtn");

    const whatsappText = `
      <h2>Guía para usar WhatsApp:</h2>
      <ol>
        <li>Abre la tienda de aplicaciones: "Play Store".</li>
<img src="Imagenes_Web/21imagen.jpg" class="guide-img" alt="Videollamada">
        <li>Busca la opción que dice "buscar", tiene una lupa y está ubicada abajo.</li>
        <img src="Imagenes_Web/Whatsappimagen1.jpg" class="guide-img" alt="Buscar WhatsApp">
        <li>Haz clic arriba, se mostrará un teclado donde escribirás WhatsApp. Luego haz clic en la app correcta y pulsa el botón verde "Instalar". Abre la app al terminar.</li>
        <img src="Imagenes_Web/2imagenen.jpg" class="guide-img" alt="Instalar WhatsApp">
        <img src="Imagenes_Web/3imagenen.jpg" class="guide-img" alt="Instalar WhatsApp">
        <li>Acepta los permisos y escribe tu número de teléfono.</li>
        <li>Te llegará un mensaje con un código. Escríbelo.</li>
        <li>Para enviar mensajes:
          <ul>
            <li>Presiona el botón verde con mensaje.</li>
            <img src="Imagenes_Web/4imagen.jpg" class="guide-img" alt="Nuevo mensaje">
            <li>Busca o crea un contacto con nombre y número. Haz clic en "Guardar".</li>
            <img src="Imagenes_Web/5imagen.jpg" class="guide-img" alt="Crear contacto">
            <img src="Imagenes_Web/6imagen.jpg" class="guide-img" alt="Guardar contacto">
            <img src="Imagenes_Web/7imagen.jpg" class="guide-img" alt="Ver contactos">
            <li>Haz clic en el contacto, escribe abajo tu mensaje, y toca el ícono de avión para enviarlo.</li>
            <img src="Imagenes_Web/8imagen.jpg" class="guide-img" alt="Enviar mensaje">
          </ul>
        </li>
        <li>Para enviar una imagen:
          <ul>
            <li>Toca el ícono de clip o cámara.</li>
            <img src="Imagenes_Web/9imagen.jpg" class="guide-img" alt="Adjuntar imagen">
            <li>Elige una foto o toma una nueva. Luego toca el ícono de enviar.</li>
            <img src="Imagenes_Web/10imagen.jpg" class="guide-img" alt="Elegir imagen">
            <img src="Imagenes_Web/11imagen.jpg" class="guide-img" alt="Enviar imagen">
          </ul>
        </li>
        <li>Para videollamadas:
          <ul>
            <li>Abre el chat de la persona.</li>
            <li>Toca el ícono de cámara arriba.</li>
          </ul>
        </li>
        <img src="Imagenes_Web/12imagen.jpg" class="guide-img" alt="Videollamada">
      </ol>`;

    const correoText = `
      <h2>Guía para usar el Correo Electrónico:</h2>
      <ol>
        <li>Busca Gmail.</li>
        <li>Abre Gmail.</li>
<img src="Imagenes_Web/14imagen.jpg" class="guide-img" alt="Videollamada">
        <li>Abre la app y registrate creando tu correo con cualquier texto y luego @gmail.com y crea una contraseña.</li>
        <li>Para enviar un correo:
          <ul>
            <li>Toca en "Redactar" o el ícono de lápiz.</li>
<img src="Imagenes_Web/15imagen.jpg" class="guide-img" alt="Videollamada">
            <li>Escribe el correo del destinatario.</li>
            <li>Agrega un asunto dando click en el pondras el titulo del correo y al dar click en "redactar un correo" pondras el mensaje.</li>
            <li>Toca "Enviar".</li>
<img src="Imagenes_Web/16imagen.jpg" class="guide-img" alt="Videollamada">
          </ul>
        </li>
      </ol>`;

    const navegacionText = `
      <h2>Guía para usar Navegación Web:</h2>
      <ol>
        <li>Abre la app "Chrome" o "Google".</li>
<img src="Imagenes_Web/17imagen.jpg" class="guide-img" alt="Videollamada">
        <li>Toca la barra de búsqueda arriba.</li>
<img src="Imagenes_Web/18imagen.jpg" class="guide-img" alt="Videollamada">
        <li>Escribe lo que quieres buscar y toca la lupa o "Buscar".</li>
<img src="Imagenes_Web/19imagen.jpg" class="guide-img" alt="Videollamada">
        <li>Selecciona un resultado de los muchos que abran para abrir la página que quieres.</li>
        <li>Desliza con el dedo para leer.</li>
<img src="Imagenes_Web/20imagen.jpg" class="guide-img" alt="Videollamada">
        <li>Usa la flecha de atrás para volver.</li>
      </ol>`;

    function mostrarTexto(html) {
      output.innerHTML = html;
      output.style.display = "block";
      speakBtn.style.display = "inline-block";
      const tempText = html.replace(/<[^>]*>?/gm, ''); // Quitar etiquetas HTML
      speakBtn.onclick = () => {
        const utterance = new SpeechSynthesisUtterance(tempText);
        utterance.lang = 'es-ES';
        window.speechSynthesis.cancel();
        window.speechSynthesis.speak(utterance);
      };
      agregarPreguntaInteraccion();
    }

    function agregarPreguntaInteraccion() {
      const preguntaHTML = `
        <div id="interaccion" style="margin-top: 30px;">
          <h3>¿Pudiste seguir los pasos?</h3>
          <button class="btn" style="background-color: green;" id="btnSi">Sí</button>
          <button class="btn" style="background-color: red;" id="btnNo">No</button>
          <button class="btn" style="background-color: gray;" id="btnAyuda">Necesito ayuda</button>
          <div id="respuesta" style="margin-top: 20px; font-size: 18px;"></div>
        </div>
      `;
      output.innerHTML += preguntaHTML;

      document.getElementById("btnSi").addEventListener("click", () => {
        document.getElementById("respuesta").textContent = "¡Excelente! Puedes seguir aprendiendo otra herramienta.";
      });

      document.getElementById("btnNo").addEventListener("click", () => {
        document.getElementById("respuesta").textContent = "Recomendamos pedir ayuda a un familiar o llamar al número 800 400 035 para recibir asistencia.";
      });

      document.getElementById("btnAyuda").addEventListener("click", () => {
        document.getElementById("respuesta").textContent = "Recomendamos pedir ayuda a un familiar o llamar al número 800 400 035 para recibir asistencia.";
      });
    }

    document.getElementById("whatsappBtn").addEventListener("click", () => {
      mostrarTexto(whatsappText);
    });

    document.getElementById("correoBtn").addEventListener("click", () => {
      mostrarTexto(correoText);
    });

    document.getElementById("navegacionBtn").addEventListener("click", () => {
      mostrarTexto(navegacionText);
    });
  </script>

</body>
</html>
