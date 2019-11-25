# Видео

HTML

    <canvas id="Canvas1" width="700" height="300"></canvas>
    <img id="img1" src="img/bay.jpg" width="715" height="315" style="display:none;" />
    <video id="vid1" src="img/video.mp4" loop style="display:none"></video>

JavaScript

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                var srcImg = document.getElementById('img1')
                var srcVid = document.getElementById('vid1')
                srcVid.play()
                setInterval(function() {
                    var theCanvas = document.getElementById('Canvas1')
                    var ctx = theCanvas.getContext('2d')
                    var srcVid = document.getElementById('vid1')
                    ctx.drawImage(srcVid, 0, 0)
                }, 16)
            }
        }
    }