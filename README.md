# Visual-Comunication
<!DOCTYPE html>
<html lang="en">
<head>
<script type="text/javascript" src="https://nicolasserrano.github.io/tools/libraries/setIframesForPanopto.js"></script>
<link rel="stylesheet" type="text/css" href="https://nicolasserrano.github.io/tools/libraries/material.css" />
<script>
window.onload = start;
function start() {
    var urlSearch = window.location.search.substring(1);
    if (urlSearch == null || urlSearch.length == 0) {
      urlSearch = "https://raw.githubusercontent.com/nicolasserrano/CS/master/JDBC.md";
    }
    ids=urlSearch.split(",");
    var i;
    for (i = 0; i < ids.length; i++) {
        expandPanel(document.getElementById(ids[i]), true)
    }
}

function expand(id) {
  var x = document.getElementById(id);
  if (x.className.indexOf("w3-show") == -1) {
    x.className += " w3-show";
    x.previousElementSibling.className = 
    x.previousElementSibling.className.replace("w3-theme-d1", "w3-theme-d4");
    x.previousElementSibling.className.replace("w3-theme-l4", "w3-theme-l5");
  } else { 
    x.className = x.className.replace(" w3-show", "");
    x.previousElementSibling.className = 
    x.previousElementSibling.className.replace("w3-theme-d4", "w3-theme-d1");
    x.previousElementSibling.className.replace("w3-theme-l5", "w3-theme-l4");
  }
}
</script>
<style>
img.w3-image {
    width: 930px;
    height: 340px;
}
.w3-card P {
    margin-top: -10px;
}
.fa {
display:inline-block;
font:normal normal normal 14px/1 FontAwesome;
font-size:inherit;
text-rendering:auto;
-webkit-font-smoothing:antialiased;
-moz-osx-font-smoothing:grayscale;
transform:translate(0, 0);
}
</style>
<title>W3.CSS Template</title>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="w3.css">
<!-- Theme Indigo
<link rel="stylesheet" href="http://www.w3schools.com/w3css/4/w3.css">
https://www.w3schools.com/w3css/tryit.asp?filename=tryw3css_theme_indigo
<link rel="stylesheet" href="http://www.w3schools.com/lib/w3-theme-indigo.css">
 -->
<link rel="stylesheet" href="w3-theme-indigo.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
</head>
<body>

<!-- Header -->
<header class="w3-display-container w3-content w3-center" >
  <img class="w3-image" src="images/CCDcover.jpg" alt="CCD" ">
    <!-- 
  <div class="w3-display-middle w3-padding-large w3-border w3-wide w3-text-light-grey w3-center">
    <h1 class=" w3-hide-medium w3-hide-small w3-xxxlarge">Curso de </h1>
    <h5 class="w3-hide-large" style="white-space:nowrap">JANE DOE</h5>
    <h3 class="w3-hide-medium w3-hide-small">Tecnun</h3>
  </div>
    Header -->
  
  <!-- Navbar (placed at the bottom of the header image) -->
  <div class="w3-bar w3-light-grey w3-round w3-display-bottommiddle w3-hide-small" style="bottom:-16px">
    <a href="#" class="w3-bar-item w3-button">Inicio</a>
    <a href="#portfolio" class="w3-bar-item w3-button">Contenido</a>
    <a href="#temas" class="w3-bar-item w3-button">Temas</a>
    <a href="#contact" class="w3-bar-item w3-button">Contacto</a>
  </div>
</header>

<!-- Navbar on small screens -->
<div class="w3-center w3-light-grey w3-padding-16 w3-hide-large w3-hide-medium">
<div class="w3-bar w3-light-grey">
  <a href="#" class="w3-bar-item w3-button">Inicio</a>
  <a href="#portfolio" class="w3-bar-item w3-button">Contenido</a>
  <a href="#temas" class="w3-bar-item w3-button">Temas</a>
  <a href="#contact" class="w3-bar-item w3-button">Contacto</a>
</div>
</div>


<!-- Page content -->
<div class="w3-content w3-padding-large w3-margin-top" id="portfolio">

