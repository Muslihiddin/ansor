<template>
        <div class="btn" :class="[ menuOpened ? 'active' : 'not-active' ]" @click="clickHandler">
            <span></span>
            <span></span>
            <span></span>
    </div>
</template>

<script>

export default {
    name: 'NavbarBurgerMenu',
    props: ['menuOpened'],
    emits:['toggle'],
    methods: {
      clickHandler(e) {
        this.$emit('toggle')
      }
    },
}
</script>

<style lang="scss" scoped>
.btn {
  width: 30px;
  height: auto;
  cursor: pointer;
}

span {
  display: block;
  width: 100%;
  border-radius: 3px;
  height: 3px;
  background-color: #fff;
  transition: all .3s;
  position: relative;
}

span + span {
  margin-top: 7px;
}

.active span:nth-child(1) {
  animation: ease .7s top forwards;

}

.not-active span:nth-child(1) {
  animation: ease .7s top-2 forwards;
  
}

.active span:nth-child(2) {
  animation: ease .7s scaled forwards;

}

.not-active span:nth-child(2) {
  animation: ease .7s scaled-2 forwards;
}

.active span:nth-child(3) {
  animation: ease .7s bottom forwards;

}

.not-active span:nth-child(3) {
  animation: ease .7s bottom-2 forwards;
}

@keyframes top {
  0% {
    top: 0;
    transform: rotate(0);
  }
  50% {
    top: 5px;
    transform: rotate(0);
  }
  100% {
    top: 5px;
    transform: rotate(45deg);
  }
}

@keyframes top-2 {
  0% {
    top: 5px;
    transform: rotate(45deg);
  }
  50% {
    top: 5px;
    transform: rotate(0deg);
  }
  100% {
    top: 0;
    transform: rotate(0deg);
  }
}

@keyframes bottom {
  0% {
    bottom: 0;
    transform: rotate(0);
  }
  50% {
    bottom: 15px;
    transform: rotate(0);
  }
  100% {
    bottom: 15px;
    transform: rotate(135deg);
  }
}

@keyframes bottom-2 {
  0% {
    bottom: 15px;
    transform: rotate(135deg);
  }
  50% {
    bottom: 15px;
    transform: rotate(0);
  }
  100% {
    bottom: 0;
    transform: rotate(0);
  }
}

@keyframes scaled {
  50% {
    transform: scale(0);
  }
  100% {
    transform: scale(0);
  }
}

@keyframes scaled-2 {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(0);
  }
  100% {
    transform: scale(1);
  }
}
</style>