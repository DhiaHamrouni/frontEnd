<template>
    <v-navigation-drawer v-model="drawer" expand-on-hover rail>
        <v-sheet class="bg-yellow-darken-2">
            <v-avatar class="mb-4" color="grey darken-1" size="64">
                <v-img src="/src/assets/logo.png" contain></v-img>
            </v-avatar>

            <div style="font-family: 'Tahoma'">John.Doe@email.com</div>
        </v-sheet>

        <v-divider></v-divider>

        <v-list>
            <v-list-item v-for="([icon, text, number], index) in links" :key="index" link>
                <template v-slot:prepend>
                    <v-icon>{{ icon }}</v-icon>
                </template>

                <v-list-item-title>{{ text }}</v-list-item-title>

                <template v-slot:append>
                    <v-badge color="grey" overlap>
                        <template v-slot:badge>{{ number }}</template>
                    </v-badge>
                </template>
            </v-list-item>
        </v-list>
    </v-navigation-drawer>
</template>

<script setup>
import { ref } from 'vue'
const links = [
    ['mdi-email', 'Applications',3],
    ['mdi-account', 'Poplee Entretiens',1],
    ['mdi-currency-usd', 'Cleemy Notes de frais', 0],
    ['mdi-account-alert', 'Timmi Abscences', 2],
]
const drawer = ref(null)
</script>
