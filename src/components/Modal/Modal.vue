<template>
  <div class="modal" v-if="showModal" @click="closeModal">
    <div class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
          <div class="md">
            <p>Novo Card</p>
            <div class="label-float">
            <input type="text" placeholder=" " />
            <label>Telefone</label>
          </div>
          <br/>
          <div class="label-float">
            <input type="text" placeholder=" " required/>
            <label>Nome de Usuário</label>
          </div>
          </div> 
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
  props:{
    showModal: Boolean,
  },
  methods:{
    closeModal(event){
      console.log(event.target)
      if (event.target.classList.contains("modal-wrapper")) {
        
        this.$emit("close");
      }
    }
  }
}
</script>

<style scoped>
.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: table;
  transition: opacity 0.3s ease;
}

.label-float {
  position: relative;
  padding-top: 13px;
}

.label-float input{
  width: 600px;
  height: 40px;
  border: 1px solid #C4C4C4;
  border-radius: 5px;
  outline: none;
  min-width: 250px;
  padding: 15px 20px;
  font-size: 16px;
}

.label-float:nth-child(4) input{
  height: 103px;
}

.label-float input::placeholder {
  color: transparent;
}

.label-float label {
  pointer-events: none;
  position: absolute;
  top: calc(50% - 8px);
  left: 15px;
  transition: all .1s linear;
  -webkit-transition: all .1s linear;
  -moz-transition: all .1s linear;
  background-color: white;
  padding: 5px;
  box-sizing: border-box;
}

.label-float input + label,
.label-float input:not(:placeholder-shown)+label {
  font-size: 13px;
  top: 0;
  color: #C4C4C4;
}

.modal-wrapper {
  display: table-cell;
  vertical-align: middle;
}

.modal-container {
  width: 682px;
  height: 463px;
  margin: 0px auto;
  padding: 20px 30px;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
  transition: all 0.3s ease;
  font-family: Helvetica, Arial, sans-serif;
}

.modal-container p:nth-child(1){
  font-family: 'Libre Franklin';
  font-size: 26px;
  font-weight: 600;
  line-height: 31px;
  color: #48409E;
}

.modal-enter .modal-container,
.modal-leave-active .modal-container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
}
</style>