<!-- Page presentacion -->
<div class="w3-panel w3-card">
<P></P>
<P>&nbsp;&nbsp;&nbsp;&nbsp;Las sesiones de este curso permitir&aacute;n familiarizarse con las herramientas para la generaci&oacute;n de contenido digital. Las sesiones de im&aacute;genes tratan de los distintos tipos de im&aacute;genes, los controles de una c&aacute;mara fotogr&aacute;fica que se usar&aacute; tambi&eacute;n en las sesiones de video, la edici&oacute;n de im&aacute;genes y su utilizaci&oacute;n en distintos modos de presentaci&oacute;n.</P>
<P>&nbsp;&nbsp;&nbsp;&nbsp; Los temas de publicaci&oacute;n Web permitir&aacute;n entender como se gestionan dichos contenidos y manipularlos utilizando los distintos editores y plataformas pero teniendo control del contenido generado.</P>
<P>&nbsp;&nbsp;&nbsp;&nbsp; Las sesiones de video tratan los distintos modos de captura y edici&oacute;n de video, desde la captura online a la edici&oacute;n con composici&oacute;n y aplicaci&oacute;n de filtros.</P>
<P>&nbsp;&nbsp;&nbsp;&nbsp; La realidad virtual permite la generaci&oacute;n y representaci&oacute;n de objetos y entidades en 3 dimensiones, para la generaci&oacute;n de im&aacute;genes, videos o publicaci&oacute;n en la Web.</p></div>

<a onclick="setVideoIcons(this)" href="javascript:void(0);">Mostrar vista previa de videos</a><select id="iframeSize" name="ifsize" size="1">
<option value="100">100</option>
<option value="200">200</option>
<option value="400" selected="selected">400</option>
<option value="600">600</option>
<option value="720">720</option>
<option value="800">800</option>
<option value="1080">1080</option>
</select>

<a onclick=expandAll() style='float: right'>Expand all &nbsp;<i class="accIcon fa fa-caret-down"></i></a>
<!-- Temas -->
<div class="w3-content w3-padding-large w3-margin-top" id="temas">

<div class="w3-button w3-border w3-round-large w3-block w3-theme w3-left-align">
<span class="w3-xlarge"><i class="w3-margin-left fa fa-picture-o"></i></span> Im&aacute;genes </div>
<div id="S1" class="w3-container">

<ul class="w3-ul w3-border">
<LI id="S1.1" class="w3-theme-l4 w3-border"> Imágenes y Fotografía</LI>
<div class="panel w3-container w3-border">
    Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=dd881b8d-18dc-491b-b6c5-abdc012c9b7d' target='_blank'>v01 Ficheros</a><BR>
    Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=b84a6fc8-e833-4c9a-9802-abdc012ee0cb' target='_blank'>v02 Ficheros en Panopto</a><BR>
    Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=7d1aca6d-fed3-4671-892b-abde01262535' target='_blank'>v03 Tipos de imagenes y repositorios</a><BR>
    Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=417e26cd-6015-4aa8-b091-abdf00820d24' target='_blank'>v04 Fotografia teoria</a><BR>
</div>


<LI id="S1.2" class="w3-theme-l4 w3-border"> Edición de imágenes  </LI>
<div class="panel w3-container w3-border">
    Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=8f8aa051-8d4c-4f3b-a087-abdf00bc32d7' target='_blank'>ed01 Captura</a><BR>
    Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=bcb331a3-9921-4ea8-bd2f-abdf00bdf407' target='_blank'>ed02 Editor Pixlr e</a><BR>
    Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=1b25ba15-355e-4da8-82b1-abdf00c19a85' target='_blank'>ed03 Capas</a><BR>
                                         
