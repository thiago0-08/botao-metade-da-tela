template
<div>
    <!-- Botão para abrir o componente de perfil -->
    <button @click="opentesteComponente">Abrir Perfil</button>

    <!-- Página/metade da tela usando o componente "testeComponente" -->
    <div v-if="showtesteComponente" class="half-screen">
      <!-- Inclui o componente testeComponente e passa o evento de fechar -->
      <testeComponente @close="closetesteComponente" />
    </div>
  </div>


script
const showtesteComponente = ref(false);

// Função para abrir o componente testeComponente
const opentesteComponente = () => {
  showtesteComponente.value = true;
};

// Função para fechar o componente testeComponente
const closetesteComponente = () => {
  showtesteComponente.value = false;
};

style
.half-screen {
  position: fixed;
  top: 0;
  right: 0;
  width: 50%;
  height: 100%;
  background-color: #f0f0f0;
  box-shadow: -2px 0 10px rgba(0, 0, 0, 0.2);
  padding: 20px;
  z-index: 1000;
}
