# Misael 
Funciones:

<!DOCTYPE HTML>

<html lang = "en">

<head>

  

  <meta charset = "UTF-8" />

  <script type = "text/javascript">

  //<![CDATA[



  function getLoc(){

    navigator.geolocation.getCurrentPosition(showMap);

  } // end getLoc



  function showMap(position){

    var lat = position.coords.latitude;

    var long = position.coords.longitude;

    var linkUrl = "http://maps.google.com?q=" + lat + "," + long;

    var mapLink = document.getElementById("mapLink");

    mapLink.href = linkUrl;

    var embedMap = document.getElementById("embedMap");

    embedMap.src = linkUrl + "&z=16&amp;output=embed";

  } // end showMap



  //]]>

  </script>

</head>



<body onload = "getLoc()">

  <h1>Geolocation </h1>



  <p>

    <a id = "mapLink"

       href = "http://maps.google.com">click for a map</a>

  </p>



<iframe id = "embedMap"

        width="800" 

        height="500" 

        frameborder="0" 

        scrolling="no" 

        marginheight="0" 

        marginwidth="0" 

        src= "">

</iframe><br />



</body>

</html>
