<template>
    <v-navigation-drawer color="blue-lighten-4" location="left">
        <ListSideBar :items="items" />
    </v-navigation-drawer>
</template>

<script setup>
import { ref } from 'vue'
import ListSideBar from './ListSideBar.vue'

const items = ref([
    { text: 'Dashboard', icon: 'mdi-view-dashboard', path: '/' },
    { text: 'Categories', icon: 'mdi-view-list', path: '/categories' },
    { text: 'News', icon: 'mdi-newspaper-variant-outline', path: '/news' },
    { text: 'Profile', icon: 'mdi-account', path: '/profile' },
])
</script>