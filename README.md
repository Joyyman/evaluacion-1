<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Relax Total</title>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Quicksand', sans-serif;
      background: linear-gradient(to right, #cce5df, #f7f3e9);
      color: #2f3e46;
      padding: 40px 20px;
      text-align: center;
      position: relative;
    }

    header h1 {
      font-size: 3.5em;
      color: #ff5722;
      margin-bottom: 15px;
      opacity: 0;
      transform: translateY(-50px);
      animation: slideIn 1s forwards, pulse 2s infinite;
    }

    header p {
      font-size: 1.5em;
      color: #ff9800;
      opacity: 0;
      animation: fadeIn 1.5s 1s forwards, pulse 2s infinite;
    }

    @keyframes slideIn {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes fadeIn {
      to {
        opacity: 1;
      }
    }

    @keyframes pulse {
      0% {
        transform: scale(1);
      }
      50% {
        transform: scale(1.1);
      }
      100% {
        transform: scale(1);
      }
    }

    .buttons {
      margin-top: 40px;
      opacity: 0;
      animation: fadeInButtons 1.5s 2s forwards;
    }

    @keyframes fadeInButtons {
      to {
        opacity: 1;
      }
    }

    .relax-button {
      background-color: #3c6e71;
      color: #fff;
      border: none;
      padding: 20px 40px;
      font-size: 1.2em;
      border-radius: 50px;
      cursor: pointer;
      margin: 15px;
      transition: background-color 0.3s ease, transform 0.3s ease;
      transform: translateY(10px);
      opacity: 0;
      animation: slideUp 1s forwards;
      animation-delay: 2.5s;
    }

    @keyframes slideUp {
      to {
        transform: translateY(0);
        opacity: 1;
      }
    }

    .relax-button:hover {
      background-color: #2e5354;
      transform: scale(1.1);
    }

    .icon {
      margin-top: 20px;
      font-size: 50px;
      color: #3c6e71;
    }

    .section {
      max-width: 800px;
      margin: 40px auto;
      background-color: #ffffffcc;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      display: none;
    }

    .section.active {
      display: block;
    }

    .section h2 {
      color: #3c6e71;
      margin-bottom: 15px;
      font-size: 2.5em;
      animation: fadeInTitle 1s forwards;
    }

    @keyframes fadeInTitle {
      to {
        opacity: 1;
      }
    }

    .benefits-list {
      text-align: left;
      font-size: 1.2em;
      line-height: 1.8;
      color: #333;
      margin-top: 20px;
      animation: fadeInList 1.5s forwards;
    }

    @keyframes fadeInList {
      to {
        opacity: 1;
      }
    }

    .benefits-list ul {
      list-style-type: none;
    }

    .benefits-list li {
      margin-bottom: 15px;
      background-color: #f1f1f1;
      padding: 15px;
      border-radius: 10px;
      transition: transform 0.3s ease, background-color 0.3s ease;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }

    .benefits-list li:hover {
      transform: translateX(10px);
      background-color: #3c6e71;
      color: #fff;
    }

    .benefits-list li strong {
      color: #ff5722;
    }

    .benefits-list li:nth-child(even) {
      background-color: #e0f7fa;
    }

    .benefits-list li:nth-child(odd) {
      background-color: #ffe0b2;
    }

    #hierbasRelax {
      background-color: #f4e1d2;
      border-radius: 20px;
      padding: 30px;
      margin-top: 50px;
      animation: slideInLeft 1s ease-out;
      box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    }

    @keyframes slideInLeft {
      0% {
        transform: translateX(-100%);
      }
      100% {
        transform: translateX(0);
      }
    }

    .herbs-list ul {
      list-style-type: none;
      padding: 0;
    }

    .herbs-list li {
      background-color: #ffffff;
      padding: 15px;
      margin-bottom: 15px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      font-size: 1.1em;
      transition: background-color 0.3s ease, transform 0.3s ease;
    }

    .herbs-list li:hover {
      background-color: #3c6e71;
      color: #fff;
      transform: translateX(10px);
    }

    .herbs-list li strong {
      color: #ff5722;
    }
  </style>
