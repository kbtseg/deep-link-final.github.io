# deep-link-final.github.io


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>*TESTE REDIRECIONAMENTO LINK* VERSAO 1.4</title>
</head>
<body>
  

   <script>
      function getMobileOperatingSystem() {
         var userAgent = navigator.userAgent || navigator.vendor || window.opera;
         if( userAgent.match( /iPad/i ) || userAgent.match( /iPhone/i ) || userAgent.match( /iPod/i ) )
         {
            return 'iOS';
         }
         else if( userAgent.match( /Android/i ) )
         {
            return 'Android';
         }
         else
         {
            return 'unknown';
         }
      }
  
      function onLoad(){
         var instagram = "http://www.instagram.com/rioclaroloterias";
         var facebook = "http://www.facebook.com/rioclaroloterias";
         switch(getMobileOperatingSystem()){
             case 'Android':
                  instagram = "instagram://user?username=rioclaroloterias";
                  facebook = "intent://page/104067871350708?referrer=app_link#Intent;package=com.facebook.katana;scheme=fb;end";
                  break;
             case 'iOS':
                  instagram = "instagram://user?username=rioclaroloterias";
                  facebook = "fb://page/?id=104067871350708";
                  break;
             default:
                  break;
          }
         document.getElementById('instagram').setAttribute('href', instagram);
         document.getElementById('facebook').setAttribute('href', facebook);
        
      }
      window.onload = onLoad;
      </script>
    
    <a id="instagram" class="grey-text text-lighten-3" target="_blank">** INSTAGRAM **</a> <br><br>
    <a id="facebook" class="grey-text text-lighten-3" target="_blank">** FACEBOOK **</a>
    


</body>
</html>