<table border=1>
<tr><td>
       <br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=cbJd47mUZe0&amp;t=4s" dir="auto">0:04</a><span dir="auto" class="style-scope yt-formatted-string"> 1. Arrange
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=cbJd47mUZe0&amp;t=27s" dir="auto">0:27</a><span dir="auto" class="style-scope yt-formatted-string"> 2. Marquee Select
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=cbJd47mUZe0&amp;t=42s" dir="auto">0:42</a><span dir="auto" class="style-scope yt-formatted-string"> 3. Lasso Select
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=cbJd47mUZe0&amp;t=67s" dir="auto">1:07</a><span dir="auto" class="style-scope yt-formatted-string"> 4. Lasso Select
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=cbJd47mUZe0&amp;t=77s" dir="auto">1:17</a><span dir="auto" class="style-scope yt-formatted-string"> 5. Crop
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=cbJd47mUZe0&amp;t=86s" dir="auto">1:26</a><span dir="auto" class="style-scope yt-formatted-string"> 6. Shape Cutout
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=cbJd47mUZe0&amp;t=131s" dir="auto">2:11</a><span dir="auto" class="style-scope yt-formatted-string"> 7. Magic Cutout
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=cbJd47mUZe0&amp;t=157s" dir="auto">2:37</a><span dir="auto" class="style-scope yt-formatted-string"> 8. Draw Cutout
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=cbJd47mUZe0&amp;t=193s" dir="auto">3:13</a><span dir="auto" class="style-scope yt-formatted-string"> 9. Lasso Cutout
</span>
</td><td>
       <br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=FkoBrJe0FEs&amp;t=4s" dir="auto">0:04</a><span dir="auto" class="style-scope yt-formatted-string"> 10. Push
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=FkoBrJe0FEs&amp;t=19s" dir="auto">0:19</a><span dir="auto" class="style-scope yt-formatted-string"> 11. Enlarge
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=FkoBrJe0FEs&amp;t=35s" dir="auto">0:35</a><span dir="auto" class="style-scope yt-formatted-string"> 12. Shrink
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=FkoBrJe0FEs&amp;t=50s" dir="auto">0:50</a><span dir="auto" class="style-scope yt-formatted-string"> 13. Swirl Right
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=FkoBrJe0FEs&amp;t=63s" dir="auto">1:03</a><span dir="auto" class="style-scope yt-formatted-string"> 14. Swirl Left
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=FkoBrJe0FEs&amp;t=76s" dir="auto">1:16</a><span dir="auto" class="style-scope yt-formatted-string"> 15. Restore
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=FkoBrJe0FEs&amp;t=87s" dir="auto">1:27</a><span dir="auto" class="style-scope yt-formatted-string"> 16. Heal
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=FkoBrJe0FEs&amp;t=105s" dir="auto">1:45</a><span dir="auto" class="style-scope yt-formatted-string"> 17. Clone
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=FkoBrJe0FEs&amp;t=120s" dir="auto">2:00</a><span dir="auto" class="style-scope yt-formatted-string"> 18. Blur
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=FkoBrJe0FEs&amp;t=133s" dir="auto">2:13</a><span dir="auto" class="style-scope yt-formatted-string"> 19. Sharpen
</span>
</td><td>
        <br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=V8SDgwVrn2c&amp;t=4s" dir="auto">0:04</a><span dir="auto" class="style-scope yt-formatted-string"> 20. Lighten
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=V8SDgwVrn2c&amp;t=21s" dir="auto">0:21</a><span dir="auto" class="style-scope yt-formatted-string"> 21. Darken
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=V8SDgwVrn2c&amp;t=30s" dir="auto">0:30</a><span dir="auto" class="style-scope yt-formatted-string"> 22. Vibrance (Increase)
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=V8SDgwVrn2c&amp;t=52s" dir="auto">0:52</a><span dir="auto" class="style-scope yt-formatted-string"> 23. VIbrance (Decrease)
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=V8SDgwVrn2c&amp;t=72s" dir="auto">1:12</a><span dir="auto" class="style-scope yt-formatted-string"> 24. Saturation (Increase)
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=V8SDgwVrn2c&amp;t=90s" dir="auto">1:30</a><span dir="auto" class="style-scope yt-formatted-string"> 25. Saturation (Decrease)
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=V8SDgwVrn2c&amp;t=114s" dir="auto">1:54</a><span dir="auto" class="style-scope yt-formatted-string"> 26. Temperature (Increase)
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=V8SDgwVrn2c&amp;t=134s" dir="auto">2:14</a><span dir="auto" class="style-scope yt-formatted-string"> 27. Temperature (Decrease)
</span>
</td><td>
        <br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=33ngjuyEiaE&amp;t=4s" dir="auto">0:04</a><span dir="auto" class="style-scope yt-formatted-string"> 28. Pen
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=33ngjuyEiaE&amp;t=25s" dir="auto">0:25</a><span dir="auto" class="style-scope yt-formatted-string"> 29. Draw
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=33ngjuyEiaE&amp;t=44s" dir="auto">0:44</a><span dir="auto" class="style-scope yt-formatted-string"> 30. Eraser
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=33ngjuyEiaE&amp;t=61s" dir="auto">1:01</a><span dir="auto" class="style-scope yt-formatted-string"> 31. Fill
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=33ngjuyEiaE&amp;t=68s" dir="auto">1:08</a><span dir="auto" class="style-scope yt-formatted-string"> 32. Shape
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=33ngjuyEiaE&amp;t=86s" dir="auto">1:26</a><span dir="auto" class="style-scope yt-formatted-string"> 33. Text
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=33ngjuyEiaE&amp;t=126s" dir="auto">2:06</a><span dir="auto" class="style-scope yt-formatted-string"> 34. Picker
</span><br><a class="yt-simple-endpoint style-scope yt-formatted-string" spellcheck="false" href="https://www.youtube.com/watch?v=33ngjuyEiaE&amp;t=136s" dir="auto">2:16</a><span dir="auto" class="style-scope yt-formatted-string"> 35. Zoom
</span>

