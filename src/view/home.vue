<template>
    <div style="position: relative">
        <var-image
            style="width: 25%; position: absolute; top: 70%; left: 37.5%"
            :src="p2_b"
            @click="center = true"
        />
        <var-popup style="width: 90%; height: 80%" v-model:show="center">
            <var-image width="100%" :src="mes_1" />
        </var-popup>
        <var-image width="80%" :src="bg2_t" />
        <var-image style="width: 50%; margin: 0 auto" :src="bg2_w" />
        <var-image :src="bg2_b" />
    </div>
    <div style="position: relative">
        <var-image
            v-if="bgThree == bg3_2"
            style="width: 25%; position: absolute; top: 20%; left: 37.5%"
            :src="bg3_w1"
        />
        <var-image
            v-if="bgThree == bg3_2"
            style="width: 25%; position: absolute; top: 30%; left: 37.5%"
            :src="bg3_w2"
        />
        <var-image
            @click="bgThreeClick"
            style="width: 25%; position: absolute; top: 70%; left: 37.5%"
            :src="p3_b"
        />
        <var-image :src="bgThree" />
    </div>
    <div style="position: relative">
        <var-image
            v-if="bgGifShow"
            style="width: 70%; position: absolute; top: 30%; left: 15%"
            :src="bg4_gif"
        />
        <var-image
            @click="bgFourClick"
            style="width: 25%; position: absolute; top: 70%; left: 37.5%"
            :src="p4_b"
        />
        <var-image :src="bg4" />
    </div>
    <div style="position: relative">
        <div class="stars-con" id="stars">
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
            <img :src="stars" />
        </div>
        <var-image style="width: 25%; position: absolute; top: 50%; left: 37.5%" :src="girl_6" />
        <var-image :src="pg5" />
    </div>
</template>

<script setup>
import { ref } from 'vue'

import bg2_t from '../assets/img/bg-2-top.png'
import bg2_w from '../assets/img/bg-2-wz.png'
import bg2_b from '../assets/img/bg-2-bottom.png'

import bg3_2 from '../assets/img/bg-3-2.png'
import bg3 from '../assets/img/bg-3.png'
import bg3_w1 from '../assets/img/pg3-wz1.png'
import bg3_w2 from '../assets/img/pg3-wz2.png'

import bg4 from '../assets/img/pg-4.png'
import bg4_gif from '../assets/img/bg4GIF.gif'

import pg5 from '../assets/img/pg5-bg.png'
import stars from '../assets/img/stars.png'
import girl_6 from '../assets/img/girl-6.png'

import p2_b from '../assets/img/p2-but.png'
import p3_b from '../assets/img/p3-but.png'
import p4_b from '../assets/img/p4-but.png'

import mes_1 from '../assets/img/mes-1.png'

const bgThree = ref(bg3)
const bgThreeClick = () => {
    if (bgThree.value == bg3) {
        bgThree.value = bg3_2
    } else {
        bgThree.value = bg3
    }
}

const bgGifShow = ref(false)
const bgFourClick = () => {
    if (bgGifShow.value == false) {
        bgGifShow.value = true
    } else {
        bgGifShow.value = false
    }
}

const center = ref(false)
</script>

