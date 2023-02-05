<template>
  <header>
    <h1>
      <img alt="RamosVeg" src="../assets/logo.png">
    </h1>
    <div class="has-text-centered">
      <button class="button" @click="alterarModo">Ativar modo {{ textoBtn }}</button>
    </div>
    <br>
    <nav class="$panel-shadow">
      <ul class="has-text-centered">
        <li>
          <router-link to="/" class="link">
            <i class="fas fa-tasks"></i>
            tarefas
          </router-link>
        </li>
        <li>
          <router-link to="/projetos" class="link">
            <i class="fas fa-project-diagram"></i>
            projetos
          </router-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue';


export default defineComponent({
  name: "BarraLateral",
  emits: ['aoAlterarModo'],
  data () {
    return {
      modoEscuro: false
    }
  },
  methods: {
    alterarModo () : void {
      this.modoEscuro = !this.modoEscuro
      this.$emit('aoAlterarModo', this.modoEscuro)
    }
  },
  computed: {
    textoBtn () : string {
      return this.modoEscuro ? 'claro' : 'escuro'
    }
  }
});
</script>
<style scoped>
h1 {
  text-align: center;
}
strong {
  color: #f95738;
}
img {
  max-width: 160px;
}
header {
  background: #ffffff;
  width: 100%;
  height: 100vh;
  padding: 2rem;
}
@media only screen and (max-width: 768px) {
  header {
    height: auto;
  }
}
.panel li {
  margin: 8px 0;
}
.link {
  color: #2d9644;
  font-size: larger;
}
.link:hover {
  color: #FAF0CA;
}
.link.router-link-active {
  color: #2d9644;
}
</style>