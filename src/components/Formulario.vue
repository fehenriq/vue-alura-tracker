<template>
  <div class="box">
    <div class="columns">
      <div class="column is-8" role="form" aria-label="Formulário para criação de uma nova tarefa">
        <input type="text" class="input" placeholder="Qual tarefa você deseja iniciar?" v-model="descricao">
      </div>
      <div class="column">
        <Temporizador @aoTemporizadorFinalizado="finalizarTarefa"/>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Temporizador from './Temporizador.vue';

export default defineComponent({
  name: "FormulárioBase",
  components: { Temporizador },
  data () {
    return {
      descricao: ''
    }
  },
  methods: {
    finalizarTarefa (tempoDecorrido: number) : void {
      console.log('%cFormulario.vue line:28 tempo da tarefa', 'color: #007acc;', tempoDecorrido)
      console.log('%cFormulario.vue line:29 descricao da tarefa', 'color: #007acc;', this.descricao);
      this.descricao = ''
    }
  }
});
</script>