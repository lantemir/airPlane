<template>
    <div class="space">
        <img class="ship" src="../assets/ship.png" alt="">
        <img class="gun" src="../assets/gun.png">
    </div>
</template>

<script>
import $ from 'jquery'

export default {
    name: "Space",
    mounted() {
        var posX = null;
        // var posY = null;
        var gunTop = null;

        window.addEventListener('keydown', function(event) {
            if(event.keyCode == 65) {
                posX -= 5;
                $('.ship').css('left', posX)
                console.log(posX)
            } else if(event.keyCode == 68) {
                posX += 5;
                $('.ship').css('left', posX)
                console.log(posX)
            }
        });

        window.addEventListener('click', function() {
            gunTop = 0;
            $('.gun').css('top', gunTop)
        });
    }
}
</script>