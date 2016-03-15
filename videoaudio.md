## Controlando a reprodução de mídia

para começar (ou repetir) a reprodução, você pode fazer isto:

    var v = document.getElementsByTagName("video")[0];
    v.play();

Controlando um reprodutor de áudio para reproduzir, pausar, aumentar e diminuir o volume usando JavaScript é simples.

    <audio id="demo" src="audio.mp3"></audio>
    <div>
      <button onclick="document.getElementById('demo').play()">Reproduzir o áudio</button>
      <button onclick="document.getElementById('demo').pause()">Pausar o áudio</button>
      <button onclick="document.getElementById('demo').volume+=0.1">Aumentar o volume</button>
      <button onclick="document.getElementById('demo').volume-=0.1">Diminuir o volume</button>
    </div>

Esta é um modo para parar o download imediatamente:



