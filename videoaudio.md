## Controlando a reprodução de mídia

audio

    <audio src="audio.ogg" controls autoplay loop>
    <p>Seu navegador não suporta o elemento audio </p>
    </audio>
    
video

    <video controls>
      <source src="foo.ogg" type="video/ogg">
      <source src="foo.mp4" type="video/mp4">
      Seu navegador não suporta o elemento <code>video</code>.
    </video>

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

    var mediaElement = document.getElementById("myMediaElementID");
    mediaElement.pause();
    mediaElement.src = "";
    
Navegando pela mídia:

    var mediaElement = document.getElementById('mediaElementID');
    mediaElement.seekable.start();  // Retorna o tempo em que o arquivo começa (em segundos)
    mediaElement.seekable.end();    // Retorna o tempo em que o arquivo termina (em segundos)
    mediaElement.currentTime = 122; // Ir para 122 segundos
    mediaElement.played.end();      // Retorna o numero de segundos que o navegador reproduziu
    
Especificando o intervalo de reprodução

    #t=[tempoinicial],[tempofinal]
    
http://foo.com/video.ogg#t=10,20
Especifica que o intervalo entre 10 e 20 segundos deve ser reproduzido.
http://foo.com/video.ogg#t=,10.5
Especifica que o vídeo deve ser reproduzido do início até 10,5 segundos.
http://foo.com/video.ogg#t=,02:00:00
Especifica que o vídeo deve ser reproduzido do início até 2 horas.
http://foo.com/video.ogg#t=60,
Especifica que o vídeo deve começar aos 60 segundos e ser reproduzido até o final.

Utilizando Flash

    <video src="video.ogv" controls>
        <object data="flvplayer.swf" type="application/x-shockwave-flash">
          <param value="flvplayer.swf" name="movie"/>
        </object>
    </video>

Reproduzindo vídeos em Ogg usando uma applet Java

    <video src="my_ogg_video.ogg" controls width="320" height="240">
      <object type="application/x-java-applet"
              width="320" height="240">
         <param name="archive" value="cortado.jar">
         <param name="code" value="com.fluendo.player.Cortado.class">
         <param name="url" value="my_ogg_video.ogg">
         <p>You need to install Java to play this file.</p>
      </object>
    </video>
    


