<template>
  <div class="text-center">
              <!-- <h3 class="display-1 font-weight-black">바른연애생활</h3> -->
    <div class='d-flex justify-center'>
      <div class='slot' ref="slot">
        <div class='slot__window display-1 font-weight-black'>
          <div class='slot__wrap'>
            <div class='slot__item' v-for='item in items'>{{ item }}</div>
            <div class='slot__item slot__item--copy' >{{ items[0] }}</div>
          </div>
        </div>
      </div>
    </div>

    <h4 class="subtitle-1 font-weight-bold white--text mb-4">친구와 함께 2:2 바른 만남</h4>

    <v-container>
      <v-row class="d-flex align-center">
        <v-col cols="12">
          <v-card width="320" color="transparent" elevation="0" class="mx-auto" style="position: relative;">
            <v-btn icon @click="start" :loading="!!opt" class="mx-auto">
              <svg width="64" height="64" viewBox="0 0 480 480" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M374.34 480H105.62C47.29 480 0 432.71 0 374.38V105.62C0 47.29 47.29 0 105.62 0H374.34C432.67 0 479.96 47.29 479.96 105.62V374.39C479.95 432.71 432.67 480 374.34 480Z" fill="#01C5FC"/>
                <path d="M338.97 213.36C333.8 216.89 326.98 216.89 321.81 213.36C236.02 154.7 275.4 112.14 276.63 110.85C276.65 110.83 276.66 110.82 276.66 110.82C277.03 110.37 277.41 109.94 277.81 109.51C283.58 103.3 291.81 99.43 300.95 99.43C308.46 99.43 315.36 102.05 320.78 106.42C326.49 111.03 334.52 111.03 340.22 106.42C345.64 102.04 352.54 99.43 360.05 99.43C369.19 99.43 377.42 103.31 383.19 109.51C383.58 109.93 383.97 110.37 384.34 110.82C384.34 110.82 384.35 110.83 384.37 110.85C385.6 112.15 424.78 154.7 338.97 213.36Z" fill="#FDCF00"/>
                <path d="M158.65 213.36C153.48 216.89 146.66 216.89 141.49 213.36C55.7 154.7 95.08 112.15 96.31 110.85C96.33 110.83 96.34 110.82 96.34 110.82C96.71 110.37 97.09 109.94 97.49 109.51C103.26 103.3 111.49 99.43 120.63 99.43C128.14 99.43 135.04 102.05 140.46 106.42C146.17 111.03 154.2 111.03 159.9 106.42C165.32 102.04 172.22 99.43 179.73 99.43C188.87 99.43 197.1 103.31 202.87 109.51C203.26 109.93 203.65 110.37 204.02 110.82C204.02 110.82 204.03 110.83 204.05 110.85C205.27 112.15 244.45 154.7 158.65 213.36Z" fill="#FDCF00"/>
                <path d="M331.25 240.27C318.27 240.27 307.76 250.79 307.76 263.77V280.15H267.24C254.32 280.15 243.85 290.62 243.85 303.54C243.85 316.46 254.32 326.93 267.24 326.93H307.76V345.06H267.24C254.32 345.06 243.85 355.53 243.85 368.45C243.85 381.37 254.32 391.84 267.24 391.84H307.76V391.87H331.08C344.03 391.87 354.54 381.37 354.54 368.41V263.55C354.53 250.69 344.11 240.27 331.25 240.27Z" fill="white"/>
                <path d="M213.12 326.92C226.04 326.92 236.51 316.45 236.51 303.53C236.51 290.61 226.04 280.14 213.12 280.14H172.6V263.76C172.6 250.78 162.08 240.26 149.11 240.26C136.25 240.26 125.83 250.68 125.83 263.54V368.4C125.83 381.36 136.33 391.86 149.29 391.86H172.61V391.83H213.13C226.05 391.83 236.52 381.36 236.52 368.44C236.52 355.52 226.05 345.05 213.13 345.05H172.61V326.92H213.12Z" fill="white"/>
              </svg>
            </v-btn>
            <img src="/images/click.png" style="position: absolute; right: 0" />
          </v-card>
        </v-col>
        <v-col cols="12" md="6">
          <v-card elevation="0" color="transparent" tile>
            <a href="https://www.apple.com/kr/app-store/">
              <v-img :class="leftAlign" src="/images/apple.png" width="190" height="56" />
            </a>
          </v-card>
        </v-col>
        <v-col cols="12" md="6">
          <v-card elevation="0" color="transparent" tile>
            <a href="https://play.google.com/store">
              <v-img :class="rightAlign" src="/images/google.png" width="220" height="64" />
            </a>
          </v-card>
        </v-col>
      </v-row>


    </v-container>

  </div>
</template>

<script>
const next = window.requestAnimationFrame ||
  window.webkitRequestAnimationFrame ||
  window.mozRequestAnimationFrame ||
  window.msRequestAnimationFrame ||
  window.oRequestAnimationFrame ||
  function(cb) { window.setTimeout(cb, 1000/60) }

export default {
  layout: 'empty',
  data() {
    return {
      items: [
        '바른연애생활',
        '바른문화생활',
        '바른운동생활',
        '바른음주생활',
        '바른취미생활',
        '바른게임생활',
        '바른요리생활',
      ],
      opt: null,
      startedAt: null,
    }
  },
  computed: {
    rightAlign() {
      return this.$vuetify.breakpoint.mdAndUp ? "mr-auto" : "mx-auto"
    },
    leftAlign() {
      return this.$vuetify.breakpoint.mdAndUp ? "ml-auto" : "mx-auto"
    },
  },
  methods: {
    start: function() {
      if (this.opt) {
        return
      }
      const slot = this.$refs.slot
      const choice = Math.floor( Math.random() * this.items.length )

      this.opt = {
        el: slot.querySelector('.slot__wrap'),
        finalPos: choice * 64,
        startOffset: 2000 + Math.random() * 500,
        height: this.items.length * 64,
        duration: 3000, // milliseconds
        isFinished: false,
      }
      
      next(this.animate)
    },
    
    animate: function(timestamp) {
			if (this.startedAt == null) {
        this.startedAt = timestamp
      }
      const timeDiff = timestamp - this.startedAt
      
      if (this.opt.isFinished) {
        return
      }

      const timeRemaining = Math.max(this.opt.duration - timeDiff, 0)
      const power = 3
      const offset = ( Math.pow(timeRemaining, power) / Math.pow(this.opt.duration, power) ) * this.opt.startOffset
        
      // negative, such that slots move from top to bottom
      const pos = -1 * Math.floor((offset + this.opt.finalPos) % this.opt.height)
      this.opt.el.style.transform = "translateY(" + pos + "px)"
        
      if ( timeDiff > this.opt.duration ) {
        console.log('finished', this.opt, pos, this.opt.finalPost)
        this.opt.isFinished = true
        this.opt = null
        this.startedAt = null
      } else {
        next( this.animate )
      }
    },
  }

}
</script>

<style>

.slot__window {
  background-color: green;
  width: 240px;
  height: 64px;
  overflow: hidden;
}

.slot__wrap {

}

.slot__item {
  width: 240px;
  height: 64px;

  text-align: center;
  background-color: #53c6ff;
  color: black;
  
  line-height: 64px;
}

.slot__item--copy {
}
</style>
