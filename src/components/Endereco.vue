<template>
  <q-card @click.native="navigateToTelefones">
    <q-card-title>{{enderecoSelecionado.endereco}}</q-card-title>
    <q-card-separator/>
    <!-- <q-card-main>Última pregação: {{enderecoSelecionado.ultimaPregacao}}</q-card-main> -->
  </q-card>
</template>

<script>
export default {
  props: ["enderecoSelecionado"],
  // name: 'ComponentName',
  data() {
    return {};
  },
  methods: {
    navigateToTelefones() {
      const id = this.enderecoSelecionado.id.toString();
      const url = `pageEnderecos/pageTelefones/${id}`;
      this.$router.push(`${url}`);
    }
  }
};
</script>

<style>
</style>