</td></tr>
</table>

</div>

<LI id="S1.3" class="w3-theme-l4 w3-border"> Creación de presentaciones </LI>
<div class="panel w3-container w3-border">
    Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=2892396c-8b3e-4a45-b1ea-abd6006f7afe' target='_blank'>v01 Presentaciones</a><BR>
    Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=ac6cbc50-6291-4a5f-9185-abe10113d586' target='_blank'>v02 Presentaciones - Internet</a><BR>
    Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=f5562ee4-e2d8-4d69-b92a-abe1011817b1' target='_blank'>v03 Presentaciones Indice</a><BR>
    Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=06e50369-56cb-4467-89c1-abe1011a0fb7' target='_blank'>v04 Presentaciones Ejemplos</a><BR>
    doc <a href="http://www.nicolasserrano.com/viscom/CreacionPresentaciones.pdf" target="_blank">Presentación sobre "Creacion de presentaciones"<br></a><BR>
</div>

</ul>
</div>

<div class="w3-button w3-border w3-round-large w3-block w3-theme w3-left-align">
<span class="w3-xlarge"><i class="w3-margin-left fa fa-laptop"></i></span> Publicaci&oacute;n Web </div>
<div id="S2" class="w3-container">
<ul class="w3-ul w3-border">
<LI id="S2.1" class="w3-theme-l4 w3-border"> Páginas Web y HTML</LI>

<div class="panel w3-container w3-border">
<p>Documento&nbsp;(p&aacute;ginas 3b,&nbsp;5a y 7b):<a href="https://aula-virtual.unav.edu/bbcswebdav/pid-1218284-dt-content-rid-2850890_1/xid-2850890_1" target="_blank">El camino a la Era Digital</a><br />
Video&nbsp;<a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=2ef91361-131f-436f-beb4-ab6d011ad559" target="_blank">Elementos de la Web</a><br />
Video&nbsp;<a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=86e27b00-6515-49d2-a5f5-ab6e00f0cd08" target="_blank">Estructura de un navegador</a><br />
Video opcional:&nbsp;<a href="https://www.antena3.com/noticias/embed/internet-celebra-su-30-aniversario/video/41/2019/03/12/5c8819887ed1a8b6edc594a1" target="_blank">30&nbsp;aniversario de la Web (Antena 3)</a><br />
Video&nbsp;<a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=64afd13a-4aea-47dc-8593-ab7601767302" target="_blank">Primera p&aacute;gina web (CERN)</a>&nbsp;-&nbsp;doc&nbsp;<a href="http://info.cern.ch/hypertext/WWW/WhatIs.html" target="_blank">First web page</a><br />
Video&nbsp;<a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=2fb95719-4ed6-4259-91fb-ab7600fb3d59" target="_blank">Crear primera p&aacute;gina Web</a><br />
Video&nbsp;<a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=e8c18503-3cf7-4d7f-ab45-ab7600fc04ad" target="_blank">Curso b&aacute;sico de HTML</a>&nbsp;-&nbsp; doc&nbsp;&nbsp;<a href="http://www.nicolasserrano.com/CS/HTML/CursoHTML.html" target="_blank">Curso HTML</a></p>
</div>

