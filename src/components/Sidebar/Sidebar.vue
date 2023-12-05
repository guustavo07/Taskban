<template>
  <div>
    <b-sidebar id="sidebar-1" title="Sidebar" shadow class="custom-sidebar">
      <span>TASKBAN</span>
      <div class="side">
        <a class="options" href="">
          <img src="../../assets/ci_dashboard-02.png" alt="Quadro">
          Quadro
        </a>
        <a class="options" href="">
          <img src="../../assets/calendario.png" alt="Imagem 2">
          Lista
        </a>
        <a class="options" href="">
          <img src="../../assets/clarity_timeline-line.png" alt="Imagem 3">
          Timeline
        </a>
        <a class="options" href="">
          <img src="../../assets/calendario.png" alt="Imagem 4">
          Calendário
        </a>
      </div>
    </b-sidebar>
  </div>
</template>

<style>
.side{
  display: flex;
  flex-direction: column;
  padding: 10px 10px;
}
.custom-sidebar {
  background-color: #FFF; 
  box-shadow: 4px 0px 30px 10px #0000000D;
  position: fixed;
  top: 0; 
  left: 0; 
  bottom: 0; 
  width: 300px; 
}

.custom-sidebar a {
  display: flex;
  align-items: center;
  padding: 8px 60px;
  gap: 20px;
  color: #494949;
  text-decoration: none;
  transition: background-color 0.3s ease;
}

/* Estilo hover para os links no sidebar */
.custom-sidebar a:hover {
  background-color: #c9c9c9;
}

/* Estilo para o conteúdo principal da aplicação */
.main-content {
  margin-left: 200px; /* Ajuste conforme a largura do sidebar */
  padding: 20px; /* Adicione algum espaçamento para evitar sobreposição com o sidebar */
}
.options{
  color: #48409E;
}
span{
  display: flex;
    height: 100px;
    width: 100%;
    color: #48409E;
    font-weight: 700;
    font-family: K2D;
    font-size: 36px;
    margin-top: 56px;
    margin-right: 66px;
    justify-content: center;
}

</style>
