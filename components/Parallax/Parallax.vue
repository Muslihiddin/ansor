<template>
<div class="parallax" id="home">
        <div id="stars"></div>
        <div id="stars2"></div>
        <div id="stars3"></div>
    <div id="horizon">
        <div class="glow"></div>
    </div>
    <div id="earth"></div>
    <div id="title">
    We want to work with you
    </div>
    <div id="subtitle">
    <span>
        We are a very experienced web
    </span>
    <span>
        &#38; mobile app
    </span>
    <span>
        development team
    </span>
    </div>
    <div id="talkButton">
        <a href="#contact_us">LET'S TALK</a>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
    </div>
    <div class="scroll">
        <p class="rotate">scroll</p>   
        <svg width="1" height="53" viewBox="0 0 1 53" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect width="1" height="53" fill="white" fill-opacity="0.5"/>
        <rect width="1" height="23" fill="white"/>
        </svg>
    </div>
</div>
</template>

<script>
export default {
    name: 'Parallax'
}
</script>

<style lang="scss" scoped>

@function multiple-box-shadow ($n) {
    $value: '#{random(2000)}px #{random(2000)}px #FFF';
    @for $i from 2 through $n {
        $value: '#{$value} , #{random(2000)}px #{random(2000)}px #FFF';
    }
    @return unquote($value)
}

        $shadows-small:     multiple-box-shadow(700);
        $shadows-medium:    multiple-box-shadow(200);
        $shadows-big:       multiple-box-shadow(100);

#stars {
    width: 1px;
    height: 1px;
    background: transparent;
    box-shadow: $shadows-small;
    animation: animStar 50s line infinite;

    &:after {
        content: " ";
        position: absolute;
        top: 2000px;
        width: 1px;
        height: 1px;
        background: transparent;
        box-shadow: $shadows-small;
    }
}

#stars2 {
    width: 2px;
    height: 2px;
    background: transparent;
    box-shadow: $shadows-medium;
    animation: animStar 100s linear infinite;

    &:after {
        content: "";
        position: absolute;
        top: 2000px;
        width: 2px;
        height: 2px;
        background: transparent;
        box-shadow: $shadows-medium;
    }
}

#stars3 {
    width: 3px;
    height: 3px;
    background: transparent;
    box-shadow: $shadows-big;
    animation: animStar 150s linear infinite;

    &:after {
        content: "";
        position: absolute;
        top: 2000px;
        width: 3px;
        height: 3px;
        background: transparent;
        box-shadow: $shadows-big;
    }
}

.parallax {
    position: absolute;
    top: -50px;
    bottom: 0;
    left: 0;
    right: 0;
    font-family: var(--comfortaa);
    color: #FFF;
    background: radial-gradient(ellipse at bottom, #000 0%, #163828 100%);
    z-index: 1;
    overflow: hidden;
}

#horizon {
    position: absolute;
    width: 160%;
    height: 70%;
    border-radius: 100% / 100%;

    background: #133224;
    -webkit-filter: blur(30px);

    left: 50%;
    bottom: -20%;
    margin-left: -80%;

    &:before {
    content: " ";
    position: absolute;
    width: 81.25%;
    height: 70%;
    border-radius: 100% / 100%;

    background: #133224;
    -webkit-filter: blur(30px);
    opacity: 0.6;
    
    margin-left: 9.375%;
    }

    &:after {
    content: " ";
    position: absolute;
    width: 32%;
    height: 20%;
    border-radius: 650px / 350px;

    background: #133224;
    -webkit-filter: blur(30px);
    opacity: 0.5;
    
    margin-left: 34%;
    }
    .glow {
        position: absolute;
        width: 100%;
        height: 100%;
        border-radius: 100% / 100%;

        background: #133224;
        -webkit-filter: blur(200px);
        opacity: 0.7;
        
        top: -10;
    }
}

#earth {
    position: absolute;
    width: 200%;
    height: 90%;
    background: black;
    border-radius: 100% / 100%;
    
    left: 50%;
    bottom: -50%;
    margin-left: -100%;
    
    &:before{
        content: " ";
        position: absolute;
        width: 100%;
        height: 90%;
        border-radius: 100% / 100%;
        
        box-shadow: inset 0px 0px 62px 25px rgba(19, 50, 36, 0.85);
    }
}

#title {
    position: absolute;
    font-weight: 700;
    top: 30%;
    left: 0;
    right: 0;
    margin-top: -80px;
    
    font-size: 96px;
    line-height: 153px;
    text-align: center;
    padding-left: 20px;
    
    background: -webkit-linear-gradient(white, rgb(219, 221, 224), #193B2B);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
        
    animation-duration: 6s;
    animation-iteration-count: infinite;
    animation-timing-function: ease;
    animation-name: animGravity;
}

#subtitle {
    position: absolute;
    font-family: var(--rubik);
    font-weight: 400;
    color: #C0DDCF;
    top: 45%;
    left: 0;
    right: 0;
    
    font-size: 32px;
    line-height: 51px;
    text-align: center;

    span {
        color: rgb(216, 216, 216);
        animation-duration: 6s;
        animation-iteration-count: infinite;
        animation-timing-function: ease;

        &:nth-child(1) {
            animation-name: animWeb;
        }
        &:nth-child(2) {
            animation-name: animMob;
        }
        &:nth-child(3) {
            animation-name: animTeam;
        }
    }
}

