<template>
    <div class="container">
        <input type="text" v-model="inputTarea" @keyup.enter="agregarTarea">
        <button @click="agregarTarea" >Agregar Tarea</button>
        <ul v-if="listaTarea.length != 0">
            <li v-for="(tarea, key) in listaTarea" :key="key"><strong>{{tarea}}</strong></li>
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
        display: flex;
        flex-flow: column wrap;
        justify-content: center;
        align-items: center;
        margin: 0 auto;
    }
    input{
        width: 400px;
        color: #662e9b;
        font-size: 1.2rem;
        margin-bottom: 10px;
    }
    button{
        background-color: #662e9b;
        color: white;
        border: none;
        width: 250px;
        border-radius: 9px;
        font-size: 1.2rem;
    }
    ul{
        padding: 0;
    }
    li{
        list-style: none;
    }
</style>