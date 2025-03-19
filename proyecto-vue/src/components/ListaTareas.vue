<template>
    <div>
        <h2>Lista de tareas</h2>
        <input type="text" v-model="nuevatarea" @keyup.enter="addtarea">
        <ul>
            <li v-for="(tareas,index) in tareas" :key="index">
                {{ tareas }}
            </li>
        </ul>
    </div>
</template>



<script setup>
import {ref} from 'vue';
const tareas =ref([]);
const nuevatarea =ref('');
const addtarea = () =>{
    tareas.value.push(nuevatarea.value)
    nuevatarea.value='';

} 
</script>



<style>

</style>