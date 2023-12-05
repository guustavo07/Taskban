<template>
  <div id="app">
    <Nav/>
    <Sidebar/>
  </div>
</template>

<script>
  import Nav from './components/NavBar/Nav.vue'
  import Sidebar from './components/Sidebar/Sidebar.vue'
  export default{
    name: "Home",
    components:{
      Nav,
      Sidebar
    }
  }
</script>

<style>
  * {
    font-family: Helvetica;
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }
  #app {
  width: 100%;
  height: 100vh; /* 100% da altura da viewport */
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #bfb9ff27; /* Para evitar barras de rolagem desnecessárias */
}
  .main-container {
    margin: 50px;
    min-height: 250px;
  }
  h1 {
    text-align: center;
    font-size: 42px;
    margin-bottom: 30px;
    color: #222;
  }
</style>