<LI id="S2.2" class="w3-theme-l4 w3-border"> Estilo de páginas Web, CSS y Frameworks</LI>
<div class="panel w3-container w3-border">
<p>Video&nbsp;<a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=617d4e62-8495-4cf5-8ff2-ab80010fc388" target="_blank">1.&nbsp;Presentación</a>&nbsp;-&nbsp;doc <a href="http://nicolasserrano.github.io/viscom/Arte.pdf" target="_blank">Que es el arte&nbsp;</a><br>
   Video&nbsp;<a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=8cec7bab-8eb9-4c8f-8f4f-ab7f00bbf5f6" target="_blank">2. Introducción</a>&nbsp;-&nbsp;doc <a href="http://nicolasserrano.github.io/viscom/CSS.html#/0" target="_blank">presentación&nbsp;</a><a href="http://nicolasserrano.github.io/viscom/CSS.html#/0" target="_blank">CSS</a><br>
   Video&nbsp;<a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=6b8eadc2-9e6a-4258-b374-ab7f00c2d74e" target="_blank">3. Fuentes</a>&nbsp;- web <a href="http://www.typetester.org/" target="_blank">typetester</a> ,<a href="http://www.thinkingwithtype.com/contents/letter/" target="_blank" shape="rect" rel="noopener">Letter Anatomy</a><br>
   Video&nbsp;<a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=a77c0239-87f0-4ee9-9b62-ab7f00cbdb6e" target="_blank">4. Color</a>&nbsp;-&nbsp;web <a href="http://paletton.com/" target="_blank">Paletton</a> &nbsp;, web <a href="https://color.adobe.com/">Adobe Color</a><br>
   Video&nbsp;<a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=882d4808-b7f3-419a-956a-ab7f00c6b86c" target="_blank">5. Aplicación estilo CSS en página Web</a>&nbsp;- docs: <a href="https://github.com/nicolasserrano/CS/blob/master/CSS/TestCSS_ini.html" target="_blank">html initial </a>-&nbsp;<a href="https://github.com/nicolasserrano/CS/blob/master/CSS/TestCSS_fin.html" target="_blank">html final</a><br>
   Video&nbsp;<a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=8a9ec0ed-de77-4d10-91d7-ab7f00cf2a17" target="_blank">6. Modelo de cajas</a>&nbsp;-&nbsp;web <a href="https://hicks.design/journal/3d-css-box-model" target="_blank">boxmodel</a><br>
   Video&nbsp;<a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=9bb839a7-1466-4106-900a-ab7f00cdc1e9" target="_blank">7. Utilidades</a>&nbsp;-&nbsp;web <a href="http://www.csszengarden.com/" target="_blank">CSS Zen Garden</a><br>
   Video&nbsp;<a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=b1c192a3-5125-43a7-a501-ab7f00d3d296" target="_blank">8. Frameworks</a>&nbsp;-&nbsp;web <a href="https://www.w3schools.com/w3css/" target="_blank">W3.CSS</a><br>
