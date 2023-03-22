<script>
export default {
    name: 'WaveComponent'
}
</script>

<template>
    <div class="ocean">
        <div class="wave wave1"></div>
        <div class="wave wave2"></div>
        <div class="wave wave3"></div>
    </div>
</template>

<style>
.ocean {
    height: 200px;
    width: 100%;
    overflow: hidden;
    position: absolute;
    bottom: 0;
    left: 0;
}

.ocean.v01 .wave {
    background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/85486/wave.svg) repeat-x;
}

.ocean.v01 {
    transform: rotate(180deg);
    position: absolute;
    top: 0;
    left: 0;
}

.wave {
    background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/85486/wave.svg) repeat-x;
    position: absolute;
    width: 6400px;
    height: 100%;
}

.wave1 {
    bottom: -25px;
    animation: wave 12s cubic-bezier(0.36, 0.45, 0.63, 0.53) -.125s infinite, swell 7s ease -1.25s infinite;
    opacity: 1;
}

.wave2 {
    bottom: -30px;
    animation: wave 10s cubic-bezier(0.36, 0.45, 0.63, 0.53) -.125s infinite, swell 7s ease -1.25s infinite;
    opacity: 1;
}

.wave3 {
    bottom: -50px;
    animation: wave 8s cubic-bezier(0.36, 0.45, 0.63, 0.53) -.125s infinite, swell 7s ease -1.25s infinite;
    opacity: 1;
}

.wave:nth-of-type(2) {
    /* bottom: -25px;
    animation: wave 7s cubic-bezier(0.36, 0.45, 0.63, 0.53) -.125s infinite, swell 7s ease -1.25s infinite;
    opacity: 1; */
}

@keyframes wave {
    0% {
        margin-left: 0;
    }

    100% {
        margin-left: -1600px;
    }
}

@keyframes swell {

    0%,
    100% {
        transform: translateY(-25px);
    }

    50% {
        transform: translateY(5px);
    }
}
</style>