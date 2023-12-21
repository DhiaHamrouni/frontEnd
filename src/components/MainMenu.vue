<template>
    <v-app id="inspire">
        <v-main>
            <v-container
                class="py-8 px-6"
                fluid
            >
                <v-row >
                    <v-col
                        v-for="card in cards"
                        :key="card"
                        cols="12"
                        class="bg-black text-center"
                    >
                        <v-card >

                            <v-list lines="two">
                                <v-list-subheader>{{ card }}</v-list-subheader>

                                <v-list-item>
                                    <template v-slot:prepend>
                                        <v-avatar color="red">
                                            <v-icon dark>
                                                mdi-alert-circle
                                            </v-icon>
                                        </v-avatar>
                                    </template>

                                    <v-list-item-content>
                                        <v-list-item-title class="text-left"> Timmi Abscence </v-list-item-title>
                                        <v-list-item-subtitle class="text-left">
                                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil repellendus distinctio similique
                                        </v-list-item-subtitle>
                                    </v-list-item-content>


                                </v-list-item>
                            <v-list-item>
                                    <template v-slot:prepend>
                                        <v-avatar color="red">
                                            <v-icon dark>
                                                mdi-alert-circle
                                            </v-icon>
                                        </v-avatar>
                                    </template>

                                    <v-list-item-title class="text-left"> Timmi Abscence </v-list-item-title>
                                    <v-list-item-subtitle class="text-left">
                                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil repellendus distinctio similique
                                    </v-list-item-subtitle>
                                </v-list-item>
                                <v-list-item>
                                    <template v-slot:prepend>
                                        <v-avatar color="gold">
                                            <v-icon dark>
                                                mdi-alert-circle
                                            </v-icon>
                                        </v-avatar>
                                    </template>

                                    <v-list-item-content>
                                        <v-list-item-title class="text-left"> Poplee Entretien </v-list-item-title>
                                        <v-list-item-subtitle class="text-left">
                                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil repellendus distinctio similique
                                        </v-list-item-subtitle>
                                    </v-list-item-content>
                                </v-list-item>
                            </v-list>
                        </v-card>
                    </v-col>
                </v-row>
            </v-container>
        </v-main>
    </v-app>
</template>

<script setup>

const cards = ['All Notifications']


</script>

<script>
export default {
    data: () => ({
        cards: ['All Notifications', 'Yesterday'],
        drawer: null,
    }),
}
</script>