</head>
<body>

  <header>
    <h1>Relax Total</h1>
    <p>Tu espacio para desconectar, respirar y reconectar contigo mismo</p>
  </header>

  <div class="buttons">
    <button class="relax-button" onclick="mostrarSeccion('meditacion')">🧘 15 minutos RELAX</button>
    <button class="relax-button" onclick="mostrarSeccion('informacionRelax')">Información RELAX</button>
    <button class="relax-button" onclick="mostrarSeccion('hierbasRelax')">Hierbas RELAX</button>
    <button class="relax-button" onclick="mostrarSeccion('beneficiosMeditacion')">Beneficios de la Meditación</button>
  </div>

  <div class="icon">
    <i class="fas fa-leaf"></i> <!-- Icono de una hoja, puedes reemplazarlo con el que desees -->
  </div>

  <div id="meditacion" class="section">
    <h2>Sesión de Relajación</h2>
    <p>Encuentra un lugar cómodo, cierra los ojos y deja que esta meditación guiada te lleve a un estado de calma y conexión interior.</p>
    <div class="video-wrapper">
      <iframe src="https://www.youtube.com/embed/aBsnQjJ2_Nk" title="Meditación guiada en español" allowfullscreen></iframe>
    </div>
  </div>

  <div id="informacionRelax" class="section">
    <h2>¿Qué es la Meditación?</h2>
    <p>La meditación es una práctica que consiste en entrenar la mente para enfocarse en algo, como la respiración, para reducir el estrés y mejorar el bienestar. Es una medicina complementaria que puede ayudar a mejorar la salud mental y física.</p>
  </div>

  <div id="hierbasRelax" class="section">
    <h2>Hierbas RELAX y sus Propiedades</h2>
    <div class="herbs-list">
      <ul>
        <li><strong>Valeriana:</strong> Sedante del sistema nervioso central, ayuda a prevenir trastornos del sueño</li>
        <li><strong>Manzanilla:</strong> Ansiolítica, ayuda a combatir el estrés</li>
        <li><strong>Lavanda:</strong> Sedante y ansiolítica, mejora la calidad del descanso</li>
        <li><strong>Melisa:</strong> Ansiolítica, ayuda a combatir el estrés</li>
        <li><strong>Tila:</strong> Analgésica, ayuda a tratar dolores de cabeza, de garganta y menstruales</li>
        <li><strong>Pasiflora:</strong> Calmante, ayuda a prevenir trastornos del sueño</li>
        <li><strong>Kava:</strong> Algunas personas la usan como tratamiento a corto plazo para la ansiedad</li>
        <li><strong>Toronjil:</strong> Usada en infusiones relajantes</li>
        <li><strong>Cedrón:</strong> Controla las reacciones alérgicas y los dolores reumáticos</li>
        <li><strong>Menta:</strong> Contiene mentol, una sustancia con propiedades sedantes que ayuda a relajar los músculos</li>
      </ul>
    </div>
  </div>

  <div id="beneficiosMeditacion" class="section">
    <h2>Beneficios de la Meditación</h2>
    <div class="benefits-list">
      <ul>
        <li><strong>Reducir el estrés:</strong> La meditación puede ayudar a reducir los niveles de cortisol, la hormona del estrés.</li>
        <li><strong>Mejorar el sueño:</strong> Meditar puede ayudar a calmar la mente y a conciliar el sueño.</li>
        <li><strong>Aumentar la concentración:</strong> La meditación puede ayudar a mejorar la atención y a centrarse en el presente.</li>
        <li><strong>Desarrollar la empatía y la compasión:</strong> La meditación puede ayudar a ser más amable consigo mismo y más cariñoso con los demás.</li>
        <li><strong>Mejorar la memoria:</strong> La meditación puede ayudar a mejorar la memorización y a combatir la pérdida de memoria.</li>
        <li><strong>Mejorar el sistema inmunológico:</strong> La meditación puede ayudar a reforzar el sistema inmunológico.</li>
        <li><strong>Mejorar el sistema circulatorio:</strong> La meditación puede ayudar a mejorar la circulación sanguínea.</li>
        <li><strong>Mejorar el sistema digestivo:</strong> La meditación puede ayudar a mejorar el sistema digestivo.</li>
        <li><strong>Mejorar el sistema muscular:</strong> La meditación puede ayudar a reducir la sensación de fatiga muscular.</li>
        <li><strong>Aumentar la creatividad:</strong> La meditación puede ayudar a generar nuevas ideas.</li>
      </ul>
    </div>
  </div>

  <script>
    function mostrarSeccion(id) {
      document.querySelectorAll('.section').forEach(sec => {
        sec.classList.remove('active');
      });
      document.getElementById(id).classList.add('active');
    }
  </script>

</body>
</html>
