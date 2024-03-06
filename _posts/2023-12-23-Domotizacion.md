---
title: "Sistema de domotización y seguridad"
excerpt: "Implementación de un sistema de domotización y seguridad para una vivienda"
header:
  teaser: "/assets/images/domotizacion.jpeg"
categories:
  - Proyecto
youtubeId1: BiXpL_gcFss
youtubeId2: vt2IA4Rqax4
youtubeId3: MEl0prDx8tg

---

<style>
    body {
    text-align: justify;
    }
    p {
    margin-bottom: 20px;
    }
    .contenedor {
      text-align: center; /* Centra los elementos dentro del contenedor */
      margin-bottom: 20px;
    }
    /* Estilos para el botón */
    .boton {
      display: inline-block;
      padding: 10px 20px;
      background-color: #4CAF50; /* Color de fondo */
      color: white; /* Color del texto */
      text-align: center;
      text-decoration: none;
      font-size: 16px;
      cursor: pointer;
      border-radius: 5px; /* Bordes redondeados */
      border: none; /* Sin borde */
      transition: background-color 0.3s; /* Transición suave del color de fondo */
      margin-bottom: 20px; /* Agrega un margen inferior para separar el botón del texto */
    }

    /* Cambio de color al pasar el ratón sobre el botón */
    .boton:hover {
      background-color: #45a049; /* Color de fondo cuando se pasa el ratón */
    }
    /* Agrega margen inferior a los contenedores de video de YouTube */
  .video-container {
    margin-bottom: 20px;
  }

</style>

<div style="display: flex; justify-content: center;">
  <img src="../../assets/images/domotizacion.jpeg" alt="Imagen 2" style="width: 100%; height: auto; margin: 10px;">
</div>

# Objetivo

En la era digital actual, la conectividad y la automatización desempeñan un papel fundamental en la transformación de nuestros hogares en entornos inteligentes y seguros.  De este modo, este proyecto implementa un sistema de sensores inteligentes para la monitorización y actuación sobre diferentes elementos del hogar. Además, el sistema también incorpora una parte dedicada exclusivamente a la seguridad, tanto de cara a robos o allanamientos, implementando cámaras de seguridad, sensores de movimiento y alarmas, como también de cara a fugas de gas e incendios, añadiendo sensores de gas y humo.

Para llevar a cabo dicho objetivo, se ha hecho uso de herramientas como NodeRed, DuckDNS, Docker, Portainer, NginxProxyManager y Arduino. Además, gracias al uso de estas herramientas se ha podido llevar a cabo una gestión segura de la red local para poder acceder al sistema sin necesidad de estar en casa. Esto ha sido posible gracias a la implantación de un servidor local propio instaurado en una Raspberry Pi 3b+.

El sistema de seguridad está compuesto principalmente por una cámara con un sistema de movimiento que permite la visualización del entorno en 360 grados. Debido a la extensión de la documentación de dicho dispositivo, se ha creado un post a parte al cual puede accederse haciendo click en el siguiente botón.

<div class="contenedor">
  <button class="boton" onclick="window.open('https://dxvidlf.github.io/me/proyecto/Camara/', '_blank')">Ver proyecto de cámara móvil</button>
</div>

La documentación detallada de todo el proceso de creación del proyecto puede encontrarse en mi perfil de github o haciendo click directamente en el siguiente botón.

<div class="contenedor">
  <button class="boton" onclick="window.open('https://github.com/dxvidlf/Sistema-de-domotizacion-y-seguridad-de-una-vivienda', '_blank')">Ver documentación completa del proyecto</button>
</div>

# Integración del sistema con Telegram

Para la integración del sistema de domotización y seguridad con Telegram, se ha creado un bot denominado "Ultrahouse 3000", el cual gestionará todas nuestras peticiones a través de la aplicación y nos informará de los sucesos que acontecen en nuestra vivienda.

<div style="display: flex; justify-content: center;">
  <img src="../../assets/images/ultrahouse3000.png" alt="Imagen 2" style="width: 30%; height: auto; margin: 10px;">
</div>

Mediante una interfaz de usuario conformada por menús que se despliegan al interaccionar con los botones de los mensajes, podemos realizar una gran variedad de acciones, siendo estas las que aparecen en las siguientes imágenes.

<div style="display: flex; justify-content: center;">
  <img src="../../assets/images/menus.png" alt="Imagen 2" style="width: 60%; height: auto; margin: 10px;">
</div>

La ejecución real del sistema en Telegram puede verse en el siguiente video, donde el usuario interacciona con el bot de Telegram requiriendo todas las opciones posibles que ofrecen los menús de acción de la parte de domótica y seguridad.

<div class="video-container">
  {% include youtubePlayer.html id=page.youtubeId1 %}
</div>

# Integración del sistema con NodeRed

NodeRed es una parte fundamental de este proyecto, dado que toda la lógica de funcionamiento que gestiona las peticiones y notificaciones al usuario son gestionadas a través de él. Además, su dashboard nos ofrece una amplia gama de opciones disponibles para configurar una interfaz de usuario amigable con la que interactuar. 

En este proyecto se han desarrollado cuatro secciones en las que el usuario puede gestionar su vivienda, encontrándose en la última de ellas el video en directo de la cámara de seguridad y una serie de botones que permiten la interacción con el sistema de movimiento de la misma. El resto de secciones están destinadas al control de la domótica de la vivienda y la visualización de todos los datos guardados referentes a la misma. Dichos datos son gestionados mediante bases de datos conformadas en MondoDB, integrado a su vez en NodeRed.

La ejecución real del sistema en NodeRed referente a las tres primeras secciones del mismo puede verse en el siguiente video.

<div class="video-container">
  {% include youtubePlayer.html id=page.youtubeId2 %}
</div>

La ejecución real del sistema en NodeRed referente a la sección de la cámara de seguridad puede verse en el siguiente video.

<div class="video-container">
  {% include youtubePlayer.html id=page.youtubeId3 %}
</div>
