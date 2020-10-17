<template>
    <div class="container">
        <input type="text" v-model="inputTarea" @keyup.enter="agregarTarea">
        <button @click="agregarTarea" >Agregar Tarea</button>
        <ul v-if="listaTarea.length != 0">
            <li v-for="(tarea, key) in listaTarea" :key="key">{{tarea}}</li>
        </ul>
        <h3 v-else>
            No hay tareas pendientes
        </h3>

    </div>

</template>

<script>
export default {
    name: 'ToDoList',
    data(){
        return {
            inputTarea: '',
            listaTarea: []
        }
    },
    methods: {
        agregarTarea(){
            if(this.inputTarea == '') return false;
            this.listaTarea.push(this.inputTarea);
            this.inputTarea = '';
        }
    },
}
</script>

<style scoped>
    .container{
        height: 470px;
        max-width: 1140px;
        display: block;
        margin: 50 auto;
    }

    button{
        background-color: #662e9b;
        color: white;
    }
</style>