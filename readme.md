<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>BOLT</title>
  <link rel="stylesheet" href="styles.css">
  <script src="script.js"></script>
  <!-- Añadir Google Maps API -->
  <script async defer src="https://maps.googleapis.com/maps/api/js?key=AIzaSyA9-bmvA0sT-x-FVC3dTqxua81F6uUxAl4&callback=initMap"></script>
  <script>
    // Función para inicializar el mapa
    function initMap() {
      // Coordenadas para Santiago
      var santiago = {lat: -33.4489, lng: -70.6693};
      // Configuración del mapa
      var map = new google.maps.Map(
        document.getElementById('map'), {zoom: 12, center: santiago});
      // Marcador
      var marker = new google.maps.Marker({position: santiago, map: map});
    }
  </script>
</head>
<body>
  <header>
    <h1>BOLT</h1>
  </header>
  
  <nav>
    <ul>
      <li><a href="#">Inicio</a></li>
      <li><a href="#">Productos</a></li>
      <li><a href="#">Calendario</a></li>
      <li><a href="#about-us">Quiénes Somos</a></li>
      <li><a href="#">Contacto</a></li>
    </ul>
  </nav>

  <main>
    <section id="product-selection">
      <h2>Selecciona tu Producto</h2>
      <form id="product-form">
        <label for="store">Tienda:</label>
        <select id="store" name="store" onchange="redirectToStore()">
          <option value="" selected disabled>Elige una tienda</option>
          <option value="falabella">Falabella</option>
          <option value="paris">París</option>
          <option value="easy">Easy</option>
        </select>

        <label for="product">Código del Producto:</label>
        <input type="text" id="product" name="product" placeholder="Ingresa el código del producto">

        <label for="date">Fecha de Entrega:</label>
        <input type="date" id="date" name="date">

        <label for="time">Horario de Entrega:</label>
        <input type="time" id="time" name="time">

        <input type="submit" value="Pedir">
      </form>
    </section>

    <!-- Sección del mapa -->
    <section id="map-section">
      <h2>Zona de Entrega en Santiago</h2>
      <div id="map" style="height: 400px; width: 100%;"></div>
    </section>

    <section id="about-us">
      <h2>Quiénes Somos</h2>
      <p>Somos BOLT, una empresa de envíos rápidos especializada en la entrega de productos de Falabella, París y Easy. Garantizamos que tu pedido llegará en el horario acordado y en perfectas condiciones.</p>
      <p>Presidente: Leandro Barrios</p>
    </section>
  </main>

  <footer>
    <p>Todos los derechos reservados. Envío garantizado en 3 días.</p>
  </footer>
</body>
</html>





