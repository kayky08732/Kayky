<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Texto Brilhante</title>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.6.0/p5.js"></script>
  <style>
    @font-face {
      font-family: 'CustomFont';
      src: url('https://example.com/path-to-your-font.ttf') format('truetype');
    }
  </style>
</head>
<body>
  <script>
    let font;

    function preload() {
      font = loadFont('https://example.com/path-to-your-font.ttf');
    }

    function setup() {
      createCanvas(windowWidth, windowHeight);
      textFont(font || 'Georgia'); // Substitui 'Georgia' pela fonte carregada
      textAlign(CENTER, CENTER);
    }

    function draw() {
      background(0); // Fundo preto para efeito de texto brilhante

      fill(255, 50, 100); // Cor vibrante de texto
      textSize(64);
      text('Love You', width / 2, height / 2);

      // Adicionar um efeito de animação
      stroke(255, random(100, 255), random(100, 255));
      strokeWeight(2);
      noFill();
      ellipse(width / 2, height / 2, frameCount % 200 + 50);
    }
  </script>
</body>
</html>
