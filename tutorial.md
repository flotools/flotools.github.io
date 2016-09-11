---
layout: page
title: Audio Tutorial
permalink: /tutorial/
---

<script>

function playing(player) {
label = player.id;
time = player.currentTime;
         if (time == 0) {
            ga('send', 'event', 'Media', 'Play', label);
         } else {
            ga('send', 'event', 'Media', 'Play', label+' @ ' + time);
         }
        }

function pausing(player) {
label = player.id;
time = player.currentTime;
            if (player.getDuration() - time != 0) {
            ga('send', 'event', 'Media', 'Pause', label+' @ ' + time);
}
        }

function ending(player) {
label = player.id;
            ga('send', 'event', 'Media', 'Finished', label);
    }

</script>

<audio controls id="audioFloTools1.0" onPlaying="playing(this)" onPause="pauseing(this)" onEnded="ending(this)">
<source src="/Intro to Flo Tools.m4a" type="audio/mp4">
Your browser does not support html5 audio.
</audio>

Music by [Frank Senior](http://www.franksenior.com/)