#talkButton {
    position: absolute;
    bottom: 50px;
    left: 0;
    right: 0;
    margin-inline: auto;
    display: flex;
    align-items: center;
    justify-content: center;

    a {
        font-size: 16px;
        line-height: 25px;
        font-weight: 700;
        color: #133224;
        border-radius: 50%;
        background-color: #FFF ;
        padding: 65px 35px;
        white-space: nowrap;
        z-index: 1000;
    }

    span {
        width: 30px;
        height: 10px;
        position: absolute;
        border: 1px solid #fff;
        border-radius: 50%;
        top: 50%;
        left: 50%;
        z-index: 1;
        transform: translate(-50%, -50%);
        

        &:nth-child(2) {
            animation: ring 15s infinite;
            animation-delay: 0s;
        }
        &:nth-child(3) {
            animation: ring 15s infinite;
            animation-delay: 4s;
        }
        &:nth-child(4) {
            animation: ring 15s infinite;
            animation-delay: 8s;
        }
        &:nth-child(5) {
            animation: ring 15s infinite;
            animation-delay: 12s;
        }
    }
}

.scroll {
    position: absolute;
    right: clamp(20px, 8vw, 240px);
    bottom: 65px;

   font-family: var(--montserrat);
   font-weight: 400;
   font-size: 16px;
   line-height: 24px;
   color: #fff;
   animation: animScroll 2s linear;
   animation-delay: 3s;

   .rotate {
        transform: rotate(-90deg);
   }
   svg {
       position: relative;
       top: 15px;
       left: 23px;
   }
}

@keyframes animStar {
    from {
        transform: translateY(0px);
    }
    to {
        transform: translateY(-2000px);
    }
}

@keyframes animGravity {
    0% {
        transform: translateY(-26px);
        opacity: 0;
    }
    30%, 80% {
        letter-spacing: 6px;
        padding-left: 5px;
        transform: translateY( 0px );
        opacity: 1;
    }
    92%, 100% {
        letter-spacing: 6px;
        padding-left: 5px;
        transform: translateY( -4px );
        opacity: 0;
    }
}

@keyframes animWeb {
    0%, 15%{
        transform: translateY(-26px);
        opacity: 0;
    }
    35%, 80%{
        transform: translateY( 0px );
        opacity: 1;
    }
    92%, 100%{
    transform: translateY( -4px );
    opacity: 0;
    }
}
@keyframes animMob {
    0% , 25%{
        transform: translateY(-26px);
        opacity: 0;
    }
    45% , 80%{
        transform: translateY( 0px );
        opacity: 1;
    }
    92% , 100%{
    transform: translateY( -4px );
    opacity: 0;
    }
}

@keyframes animTeam {
    0% , 35%{
        transform: translateY(-26px);
        opacity: 0;
    }
    55% , 80%{
        transform: translateY( 0px );
        opacity: 1;
    }
    92% , 100%{
    transform: translateY( -4px );
    opacity: 0;
    }
}

@keyframes ring {
  0% {
    width: 1px;
    height: 1px;
    opacity: 1;
  }
  50% {
    opacity: 0.3;
  }
  70% {
   opacity: 0;
  }
  100% {
    width: 320px;
    height: 310px;  
    opacity: 0;
  }
}

@keyframes animScroll {
    0% {
        opacity: 0;
        transform: translateY(-45px);
    }
    100% {
        opacity: 1;
        transform: translateY(0);
    }
}


@media screen and(max-width: 1290px) {
    #title {
        font-size: 80px;
        line-height: 123px;
    }
}

@media screen and(max-width: 1180px) {
    #title {
        font-size: 70px;
        line-height: 110px;

        top: 40%;
    }
}

@media screen and(max-width: 1050px) {
    #title {
        font-size: 60px;
        line-height: 96px;

        top: 40%;
    }
}

@media screen and (max-width: 920px) {
    #title {
        top: 30%;
        line-height: 66px;
        width: 780px;
        margin-inline: auto;
    }
}

@media screen and(max-width: 770px) {
    #title {
        width: 660px;
    }
    #talkButton {
        a {
            padding: 45px 15px;
        }
    }

    @keyframes ring {
        0% {
            width: 15px;
            height: 15px;
            opacity: 1;
        }
        50% {
            opacity: 0.3;
        }
        70% {
        opacity: 0;
        }
        100% {
            width: 220px;
            height: 210px;  
            opacity: 0;
        }

    }
}

@media screen and(max-width: 640px) {
    #title {
        width: 520px;
    }

    #subtitle {
        left: 7px;
        right: 7px;
    }
}

@media screen and(max-width: 530px) {
    #title {
        margin-inline: 0;
        text-align: left;
        top: 35%;
        font-size: 50px;
        line-height: 63px;
        width: 435px;
        left: 5px;
        right: 5px;
    }

    #subtitle {
        text-align: left;
        font-size: 28px;
        line-height: 35px;
        left: 7px;
        right: 7px;
    }

    .scroll {
        right: 15px;
    }
}

@media screen and(max-width: 430px) {
    #title {
        top: 27%;
        width: 350px;
    }
}

@media screen and(max-width: 350px) {
    #title {
        top: 27%;
        width: 300px;
        line-height: 50px;
    }
}
</style>