<template>
  <q-card>
    <q-card-title>{{enderecoSelecionado.endereco}}</q-card-title>
    <q-card-separator/>
    <q-card-main>Última pregação: {{enderecoSelecionado.ultimaPregacao}}</q-card-main>
  </q-card>
</template>

<script>
export default {
  props: ["enderecoSelecionado"],
  // name: 'ComponentName',
  data() {
    return {};
  },
  methods: {}
};
</script>

<style>
</style>
