<template>
  <v-layout>
    <!-- <v-system-bar color="deep-purple darken-3"></v-system-bar> -->

    <!-- sidebar -->
    <SideBar v-model="drawer" />

    <!-- Navbar -->
    <NavBar @openClose="drawerOpenClose" />

    <!-- Main -->
    <v-main style="height: 500px;">
      <v-card-text>
        <RouterView />
      </v-card-text>
    </v-main>
  </v-layout>
</template>

<script setup>
import { ref, provide } from 'vue'
import SideBar from './components/SideBar.vue'
import NavBar from './components/NavBar.vue'
import { RouterView } from 'vue-router'

const drawer = ref(true)

provide('username', 'Salman')

const drawerOpenClose = () => {
  drawer.value = !drawer.value
}
</script>