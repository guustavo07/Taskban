<template>
  <div id="nav">
    <button @click="openModal">+ Novo Card</button>
    <Modal :showModal="isModalVisible" @close="closeModal"/>
  </div>
</template>

<script>
import Modal from '../Modal/Modal.vue';

export default {
  components: {
    Modal
  },
  name: "Navbar",
  data(){
    return{
      isModalVisible: false,
    };
  },
  methods: {
    openModal() {
      this.isModalVisible = true;
    },
    closeModal(){
      this.isModalVisible = false;
    }
  },
};
</script>

<style scoped>
#nav {
  width: 100%;
  height: 90px;
  background-color: #48409E;
  box-shadow: 0px 4px 10px 0px #0000001A;
  padding: 15px 50px;
  display: flex;
  justify-content: flex-end;
  align-items: center;
}
button {
  background-color: #BFB9FF;
  width: 147px;
  height: 55px;
  padding: 18px 21px 18px 23px;
  border-radius: 10px;
  color: #fff;
  font-family: 'Libre Franklin';
  font-weight: 500;
  font-size: 18px;
  line-height: 21px;
  border: none;
  outline: none;
}
</style>
