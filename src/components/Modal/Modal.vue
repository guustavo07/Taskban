<template>
  <div class="modal" v-if="showModal" @click="closeModal">
    <div class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
          <div class="md">
            <p>Novo Card</p>
            <div class="label-float">
              <input type="text" placeholder="Digite aqui o título da task" />
              <label>Título da Task</label>
            </div>
            <div class="label-float">
              <textarea type="text" placeholder="Digite a descrição " required/>
              <label>Descrição</label>
            </div>
            <div class="label-float">
              <div>
                <datepicker v-model="selectedDate"></datepicker>
                <label>Data Final</label>
              </div>
              <div class="radios">
                <p id="idP">Priority</p>
                <div class="btn-pr">
                  <button :class="{ active: selectedOption === 1 }" @click="selectOption(1)">HIGH</button>
                  <button :class="{ active: selectedOption === 2 }" @click="selectOption(2)">MEDIUM</button>
                  <button  :class="{ active: selectedOption === 3 }" @click="selectOption(3)">LOW</button>
                </div>
              </div>
            </div>
            <div class="Btns">
              <button>Cancelar</button>
              <button>Criar</button>
            </div>
          </div> 
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Datepicker from 'vuejs-datepicker'; //npm install vuejs-datepicker rodar !!!!!!!!!!!!!!
export default {
  components:{
    Datepicker
  },
  name: "Modal",
  props:{
    showModal: Boolean,
  },
  data(){
    return{
      selectedDate: null,
      selectedOption: null
    };
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
.radios button{
  width: 61px;
  height: 25px;
  padding: 5px, 15px, 5px, 15px;
  border-radius: 100px;
  border: 1px;
}

.btn-pr{
  display: flex;
  width: 232px;
  height: 40px;
  gap: 15px;
}

.radios button:nth-child(1){
  background-color: #FFF;
  border: 1px solid #FF7979;
  color: #FF7979;
}
.radios button:nth-child(2){
  width: 82px;
  background-color: #FFF;
  border: 1px solid #FFBA53;
  color: #FFBA53;
}
.radios button:nth-child(3){
  background-color: #FFF;
  border: 1px solid #2BA700;
  color: #2BA700;
}


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
  width: 280px;
  height: 40px;
  border: 1px solid #C4C4C4;
  border-radius: 5px;
  outline: none;
  min-width: 250px;
  padding: 15px 20px;
  font-size: 16px;
}

.label-float:nth-child(4){
  display: flex;
  gap: 88px;
  align-items: center;
}

.radios{
  width: 232px;
  height: 40px;
}
.label-float textarea{
  width: 600px;
  height: 103px;
  border: 1px solid #C4C4C4;
  border-radius: 5px;
  outline: none;
  min-width: 250px;
  padding: 15px 20px;
  font-size: 16px;
  resize: none;
}

.label-float input::placeholder {
  color: #C4C4C4;
}
.label-float textarea::placeholder {
  color: #C4C4C4;
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
.label-float textarea + label,
.label-float textarea:not(:placeholder-shown)+label {
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

#idP{
  margin-bottom: 10px;
  font-family: Libre Franklin;
  font-size: 11px;
  font-weight: 400;
  line-height: 13px;
  letter-spacing: 0em;
  text-align: left;
  color: #6F6F6F;
}
.modal-enter .modal-container,
.modal-leave-active .modal-container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
}
.Btns{
  width: 100%;
    display: flex;
    margin-top: 65px;
    justify-content: end;
    gap: 30px;
}

.Btns button:nth-child(1){
  width: 180px;
  height: 37px;
  border-radius: 20px;
  border: 2px solid #FF7979;
  padding: 10px, 200px, 10px, 200px;
  background-color: #FFF;
  color: #FF7979;
  font-family: Libre Franklin;
  font-size: 14px;
  font-weight: 600;
  line-height: 17px;
  letter-spacing: 0em;
  text-align: center;
}
.Btns button:nth-child(2){
  width: 180px;
  height: 37px;
  border-radius: 20px;
  border: 2px solid #48409E;
  padding: 10px, 200px, 10px, 200px;
  background-color: #48409E;
  color: #FFF;
  font-family: Libre Franklin;
  font-size: 14px;
  font-weight: 600;
  line-height: 17px;
  letter-spacing: 0em;
  text-align: center;

}
</style>