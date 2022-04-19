<template>
    <div class="wrapper-numbers flex flex-wrap items-center justify-center sm:justify-between">
            <div class="card flex flex-wrap flex-col text-center ">
                <span class="num text-white block1">+</span>
                <span class="text">Years of custom software development</span>
            </div>
            <div class="card flex flex-wrap flex-col text-center ">
                <span class="num text-white block2">+</span>
                <span class="text">Years of app development experience</span>
            </div>
            <div class="card flex flex-wrap flex-col text-center ">
                <span class="num text-white block3">%</span>
                <span class="text">of our team is hard core developers</span>
            </div>
            <div class="card flex flex-wrap flex-col text-center ">
                <span class="num text-white block4"></span>
                <span class="text">of our team is hard core developers</span>
            </div>
        </div>
</template>

<script>
export default {
    name: 'ProductsNumbers',
    data() {
      return {
        scrollPosition: false,
      }
    },
    mounted() {
      this.animateOnScroll1()
      this.animateOnScroll2()
      this.animateOnScroll3()
      this.animateOnScroll4()
    },
    methods: {
      animateOnScroll1() {
        this.$gsap.to(window, {})

        this.$gsap.to('.wrapper-numbers', {
          scrollTrigger: {
            trigger: '.block1',
            end: 'bottom',
            toggleClass: 'num1'
          }
        })
      },
      animateOnScroll2() {
          this.$gsap.to(window, {})

          this.$gsap.to('.wrapper-numbers', {
            scrollTrigger: {
              trigger: '.block2',
              end: 'bottom',
              toggleClass: 'num1'
            }
          })
        },
        animateOnScroll3() {
          this.$gsap.to(window, {})

          this.$gsap.to('.wrapper-numbers', {
            scrollTrigger: {
              trigger: '.block3',
              end: 'bottom',
              toggleClass: 'num3'
            }
          })
        },
        animateOnScroll4() {
          this.$gsap.to(window, {})

          this.$gsap.to('.wrapper-numbers', {
            scrollTrigger: {
              trigger: '.block4',
              end: 'bottom',
              toggleClass: 'num4'
            }
          })
        }
  }, 
}
</script>

<style lang="scss" scoped>
.box {
  width: 100px;
  height: 100px;
  background-color: #00c58e;
}

    .card {
        background: linear-gradient(338.57deg, #28A472 1.17%, #65C785 91.77%);
        font-family: var(--space);
        max-width: 302px;
        border-radius: 16px;
        margin-top: 72px;
        padding: 30px 46px;
    }

    .num {
        font-size: 80px;
        font-weight: 700;
        line-height: 102px;
    }

    .text {
        color: var(--Green_04);
    }

    // Count animation
    .num1::before {
        content: counter(count);
        animation: counter 1.7s linear alternate-reverse;
        counter-reset: count 12;
    }

    @keyframes counter {
  0% {
    counter-increment: count -1;
  }
  10% {
    counter-increment: count -2;
  }
  20% {
    counter-increment: count -3;
  }
  30% {
    counter-increment: count -4;
  }
  35% {
    counter-increment: count -5;
  }
  40% {
    counter-increment: count -6;
  }
  50% {
    counter-increment: count -7;
  }
  60% {
    counter-increment: count -8;
  }
  70% {
    counter-increment: count -9;
  }
  75% {
    counter-increment: count -10;
  }
  80%{
    counter-increment: count -11;
  }
  90% {
    counter-increment: count -12;
  }
  100% {
    counter-increment: count 0;
  }
}

  .num3::before {
        content: counter(count);
        animation: counter 1.7s linear alternate-reverse;
        counter-reset: count 97;
    }

    @keyframes counter3 {
  0% {
    counter-increment: count -10;
  }
  10% {
    counter-increment: count -21;
  }
  20% {
    counter-increment: count -32;
  }
  30% {
    counter-increment: count -43;
  }
  35% {
    counter-increment: count -53;
  }
  40% {
    counter-increment: count -63;
  }
  50% {
    counter-increment: count -75;
  }
  60% {
    counter-increment: count -84;
  }
  70% {
    counter-increment: count -98;
  }
  75% {
    counter-increment: count -10;
  }
  80%{
    counter-increment: count -11;
  }
  90% {
    counter-increment: count -12;
  }
  100% {
    counter-increment: count -97;
  }
}

  .num4::before {
        content: counter(count);
        animation: counter 1.7s linear alternate-reverse;
        counter-reset: count 20;
    }

    @keyframes counter4 {
  0% {
    counter-increment: count -2;
  }
  10% {
    counter-increment: count -4;
  }
  20% {
    counter-increment: count -6;
  }
  30% {
    counter-increment: count -8;
  }
  35% {
    counter-increment: count -10;
  }
  40% {
    counter-increment: count -12;
  }
  50% {
    counter-increment: count -14;
  }
  60% {
    counter-increment: count -16;
  }
  70% {
    counter-increment: count -17;
  }
  75% {
    counter-increment: count -18;
  }
  80%{
    counter-increment: count -19;
  }
  90% {
    counter-increment: count -20;
  }
  100% {
    counter-increment: count -20;
  }
}

    
</style>