<style scoped>
.stars-con {
    width: 100%;
    height: 100vw;
    position: absolute;
    top: -2vh;
}
.stars-con img:nth-of-type(1) {
    position: absolute;
    width: 6vw;
    top: 7vw;
    right: 30vw;
    -webkit-animation: startplay 2s infinite;
    -o-animation: startplay 2s infinite;
    animation: startplay 2s infinite;
}
.stars-con img:nth-of-type(2) {
    position: absolute;
    width: 6vw;
    top: 8vw;
    right: 40vw;
    -webkit-animation: startplay 1.1s infinite 1s;
    -o-animation: startplay 1.1s infinite 1s;
    animation: startplay 1.1s infinite 1s;
}
.stars-con img:nth-of-type(3) {
    position: absolute;
    width: 6vw;
    top: 9vw;
    right: 50vw;
    -webkit-animation: startplay 2s infinite 0.2s;
    -o-animation: startplay 2s infinite 0.2s;
    animation: startplay 2s infinite 0.2s;
}
.stars-con img:nth-of-type(4) {
    position: absolute;
    width: 6vw;
    top: 10vw;
    right: 60vw;
    -webkit-animation: startplay 1.6s infinite 0.3s;
    -o-animation: startplay 1.6s infinite 0.3s;
    animation: startplay 1.6s infinite 0.3s;
}
.stars-con img:nth-of-type(5) {
    position: absolute;
    width: 6vw;
    top: 6vw;
    left: 30vw;
    -webkit-animation: startplay 2.4s infinite 0.1s;
    -o-animation: startplay 2.4s infinite 0.1s;
    animation: startplay 2.4s infinite 0.1s;
}
.stars-con img:nth-of-type(6) {
    position: absolute;
    width: 6vw;
    top: 15vw;
    left: 28vw;
    -webkit-animation: startplay 2.2s infinite;
    -o-animation: startplay 2.2s infinite;
    animation: startplay 2.2s infinite;
}
.stars-con img:nth-of-type(7) {
    position: absolute;
    width: 6vw;
    top: 25vw;
    left: 26vw;
    -webkit-animation: startplay 2s infinite;
    -o-animation: startplay 2s infinite;
    animation: startplay 2s infinite;
}
.stars-con img:nth-of-type(8) {
    position: absolute;
    width: 6vw;
    top: 35vw;
    left: 24vw;
    -webkit-animation: startplay 1.4s infinite 0.5s;
    -o-animation: startplay 1.4s infinite 0.5s;
    animation: startplay 1.4s infinite 0.5s;
}
.stars-con img:nth-of-type(9) {
    position: absolute;
    width: 6vw;
    top: 35vw;
    left: 35vw;
    -webkit-animation: startplay 3s infinite;
    -o-animation: startplay 3s infinite;
    animation: startplay 3s infinite;
}
.stars-con img:nth-of-type(10) {
    position: absolute;
    width: 6vw;
    top: 35vw;
    left: 45vw;
    -webkit-animation: startplay 1.8s infinite;
    -o-animation: startplay 1.8s infinite;
    animation: startplay 1.8s infinite;
}
.stars-con img:nth-of-type(11) {
    position: absolute;
    width: 6vw;
    top: 35vw;
    left: 55vw;
    -webkit-animation: startplay 1.6s infinite;
    -o-animation: startplay 1.6s infinite;
    animation: startplay 1.6s infinite;
}
.stars-con img:nth-of-type(12) {
    position: absolute;
    width: 6vw;
    top: 35vw;
    left: 65vw;
    -webkit-animation: startplay 1s infinite;
    -o-animation: startplay 1s infinite;
    animation: startplay 1s infinite;
}
.stars-con img:nth-of-type(13) {
    position: absolute;
    width: 6vw;
    top: 35vw;
    left: 75vw;
    -webkit-animation: startplay 2.5s infinite 1s;
    -o-animation: startplay 2.5s infinite 1s;
    animation: startplay 2.5s infinite 1s;
}
.stars-con img:nth-of-type(14) {
    position: absolute;
    width: 6vw;
    top: 20vw;
    left: 50vw;
    -webkit-animation: startplay 1.1s infinite 1s;
    -o-animation: startplay 1.1s infinite 1s;
    animation: startplay 1.1s infinite 1s;
}
.stars-con img:nth-of-type(15) {
    position: absolute;
    width: 6vw;
    top: 30vw;
    left: 50vw;
    -webkit-animation: startplay 1.7s infinite 0.2s;
    -o-animation: startplay 1.7s infinite 0.2s;
    animation: startplay 1.7s infinite 0.2s;
}
.stars-con img:nth-of-type(16) {
    position: absolute;
    width: 6vw;
    top: 40vw;
    left: 50vw;
    -webkit-animation: startplay 2.3s infinite;
    -o-animation: startplay 2.3s infinite;
    animation: startplay 2.3s infinite;
}
.stars-con img:nth-of-type(17) {
    position: absolute;
    width: 6vw;
    top: 50vw;
    left: 50vw;
    -webkit-animation: startplay 2.2s infinite;
    -o-animation: startplay 2.2s infinite;
    animation: startplay 2.2s infinite;
}
.stars-con img:nth-of-type(18) {
    position: absolute;
    width: 6vw;
    top: 60vw;
    left: 50vw;
    -webkit-animation: startplay 0.6s infinite;
    -o-animation: startplay 0.6s infinite;
    animation: startplay 0.6s infinite;
}
.stars-con img:nth-of-type(19) {
    position: absolute;
    width: 6vw;
    top: 70vw;
    left: 50vw;
    -webkit-animation: startplay 1.8s infinite 0.2s;
    -o-animation: startplay 1.8s infinite 0.2s;
    animation: startplay 1.8s infinite 0.2s;
}
.stars-con img:nth-of-type(20) {
    position: absolute;
    width: 6vw;
    top: 45vw;
    left: 38vw;
    -webkit-animation: startplay 1.6s infinite;
    -o-animation: startplay 1.6s infinite;
    animation: startplay 1.6s infinite;
}
.stars-con img:nth-of-type(21) {
    position: absolute;
    width: 6vw;
    top: 52vw;
    left: 33vw;
    -webkit-animation: startplay 1.2s infinite 0.2s;
    -o-animation: startplay 1.2s infinite 0.2s;
    animation: startplay 1.2s infinite 0.2s;
}
.stars-con img:nth-of-type(22) {
    position: absolute;
    width: 6vw;
    top: 59vw;
    left: 28vw;
    -webkit-animation: startplay 3s infinite 1s;
    -o-animation: startplay 3s infinite 1s;
    animation: startplay 3s infinite 1s;
}
.stars-con img:nth-of-type(23) {
    position: absolute;
    width: 6vw;
    top: 66vw;
    left: 23vw;
    -webkit-animation: startplay 2.3s infinite;
    -o-animation: startplay 2.3s infinite;
    animation: startplay 2.3s infinite;
}
.stars-con img:nth-of-type(24) {
    position: absolute;
    width: 6vw;
    top: 45vw;
    left: 65vw;
    -webkit-animation: startplay 1.7s infinite 0.3s;
    -o-animation: startplay 1.7s infinite 0.3s;
    animation: startplay 1.7s infinite 0.3s;
}
.stars-con img:nth-of-type(25) {
    position: absolute;
    width: 6vw;
    top: 53vw;
    left: 70vw;
    -webkit-animation: startplay 2.2s infinite 0.2s;
    -o-animation: startplay 2.2s infinite 0.2s;
    animation: startplay 2.2s infinite 0.2s;
}
.stars-con img:nth-of-type(26) {
    position: absolute;
    width: 6vw;
    top: 61vw;
    left: 75vw;
    -webkit-animation: startplay 1.5s infinite 0.5s;
    -o-animation: startplay 1.5s infinite 0.5s;
    animation: startplay 1.5s infinite 0.5s;
}
.stars-con img:nth-of-type(27) {
    position: absolute;
    width: 6vw;
    top: 69vw;
    left: 80vw;
    -webkit-animation: startplay 2s infinite;
    -o-animation: startplay 2s infinite;
    animation: startplay 2s infinite;
}
.stars-con img:nth-of-type(28) {
    position: absolute;
    width: 6vw;
    top: 68vw;
    left: 40vw;
    -webkit-animation: startplay 2.5s infinite;
    -o-animation: startplay 2.5s infinite;
    animation: startplay 2.5s infinite;
}
.stars-con img:nth-of-type(29) {
    position: absolute;
    width: 6vw;
    top: 35vw;
    left: 50vw;
    -webkit-animation: startplay 1s infinite 1s;
    -o-animation: startplay 1s infinite 1s;
    animation: startplay 1s infinite 1s;
}
</style>
