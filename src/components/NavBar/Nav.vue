<template>
  <div id="nav">
    <button>+ Novo Card</button>
  </div>
</template>

<script>
export default {
  name: "Navbar"
}
</script>

<style scoped>
   #nav {
    width: 100%;
    height: 10%;
    background-color: #48409E
;
    padding: 15px 50px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
  }
  button{
    background-color: #BFB9FF;
    width: 147px;
    height: 58px;
    border-radius: 10px;
    color: #fff;
    font-family: 'Libre Franklin';
    font-weight: 500;
    font-size: 18px;
    line-height: 21px;
  }

</style>