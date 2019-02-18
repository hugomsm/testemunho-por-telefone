<template>
  <div>
    <endereco
      v-for="endereco in enderecos"
      :key="endereco.id"
      :enderecoSelecionado="endereco"
      inline
      style="max-width: 300px"
      class="q-ma-md"
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
          id: 1,
          endereco: "Rua XXX, 53",
          ultimaPregacao: new Date().toString(),
          telefones: []
        },
        {
          id: 2,
          endereco: "Rua AAA, 54",
          ultimaPregacao: new Date().toString(),
          telefones: []
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
