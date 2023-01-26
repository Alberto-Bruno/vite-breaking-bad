<script>
import axios from 'axios';
import { store } from './store/store';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import pokemon from './components/pokemon/pokemon.vue';

const urlType = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?&type1=';
export default {
    components: { AppHeader, AppMain, pokemon },
    data() {
        return {
            store,
            pokemon: '',
        }
    },
    methods: {
        fetchPokemon(url) {
            axios.get(url)
                .then(res => {
                    store.pokemon = res.data.docs;
                })
        },
        fetchGeneric(url) {
            axios.get(url)
                .then(res => {
                    store.type = res.data;
                    console.log(store.type)
                })
        }
    },
    created() {
        this.fetchPokemon(store.apiUri)
        this.fetchGeneric(store.apiType)
    }
}
</script>

<template>
    <app-header></app-header>
    <pokemon></pokemon>
    <app-main></app-main>
</template>

<style lang="scss">
@use './assets/styles/style.scss';
</style>