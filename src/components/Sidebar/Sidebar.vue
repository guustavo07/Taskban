<template>
  <div>
    <b-sidebar id="sidebar-1" title="Sidebar" shadow class="custom-sidebar">
      <span>TASKBAN</span>
      <div class="side">
        <a class="options" href="">Quadro</a>
        <a class="options" href="">Lista</a>
        <a class="options" href="">Timeline</a>
        <a class="options" href="">Calendário</a>
      </div>
    </b-sidebar>
  </div>
</template>

<style>
.side{
  padding: 10px 10px;
}
.custom-sidebar {
  background-color: #FFF; 
  position: fixed; /* Define o posicionamento fixo */
  top: 0; /* Alinha o topo do sidebar com o topo da janela */
  left: 0; /* Alinha a esquerda do sidebar com a esquerda da janela */
  bottom: 0; /* Ocupa a altura total da janela */
  width: 300px; /* Largura desejada para o sidebar */
}

/* Estilo para os links dentro do sidebar */
.custom-sidebar a {
  display: block;
  padding: 8px 16px;
  color: #494949;
  text-decoration: none;
  transition: background-color 0.3s ease;
}

/* Estilo hover para os links no sidebar */
.custom-sidebar a:hover {
  background-color: #FFF;
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
