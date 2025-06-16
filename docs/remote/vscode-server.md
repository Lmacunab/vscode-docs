<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Pausa Al Zilencio</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to bottom, #fef9f9, #fff0f5, #f3e5f5);
      color: #333;
      transition: background 0.5s, color 0.5s;
    }

    .dark-mode {
      background: #1e1e2f;
      color: #f0f0f0;
    }

    #progress-bar {
      position: fixed;
      top: 0;
      left: 0;
      height: 5px;
      background-color: #a18cd1;
      width: 0%;
      z-index: 999;
    }

    #menu-toggle { display: none; }

    #sidebar {
      position: fixed;
      top: 0;
      left: 0;
      width: 240px;
      height: 100%;
      background: linear-gradient(to bottom, #dcd6f7, #a6c1ee);
      padding-top: 60px;
      box-shadow: 2px 0 10px rgba(0,0,0,0.1);
      z-index: 998;
    }

    #sidebar ul {
      list-style-type: none;
      padding: 0;
    }

    #sidebar ul li {
      margin: 20px 0;
      text-align: center;
    }

    #sidebar ul li a {
      text-decoration: none;
      color: #6a5acd;
      font-weight: bold;
      font-size: 18px;
      transition: 0.3s;
    }

    #sidebar ul li a:hover,
    #sidebar ul li a.active {
      color: #ff69b4;
      background-color: #f3e5f5;
      padding: 5px 10px;
      border-radius: 10px;
    }

    header {
      margin-left: 240px;
      padding: 40px;
      background-color: #ffffffcc;
      text-align: center;
      border-bottom: 1px solid #ddd;
    }

    header h1 {
      font-size: 40px;
      color: #6a5acd;
      margin: 0;
    }

    header h2 {
      font-size: 24px;
      color: #a18cd1;
      margin-top: 10px;
    }

    .buttons {
      display: flex;
      justify-content: center;
      gap: 15px;
      margin-top: 20px;
    }

    .buttons button {
      padding: 10px 15px;
      border: none;
      border-radius: 10px;
      background-color: #d9b8ff;
      color: #fff;
      font-weight: bold;
      cursor: pointer;
    }

    .buttons button:hover {
      background-color: #a18cd1;
    }

    main {
      margin-left: 240px;
      padding: 40px;
    }

    section {
      padding: 60px 0;
      border-bottom: 1px solid #ddd;
    }

    h2 {
      color: #a18cd1;
      font-size: 30px;
      margin-bottom: 15px;
    }

    p, ul li {
      font-size: 20px;
      line-height: 1.8;
    }

    ul { padding-left: 20px; }

    img {
      max-width: 100%;
      border-radius: 10px;
      margin: 20px 0;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }

    .comentarios {
      background-color: #fff;
      border-radius: 10px;
      padding: 20px;
      margin-top: 50px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }

    .comentarios textarea {
      width: 100%;
      padding: 15px;
      border-radius: 8px;
      border: 1px solid #ccc;
      resize: none;
      font-size: 16px;
      height: 120px;
    }

    .comentarios button {
      margin-top: 10px;
      padding: 10px 20px;
      background-color: #a18cd1;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: not-allowed;
      font-weight: bold;
    }

    footer {
      margin-left: 240px;
      padding: 20px;
      text-align: center;
      font-size: 14px;
      color: #999;
    }

    .motivador {
      background-color: #f3e5f5;
      color: #6a5acd;
      font-size: 18px;
      margin-top: 30px;
      padding: 15px;
      border-left: 5px solid #a18cd1;
      border-radius: 10px;
    }
  </style>
</head>
<body>
  <div id="progress-bar"></div>

  <nav id="sidebar">
    <ul>
      <li><a href="#inicio" class="nav-link">Inicio</a></li>
      <li><a href="#que-es" class="nav-link">¿Qué es?</a></li>
      <li><a href="#problemas" class="nav-link">Problemas comunes</a></li>
      <li><a href="#causas" class="nav-link">Causas</a></li>
      <li><a href="#efectos" class="nav-link">Efectos</a></li>
      <li><a href="#ayuda" class="nav-link">Pedir ayuda</a></li>
      <li><a href="#conclusion" class="nav-link">Conclusión</a></li>
      <li><a href="#fuentes" class="nav-link">Fuentes</a></li>
      <li><a href="#comentarios" class="nav-link">Comentarios</a></li>
    </ul>
  </nav>

  <header>
    <h1>Pausa Al Zilencio</h1>
    <h2>La salud mental de los adolescentes</h2>
    <div class="buttons">
      <button onclick="toggleMusic()">🎵 Música</button>
      <button onclick="toggleDarkMode()">🌓 Modo oscuro</button>
    </div>
    <div id="motivador" class="motivador">✨ Tú importas y mereces estar bien.</div>
  </header>

  <main>
     <!-- Inicio -->
     <section id="inicio">
       <h2>🟣 1. Inicio</h2>
       <p>¡Hola! Bienvenid@ a esta página sobre salud mental en adolescentes.
