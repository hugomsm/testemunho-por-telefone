<template>
  <q-layout view="lHh Lpr lFf">
    <q-layout-header>
      <q-toolbar color="primary" :inverted="$q.theme === 'ios'">
        <q-btn flat dense round @click="leftDrawerOpen = !leftDrawerOpen" aria-label="Menu">
          <q-icon name="menu"/>
        </q-btn>

        <q-toolbar-title class="absolute-center">Testemunho por Telefone</q-toolbar-title>
      </q-toolbar>
    </q-layout-header>

    <q-layout-drawer
      v-model="leftDrawerOpen"
      :content-class="$q.theme === 'mat' ? 'bg-grey-2' : null"
    >
      <q-list no-border link inset-delimiter>
        <q-list-header>Opções</q-list-header>
        <q-item>
          <q-item-side icon="home"/>
          <q-item-main label="Início"/>
        </q-item>
        <q-item>
          <q-item-side icon="phone"/>
          <q-item-main label="Telefones"/>
        </q-item>
        <q-item>
          <q-item-side icon="perm_identity"/>
          <q-item-main label="Minhas revisitas"/>
        </q-item>
        <q-item>
          <q-item-side icon="settings"/>
          <q-item-main label="Configurações"/>
        </q-item>
      </q-list>
    </q-layout-drawer>

    <q-page-container>
      <router-view/>
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  data(){
    return {
      leftDrawerOpen: false
    }
  },
  name: "MyLayout"
};
</script>

<style>
</style>