<br>
Video opcional <a href="https://edu.gcfglobal.org/en/beginning-graphic-design/typography/1/" target="_blank">Typography</a>&nbsp;(video 6' y p&aacute;gina Web)<br>
Video opcional <a href="https://edu.gcfglobal.org/en/beginning-graphic-design/color/1/" target="_blank">Color</a> (video 6' y p&aacute;gina Web)</span><br>
Video opcional <a href="https://edu.gcfglobal.org/en/beginning-graphic-design/layout-and-composition/1/" target="_blank">Composition & layout</a><br>
                                                                                                                     
</p>
<p>
   doc <a href="http://www.nicolasserrano.com/CS/CSS/CSS.pdf" target="_blank">Referencia CSS<br></a></p> 
  </div>
<LI id="S2.3" class="w3-theme-l4 w3-border">  Interacción en páginas Web, JavaScript</LI>
<div class="panel w3-container w3-border">
    <p>Video <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=14071372-9a58-447d-9f03-ab97009e688e" target="_blank">1. Expresiones y variables en JavaScript</a>
        - doc <a href="https://nicolasserrano.github.io/CS/JavaScript/JavascriptOnePage.pdf" target="_blank">JavaScript in One Page</a><br>
    Video <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=c5d6f172-88c8-4436-a858-ab9700a10100" target="_blank">2. Funciones en JavaScript</a><br>
    Video <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=129ce087-a908-4eac-8a94-ab9700a38c83" target="_blank">3. Ejemplo función en JavaScript</a><br>
    Video <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=72e81449-e01b-4772-b539-ab9700a65831" target="_blank">4. Condiciones en JavaScript</a><br>
    Video <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=45cae973-875b-4858-96d7-ab9700a789c0" target="_blank">5. Bucles en JavaScript</a><br>
    Video <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=33caebdd-5482-400e-9c1b-ab9700a8ab81" target="_blank">6. Vectores en JavaScript</a>
    <hr>
    Video <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=233e2018-ead2-4657-b7d2-ab9700a9f852" target="_blank">7. Objetos en JavaScript</a><br>
    Video <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=8f538e51-d1e3-4271-b38b-ab9700af34c7" target="_blank">8. JavaScript en ficheros HTML</a>
        - <a href="https://github.com/nicolasserrano/CS/blob/master/JavaScript/secant.html" target="_blank">code secant.html</a>
        - <a href="https://nicolasserrano.github.io/CS/JavaScript/secant.html" target="_blank">execute secant.html</a><br>
    Video  <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=14966b44-c83c-46ae-b636-ab9700b19203" target="_blank">9. Ejemplos JavaScrip en pagina HTML</a>
        - <a href="https://github.com/nicolasserrano/CS/blob/master/JavaScript/JavaScript1.html" target="_blank">examples code</a>
        - <a href="https://nicolasserrano.github.io/CS/JavaScript/JavaScript1.html" target="_blank">examples execute</a><br>
    Video <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=e7106efb-9654-4e62-9aca-ab9700b39d08" target="_blank">10. Ejemplos manipulacion DOM</a><br>
    Video opcional <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=69b3a602-fcbc-435d-a099-ab9700ba5248" target="_blank">11. JSON</a>
        - <a href="https://nicolasserrano.github.io/CS/JavaScript#json" target="_blank">JSON</a><br></p>
  </div>
</ul>
</div>

<div class="w3-button w3-border w3-round-large w3-block w3-theme w3-left-align">
<span class="w3-xlarge"><i class="w3-margin-left fa fa-video-camera"></i></span>&nbsp; Video</div>
<div id="S3" class="w3-container">
<ul class="w3-ul w3-border">
<LI id="S3.1" class="w3-theme-l4 w3-border">   Grabación, edición y publicación de video con Panopto   &nbsp; </LI>
  <div class="panel w3-container w3-border">
    <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=f8246d24-f64e-4bd2-8cc5-ab7c009cef97" target='_blank'>1. Introducción Panopto</a><BR>
    <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=3cbaf61b-810f-4a0a-a070-ab7b00b767dc" target='_blank'>2. Instalación (Calidad e Innovación UNAV)</a><BR>
    <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=54efa5bb-8a80-41b1-b9d2-ab7c00a74975" target='_blank'>3. Acceso a Panopto</a><BR>
    <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=48d8b62c-c46a-441a-af82-ab7c00a85e96" target='_blank'>4. Permisos</a><BR>
    <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=3c2c1072-7da0-4a62-99f0-ab7b00b767a5" target='_blank'>5. Grabación  (Calidad e Innovación UNAV)</a><BR>
    <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=4ef23714-10cd-420e-a893-ab8000c3a488" target='_blank'>5b. Grabación con segunda pantalla</a><BR>
    <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=876c336b-2e5e-4ea4-bfea-abe900f73b5a" target='_blank'>5c. Uso de tabletas gráficas</a><BR>
    <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=0acf667b-3d4b-4882-957b-ab7c00aa11ca" target='_blank'>6. Creación de carpeta y grabación 2 pantallas</a><BR>
    <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=c52786da-c431-4f68-ac52-ab7f00b1a68c" target='_blank'>7. Edición</a><BR>
    <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=ab5aedd7-b642-40c3-90d5-ab7b00b767fc" target='_blank'>8. Compartir (Calidad e Innovación UNAV)</a><BR>  
  </div>
<LI id="S3.2" class="w3-theme-l4 w3-border"> Composición y grabación de video con OBS </LI>
  <div class="panel w3-container w3-border">
    Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=7f7f9a46-1657-4ca3-a2ab-abe20103437e' target='_blank'>Grabación con OBS</a><BR>
    Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=6c90c623-bb10-491b-89d4-abe20117a40e' target='_blank'>Pantalla y cámara con OBS</a><BR>
    Video <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=e0d525ef-a60a-4004-b878-ab7c009e11ef">Grabación con Lightboard</a><BR>
    doc <a href="http://www.nicolasserrano.com/viscom/TutorialOBS.pdf" target="_blank">Tutorial para grabar la pantalla con OBS<br></a><BR>
  </div>
<LI id="S3.3" class="w3-theme-l4 w3-border"> Edición de video (Shotcut) </LI>
  <div class="panel w3-container w3-border">
  Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=13602344-b15c-4371-8496-abe2011cad8d' target='_blank'>ShotCut v01</a><BR>
  Shotcut Video Editor - Tutorial for Beginners <a href='https://www.youtube.com/watch?v=P9pzmzXj03A&t=404s' target='_blank'>YouTube tutorial (filters, titles and keyframes)</a><BR>
  <a href="https://guides.lib.uoguelph.ca/Shotcut" target='_blank'>Web tutorial</a><BR>
  <a href="https://www.shotcut.org/tutorials/" target='_blank'>Shotcut official Tutorial Videos</a><BR>
  </div>
  
</ul>
</div>

<div class="w3-button w3-border w3-round-large w3-block w3-theme w3-left-align">
<span class="w3-xlarge"><i class="w3-margin-left fa fa-object-ungroup"></i></span>&nbsp;  Realidad Virtual </div>
<div id="S4" class="w3-container">

<ul class="w3-ul w3-border">
<LI id="S4.1" class="w3-theme-l4 w3-border"> La geometría de los objetos 3D </LI>
  <div class="panel w3-container w3-border">
  <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=51b459c2-7d90-4137-8e53-abed00c50cdd" target='_blank'>1. Instalación</a><BR>
  <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=18b4760c-d8c1-4663-91ee-abed00c510bd" target='_blank'>2. Interface</a><BR>
  <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=43d12940-d75b-45b7-8336-abed00c50ca5" target='_blank'>3. Modo objeto</a><BR>
  <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=64ee8966-dc17-427f-b141-abed00c50c4f" target='_blank'>4. Modo edición</a><BR>
  <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=d48338ee-a3d0-42aa-828e-ac63010a5195" target='_blank'>5. Importación de objetos</a><BR>
  Presentaci&oacute;n <a href='https://www.nicolasserrano.com/viscom/CG.pdf' target='_blank'>Computer Graphics</a><BR>
  </div>
<LI id="S4.2" class="w3-theme-l4 w3-border"> Materiales, luz y color </LI>
  <div class="panel w3-container w3-border">
  Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=2fa7df81-f27a-48a2-a304-ac69009f1315' target='_blank'>CG01. Luz</a><BR>
  Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=d6f9cd13-550b-469d-a615-ac6b011e0cc8' target='_blank'>CG02. Color</a><BR>
  Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=9812529f-cb25-4cc3-a65c-ac6b011f25fc' target='_blank'>CG03. Espacios de color</a><BR>
  Video <a href='https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=c097d4d9-6959-469d-9ee3-ac630116e40f' target='_blank'>bl_06_materiales</a><BR>
  <hr>
  Adicionales<BR>
  Video <a href="https://www.youtube.com/watch?v=XI-pZshRp8g" target='_blank'>Blender 2.8 PBR Texturing</a> - Material: <a href="https://cc0textures.com/view?id=DiamondPlate001" target='_blank'>DiamondPlate</a><BR>
  Alternative video: <a href="https://www.youtube.com/watch?v=rzXNZkEoTAk">The Basics of Good Texturing in Blender by Blender Guru</a> - doc: <a href="https://help.poliigon.com/en/articles/1712652-what-are-the-different-texture-maps-for" target='_blank'>Different texture maps</a><BR>
  Video <a href="https://www.youtube.com/watch?v=4H5W6C_Mbck" target='_blank'>The Principled BSDF in Blender</a> - Reference <a href="https://disney-animation.s3.amazonaws.com/library/s2012_pbs_disney_brdf_notes_v2.pdf" target='_blank'>Physically-Based Shading at Disney</a><BR>
  Sites for textures: <a href="https://cc0textures.com/" target='_blank'>CC0 textures</a> - <a href="https://www.poliigon.com/search?type=texture" target='_blank'>Poliigon</a> - <a href="https://www.textures.com/" target='_blank'>textures.com</a><BR>
  Docs: <a href="https://marmoset.co/posts/basic-theory-of-physically-based-rendering/" target='_blank'>Basic Theory of PBR in Marmoset</a> - <a href="https://help.sketchfab.com/hc/en-us/articles/204429595-Materials-PBR-" target='_blank'>PBR Materials in Sketchfab</a>  - <a href="https://blog.selfshadow.com/publications/s2015-shading-course/#course_content" target='_blank'>SIGGRAPH 2015 Course: Physically Based Shading in Theory and Practice</a><BR>
  </div>
<LI id="S4.3" class="w3-theme-l4 w3-border"> Animación en 3D </LI>
  <div class="panel w3-container w3-border">
   Video <a href="https://www.youtube.com/watch?v=SZJswvw9wEs" target='_blank'>Animation with keyframes</a><BR>
   Video <a href="https://unav.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=6e733142-41d3-4207-9e39-abfe016618ec" target='_blank'>Blender con Python</a> - doc <a href="https://sinestesia.co/blog/tutorials/python-2d-grid/" target='_blank'>Meshes with Python</a><BR>
   Other tutorials: <a href="https://www.youtube.com/c/Olav3D" target='_blank'>Olav3D Tutorials</a><BR>
  </div>
</ul>
</div>

<style>
i.fa.fa-caret-down, i.fa.fa-caret-up {
    float: right;
}


.panel {
  padding: 0 18px;
  background-color: white;
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.2s ease-out;
}
</style>

<script>
//var acc = document.getElementsByClassName("accordion");
//var acc = document.querySelectorAll("#temas LI, #temas div.w3-button");
//var acc = document.querySelectorAll("#temas div.w3-button");
var acc = document.querySelectorAll("#temas LI");
var i;

for (i = 0; i < acc.length; i++) {
  elem_i = document.createElement("i");
  elem_i.classList.add("accIcon");
  elem_i.classList.add("fa");
  elem_i.classList.add("fa-caret-down");
  acc[i].appendChild(elem_i);
  acc[i].addEventListener("click", function () {expandPanel(this);});
}

function expandPanel(elem, finalState) {
    if (finalState != null) {
        console.log("finalState: " + finalState);
        if (finalState && elem.classList.contains("active")) return;
        if (!finalState && !elem.classList.contains("active")) return;
    }
    elem.classList.toggle("active");
    element_i = elem.querySelector("i.accIcon");
    element_i.classList.toggle("fa-caret-down");
    element_i.classList.toggle("fa-caret-up");
    var panel = elem.nextElementSibling;
    if (panel.style.maxHeight) {
      panel.style.maxHeight = null;
    } else {
      panel.style.maxHeight = panel.scrollHeight + "px";
    } 
}

var expandedAll = false;
function expandAll() {
    expandedAll = !expandedAll;
    var acc = document.querySelectorAll("#temas LI");
    var i;

    for (i = 0; i < acc.length; i++) {
        expandPanel(acc[i], expandedAll);
    }
}
</script>


<!-- Contacto -->
  <div class="w3-light-grey w3-padding-large w3-padding-32 w3-margin-top" id="contact">
    <h5 class="w3-center">Contacto</h5>
<!-- 
    <hr>
 -->

    <div id="links">
    <div class="w3-center"><a  href="http://nicolasserrano.com">Nicolas Serrano</a></div>
© Tecnun. Escuela de Ingenieros. Universidad de Navarra | P° de Manuel Lardizabal, 13. <BR>20018 Donostia-San Sebastián. Gipuzkoa (España).
<script>document.title = "Creacion de Contenidos Digitales"</script>
<!-- Version
v1.07: incluido abrir paneles desde lista de valores en la url, ejemplo ?S3.1,S3.2,S3.3#S3
v1.08: añadido video Uso de tabletas gráficas
 -->
  <small>v1.085
        - <a href=https://github.com/nicolasserrano/nicolasserrano.github.io/edit/master/CCD.html>Edit</a>
        - <a href=http://nicolasserrano.github.io/CCD>View</a>
        - <a href=https://github.com/nicolasserrano/nicolasserrano.github.io/blob/master/CCD.html>File</a>
        - <a href=http://www.nicolasserrano.com/CCD.html?S2.2#S2.2>Reference example</a>
  </small>
        <div class="w3-center" id="logouni">
            <a href="http://www.unav.edu" title="Universidad de Navarra"><span>Universidad de Navarra</span></a>
        </div>
        
    </div>
        
  </div>
<!-- End page content -->
</div>

</body>
</html>
