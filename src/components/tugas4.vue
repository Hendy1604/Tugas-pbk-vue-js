<script setup>

    import {ref} from 'vue';

    const number = ref();
    let result = ref();
    let container = ref('uppCase');

    

    function count(){
        result.value = eval(number.value);
    }

    function gayaFont(){
        if(container.value == 'lowCase'){
            container.value = 'uppCase';
        } else {
            container.value = 'lowcase';
        }
    }

</script>

<template>

        <div v-bind:class="container">
        <input type="text" placeholder="Masukkan angka" v-model="number">
        <button v-on:click="count">count</button>
        <button v-on:click="gayaFont">Ubah Gaya</button>

        <br><br>

        <div>Soal: <br> <b> {{ number }}</b></div><br>
        <div>Jawaban: <br> <b> {{ result }}</b></div>
        </div>



</template>

<style scoped>
    .lowCase {
        text-transform: lowercase;
    }

    .uppCase {
        text-transform: uppercase;
    }


</style>