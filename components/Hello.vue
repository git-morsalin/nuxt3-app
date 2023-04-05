<template>
    <h1>{{ msg }} ({{ msg.length }})</h1>
    <p>
        <input type="text" v-model="msg">
    </p>
        <button @click="increment">Count is: {{ count }}</button>
    <div>
        
        <h1>{{ helloData }}</h1>
        <h2>{{ treeFruit }} ({{ treeFruit.length }})</h2>
    </div>
</template>
<script setup>
import { ref } from 'vue';
    const count = ref(0)
    let msg = ref("Hello Nuxt with laracast")
    function increment(){
        count.value++
    }
    defineProps({
        helloData: {
            type:String,
            default:"Hello world here free"
        },
        treeFruit: {
            type:String,
            default:"Jackfruit"
        }
    })
    setTimeout(() => {
        msg.value = "Laracast for better"
    }, 3000 );
</script>