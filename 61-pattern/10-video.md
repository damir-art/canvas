# Паттерн "Видео"
Как паттерн выступает определённый кадр.

Устанавливаем как паттерн кадр на третьей секунде.

HTML

    <video id="vidEl" src="img/video.mp4" autoplay controls style="display:none"></video>

JavaScript

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                setTimeout(function(){
                    var vid       = document.getElementById('vidEl')
                    var theCanvas = document.getElementById('Canvas1')
                    var ctx       = theCanvas.getContext('2d')
                    var vidPat    = ctx.createPattern(vid, 'repeat')
                    ctx.fillStyle = vidPat
                    ctx.fillRect(0, 0, ctx.canvas.width, ctx.canvas.height)
                }, 3000)
            }
        }
    }