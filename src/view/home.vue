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
        <var-image style="width: 25%; position: absolute; top: 70%; left: 37.5%" :src="p3_b" />
        <var-image :src="bg3" />
    </div>
    <div style="position: relative">
        <var-image style="width: 25%; position: absolute; top: 70%; left: 37.5%" :src="p4_b" />
        <var-image :src="bg4" />
    </div>
    <div style="position: relative">
        <var-image style="width: 25%; position: absolute; top: 70%; left: 37.5%" :src="p2_b" />
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
import bg4 from '../assets/img/pg-4.png'
import pg5 from '../assets/img/pg5-bg.png'

import p2_b from '../assets/img/p2-but.png'
import p3_b from '../assets/img/p3-but.png'
import p4_b from '../assets/img/p4-but.png'

import mes_1 from '../assets/img/mes-1.png'

const center = ref(false)
</script>

<style scoped></style>
