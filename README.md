# A Better Audio Player for HTML5 - BetterAudio.js

Features:
- Use CSS styles to change audio element (player)
- Manage playlists
- Javascript API

## Intro

Original Codepen: http://codepen.io/k-ivan/pen/pJMLmJ by @k-ivan  
Original fork: https://github.com/likev/html5-audio-player by @likev  

![html5-audio-player-screenshot](html5-audio-player.png)

## Quick Start

1. insert Google Material Icons and BetterAudio.css before `</head>`
2. insert BetterAudio.js before `</body>`
3. use BetterAudio.init function

code example:
```html
<!DOCTYPE html>
<html >
  <head>
    <meta charset="UTF-8">
    <title>Audio player HTML5</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
    <link rel="stylesheet" href="css/BetterAudio.css">
    <style>

    #player{
        position: relative;
        max-width: 700px;
        height: 500px;
        border: solid 1px gray;
    }
    </style>
  </head>

  <body>
      <!-- Audio player container-->
     <div id='player'></div>

    <!-- Audio player js begin-->
    <script src="js/BetterAudio.js"></script>

    <script>
        // test image for web notifications
        var iconImage = null;

        BetterAudio.init({
            container:'#player',//a string containing one CSS selector
            volume   : 0.7,
            autoPlay : true,
            notification: false,
            playList: [
                {icon: iconImage, title: "Jump Steady Blues", file: "http://www.openmusicarchive.org/audio/Jump_Steady_Blues.mp3"},
                {icon: iconImage, title: "Eddies Twister", file: "http://www.openmusicarchive.org/audio/Eddies_Twister.mp3"}
          ]
        });
    </script>
    <!-- Audio player js end-->

  </body>
</html>
```

Have fun! :-)
