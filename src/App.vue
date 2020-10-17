<template>
  <div id="app">
    <encabezado-app>To Do List</encabezado-app>
    <to-do-list></to-do-list>
    <pie-app>©Curso Full-Stack Doctadevs</pie-app>
  </div>
</template>

<script>
import EncabezadoApp from './components/EncabezadoApp'
import ToDoList from './components/ToDoList'
import PieApp from './components/PieApp'

export default {
  name: 'App',
  components: {
    EncabezadoApp,
    ToDoList,
    PieApp
  }
}
</script>

<style>
  body{
    font-family: Verdana;
    margin: 0 auto;
  }
</style>
