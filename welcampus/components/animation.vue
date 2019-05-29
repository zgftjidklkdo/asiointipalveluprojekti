<template>
  <v-app>
    <v-content>
      <v-container>
        <body>
          <div id="dude" />
          <div id="instructions" />
        </body>
      </v-container>
    </v-content>
  </v-app>
</template>

<style>
    #instructions {
        position: absolute;
        top: 0px;
        left: 0px;
        width: 80px;
        height: 65px;
        background: url('../assets/wasd.png') no-repeat;
    }

    #dude {
        position: absolute;
        top: 0px;
        left: 0px;
        width: 45px;
        height: 45px;
        background: url('../assets/animation_finished.png') no-repeat;
    }

    #dude.front-right { background-position: 0px 0px; }
    #dude.front-stand { background-position: -45px 0px; }
    #dude.front-left { background-position: -90px 0px; }
    #dude.left-right { background-position: 0px -48px; }
    #dude.left-stand { background-position: -45px -48px; }
    #dude.left-left { background-position: -90px -48px; }
    #dude.right-right { background-position: -0px -96px; }
    #dude.right-stand { background-position: -45px -96px; }
    #dude.right-left { background-position: -90px -96px; }
    #dude.back-right { background-position: 0px -144px; }
    #dude.back-stand { background-position: -45px -144px; }
    #dude.back-left { background-position: -90px -144px; }
</style>

<script>
/* eslint eqeqeq: "off" */
import $ from 'jquery'

export default {
  name: 'Animation',
  mounted: () => {
    let currentKey
    let TimerWalk
    let charStep = 2
    const charSpeed = 400

    $(document).ready(function () {
      $('#dude').addClass('front-stand')
    })

    $(document).keydown(function (e) {
      if (!currentKey) {
        currentKey = e.keyCode

        switch (e.keyCode) {
          case 87:
            charWalk('up')
            break
          case 68:
            charWalk('right')
            break
          case 83:
            charWalk('down')
            break
          case 65:
            charWalk('left')
            break
        }
      }
    })

    $(document).keyup(function (e) {
      if (e.keyCode == currentKey) {
        currentKey = false
        clearInterval(TimerWalk)
        $('#dude').stop(true, true)
      }
    })

    function charWalk(dir) {
      if (dir == 'up') dir = 'back'
      if (dir == 'down') dir = 'front'

      processWalk(dir)

      TimerWalk = setInterval(function () {
        processWalk(dir)
      }, charSpeed)
    }

    function processWalk(dir) {
      charStep++

      if (charStep == 5) charStep = 1

      $('#dude').removeAttr('class')

      switch (charStep) {
        case 1:
          $('#dude').addClass(dir + '-stand')
          break
        case 2:
          $('#dude').addClass(dir + '-right')
          break
        case 3:
          $('#dude').addClass(dir + '-stand')
          break
        case 4:
          $('#dude').addClass(dir + '-left')
          break
      }

      switch (dir) {
        case 'front':
          $('#dude').animate({
            top: '+=32'
          }, charSpeed)
          break
        case 'back':
          if ($('#dude').position().top > 0) {
            $('#dude').animate({
              top: '-=32'
            }, charSpeed)
          }
          break
        case 'left':
          if ($('#dude').position().left > 0) {
            $('#dude').animate({
              left: '-=32'
            }, charSpeed)
          }
          break
        case 'right':
          $('#dude').animate({
            left: '+=32'
          }, charSpeed)
          break
      }
    }
  }
}
</script>