Mira, la adolescencia es como una montaña rusa: un día estás feliz, al día siguiente triste, luego todo te estresa y después te da risa. No estás loc@, simplemente estás creciendo y pasando por cambios.

En esta web vas a entender mejor qué es la salud mental, por qué a veces te sientes raro o confundid@, y qué hacer cuando eso pasa.
La idea es que no te sientas sol@ con lo que te pasa, y que sepas que hay formas de sentirte mejor. Este espacio es para ti. 💬🧠</p>
       <img src="https://images.pexels.com/photos/1756170/pexels-photo-1756170.jpeg" alt="Adolescente feliz">
     </section>

     <!-- Qué es -->
     <section id="que-es">
       <h2>🟣 2. ¿Qué es la salud mental?</h2>
       <p>La salud mental no es estar feliz todo el tiempo ni ser perfect@. Es más bien cómo te sientes por dentro, cómo piensas, cómo manejas tus emociones, y cómo te llevas con los demás.
        Cuidar la salud mental es como cuidar tu cuerpo: si te duele la cabeza, descansas; si te sientes triste o estresad@, también hay formas de ayudarte.
        Sentirte mal a veces es normal, pero lo importante es que aprendas a reconocer lo que te pasa y que no lo ignores. 💖🧘‍♀️</p>
       <img src="https://images.pexels.com/photos/3958421/pexels-photo-3958421.jpeg" alt="Reflexión emocional">
     </section>

     <!-- Problemas -->
     <section id="problemas">
       <h2>🟣 3. Problemas que más vivimos los adolescentes</h2>
       <p>A esta edad, muchas cosas cambian y se sienten intensas. A veces ni sabemos por qué estamos tristes o molestos. Te cuento algunos de los problemas más comunes:</p>
       <ul>
         <li><strong>Ansiedad:</strong>  es cuando te sientes nervios@ todo el tiempo, como si algo malo fuera a pasar. Puedes sentir que el corazón te late rápido, que no puedes respirar bien o que no puedes dejar de pensar.</li>
         <li><strong>Depresión:</strong> es sentirte triste por mucho tiempo. Nada te motiva, todo te da flojera o ya no te emociona lo que antes sí. A veces ni quieres levantarte de la cama.</li>
         <li><strong>Baja autoestima:</strong>  es cuando sientes que no vales, que no eres suficiente o que todos son mejores que tú. Te comparas mucho o te criticas un montón.</li>
         <li><strong>Trastornos alimenticios:</strong>  como dejar de comer o comer demasiado por nervios o por querer cambiar tu cuerpo. A veces no se trata solo de comida, sino de cómo te sientes contigo mism@.</li>
         <li><strong>Autolesiones o pensamientos tristes extremos:</strong> es cuando alguien se lastima a propósito o piensa en cosas feas como que no quiere seguir. Es algo muy serio, pero se puede tratar si se pide ayuda.</li>
        </ul>
        <p>Muchos de estos problemas no se notan por fuera. Así que si tú o alguien que conoces los está viviendo, no lo minimices. Hablarlo puede ayudar muchísimo.</p>
       <img src="https://images.pexels.com/photos/32533363/pexels-photo-32533363.jpeg" alt="Adolescente depresivo">
     </section>

     <!-- Causas -->
     <section id="causas">
       <h2>🟣 4. ¿Por qué pasa todo esto?</h2>
       <p>No es que un día te levantes y ¡boom! te sientes mal sin razón. Hay varias cosas que pueden hacer que tu salud mental se afecte:<p>
       <ul>
         <li><strong>Presión del cole:</strong> exámenes, tareas, notas, que los profes esperen mucho de ti, que tus papás te comparen… Todo eso agota y estresa. A veces parece que si no sacas buena nota, ya vales menos, y no es así.</li>
         <li><strong>Redes sociales:</strong> ves gente "perfecta", con cuerpazos, ropa top, viajes, novios/novias y vidas increíbles… y te empiezas a comparar. Eso baja tu autoestima, aunque sabes que muchas cosas son editadas o actuadas.</li>
         <li><strong>Problemas en casa:</strong> peleas, gritos, falta de cariño o que nadie te escuche. Si tu casa no es un lugar seguro, es normal que te sientas bajonead@ o confundid@.</li>
         <li><strong>Amores y amistades:</strong> cuando te peleas con tu bff, cuando te gusta alguien que no te corresponde, cuando te sientes fuera de tu grupo… todo eso duele. A veces más de lo que uno admite</li>
         <li><strong>Bullying:</strong> que te molesten, se rían de ti o te dejen de lado en el cole. Eso duele muchísimo y afecta cómo te ves a ti mism@.</li>
         <li><strong>Hormonas locas:</strong> sí, literal. En la adolescencia las hormonas están full activas y eso hace que tengas cambios de humor rarísimos sin razón. Un minuto feliz, al otro llorando. NORMAL.</li>
         <li><strong>Expectativas:</strong> sentir que debes ser el/la hij@ perfect@, sacar buenas notas, ser flac@, popular, “cool” o “exit@s@”... es demasiado. Y cuando sientes que no llegas, te frustras.</li>
       </ul>
       <p>🎯 Todo esto es real. No estás exagerando. Y sentirte mal por eso no te hace débil.</p>
       <img src="https://images.pexels.com/photos/7683901/pexels-photo-7683901.jpeg" alt="Chico dormido con libros">
     </section>

     <!-- Efectos -->
     <section id="efectos">
       <h2>🟣 5. ¿Cómo afecta en tu día a día?</h2>
       <ul>
         <li>Cuando la salud mental no está bien, muchas cosas empiezan a cambiar:<li>
         <li>Ya no rindes igual en el cole porque no puedes concentrarte. Estás como en modo zombie.</li>
         <li>Duermes demasiado o no puedes dormir nada. Tu cabeza no para de pensar o te sientes sin energía todo el día.</li>
         <li>Comes mucho por ansiedad o dejas de comer porque no tienes ganas. O simplemente te da igual.</li>
         <li>Te alejas de tus amigos, o te molesta todo lo que hacen. Te sientes raro hasta con la gente que quieres.</li>
         <li>Te deja de gustar lo que antes te emocionaba: jugar, dibujar, salir, ver series. Todo te da flojera o no tiene sentido.</li>
         <li>Te miras al espejo y no te gusta lo que ves. Te criticas, te sientes fe@ o tont@ aunque no sea verdad.</li>
         <li><strong>Y lo peor:</strong> a veces sientes que nadie te entiende. Pero créeme, sí hay formas de mejorar.</li>
        </ul>
       <img src="https://images.pexels.com/photos/6147127/pexels-photo-6147127.jpeg" alt="chico alejandose de sus amigos">
     </section>

     <!-- Ayuda -->
     <section id="ayuda">
       <h2>🟣 6. ¿Cómo pedir ayuda?</h2>
       <p>💪 Sé que cuesta decir lo que sientes. A veces piensas “me van a decir exagerad@”, “no quiero preocupar a nadie”, o “mejor me aguanto”.
        Pero no. Guardarte todo eso solo te hace más daño.</p>
        <p> 💪 Pedir ayuda es de valientes.</p>
        <p> Puedes hablar con un psicólog@, con tus papás, un profe buena onda o hasta con un amigo/a. Lo importante es no quedarte callad@.
          También puedes escribir lo que sientes en un cuaderno, hacer dibujos, bailar, caminar, escuchar música tranquila o lo que te haga sentir un poco mejor.</p>
       <p> Y si no tienes a nadie cerca en ese momento, hay líneas de ayuda por WhatsApp, teléfono o incluso chats anónimos donde puedes contar lo que sientes sin miedo.</p>
       <li><strong> 💬 Lo repito:</strong> NO estás sol@. Y sí hay gente que te puede ayudar.<li>
       <img src="https://images.pexels.com/photos/4100419/pexels-photo-4100419.jpeg" alt="Adolescente con psicologo">
     </section>

     <!-- Conclusión -->
     <section id="conclusion">
       <h2>🟣 7. Conclusión</h2>
       <p>La salud mental importa. Y aunque a veces parezca un tema complicado o que nadie entiende, tú no estás sol@.</p>
       <p>Reconocer que no estás bien es valiente. Hablar es valiente. Pedir ayuda es valiente.</p>
       <p>💜 Cuidarte también es una forma de resistir. Tú vales, importas y mereces estar bien.<p>

       <img src="https://images.pexels.com/photos/7692763/pexels-photo-7692763.jpeg" alt="adolescente sonriendo">
     </section>

     <!-- Artículo especial -->
     <section style="background-color: #fff5fc; border-left: 6px solid #fbc2eb; padding: 30px; margin-bottom: 40px; border-radius: 10px;">
       <h2 style="font-size: 28px; color: #d46bcb;">Artículo especial: "Pausa al Zilencio"</h2>
       <p style="font-size: 18px;">Este artículo busca ayudar a adolescentes a entender su salud mental, conocer causas, efectos y cómo pedir ayuda, con un lenguaje real, cálido y súper cercano. 💬</p>
     </section>

     <!-- Fuentes -->
     <section id="fuentes">
       <h2>📚 8. Fuentes</h2>
       <ul style="font-size: 18px;">
         <li>Unicef (2022). <i>Salud mental en adolescentes.</i></li>
         <li>OMS (2023). <i>Adolescent Mental Health.</i></li>
         <li>BBC Mundo (2023). Artículos sobre salud emocional juvenil.</li>
       </ul>
     </section>

     <!-- Comentarios -->
     <section id="comentarios">
       <h2>💬 9. Comentarios</h2>
       <div style="background-color: #f2f2f2; border-radius: 10px; padding: 20px; margin-top: 10px;">
         <p><strong>✨ Andrea:</strong> Me encantó esta web, sentí que alguien me entendía por fin 🥹💜</p>
       </div>
       <div style="background-color: #f2f2f2; border-radius: 10px; padding: 20px; margin-top: 10px;">
         <p><strong>✨ Diego:</strong> Ojalá el cole hablara más de esto. Me sentí muy identificado.</p>
       </div>
       <textarea placeholder="Escribe tu comentario aquí"></textarea>
       <button disabled>Enviar</button>
     </section>
    </main>

      <footer>
        © 2025 Pausa Al Zilencio — hecho con 💜 por Lu
      </footer>

      <audio id="background-music" loop>
        <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_b4cb94f49e.mp3?filename=calm-relaxing-music-11766.mp3" type="audio/mpeg">
        Tu navegador no soporta música.
      </audio>

      <script>
        const progressBar = document.getElementById("progress-bar");
        const sections = document.querySelectorAll("section");
        const navLinks = document.querySelectorAll(".nav-link");
        const audio = document.getElementById("background-music");
        const motivador = document.getElementById("motivador");
        let frases = [
          "✨ Tú importas y mereces estar bien.",
          "💖 No estás sol@, siempre hay una salida.",
          "🌈 Lo estás haciendo mejor de lo que crees.",
          "🧠 Tu mente también merece cuidados.",
          "💜 Hablar es sanar. No te calles."
        ];

        window.onscroll = function () {
          let winScroll = document.body.scrollTop || document.documentElement.scrollTop;
          let height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
          let scrolled = (winScroll / height) * 100;
          progressBar.style.width = scrolled + "%";

          let current = "";
          sections.forEach(section => {
            const sectionTop = section.offsetTop - 100;
            if (scrollY >= sectionTop) {
              current = section.getAttribute("id");
            }
          });

          navLinks.forEach(link => {
            link.classList.remove("active");
            if (link.getAttribute("href") === "#" + current) {
              link.classList.add("active");
            }
          });
        };

        function toggleMusic() {
          if (audio.paused) {
            audio.play();
          } else {
            audio.pause();
          }
        }

        function toggleDarkMode() {
          document.body.classList.toggle("dark-mode");
        }

        setInterval(() => {
          let random = frases[Math.floor(Math.random() * frases.length)];
          motivador.textContent = random;
        }, 6000);
      </script>
    </body>
    </html>