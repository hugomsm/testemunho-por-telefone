<template>
  <q-page padding>
    <router-view/>
    <grid-enderecos></grid-enderecos>
  </q-page>
</template>

<script>
import gridEnderecos from "../components/gridEnderecos.vue";

export default {
  // name: 'PageName',
  components: {
    gridEnderecos: gridEnderecos
  }
};
</script>

<style>
</style>
