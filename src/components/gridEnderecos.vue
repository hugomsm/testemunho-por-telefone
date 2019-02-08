<template>
  <div>
    <endereco
      v-for="endereco in enderecos"
      :key="endereco.id"
      :enderecoSelecionado="endereco"
      inline
      style="max-width: 300px"
    ></endereco>
    <!-- botão pra cadastrar novo endereço -->
  </div>
</template>

<script>
import Endereco from "../components/Endereco.vue";

export default {
  // name: 'ComponentName',
  data() {
    return {
      // carregar enderecos do bd do back
      enderecos: [
        {
          endereco: "Rua XXX, 53",
          ultimaPregacao: new Date().toString()
        }
      ]
    };
  },
  components: {
    Endereco: Endereco
  }
};
</script>

<style>
</style>
