29 lines (25 sloc)  736 Bytes

<script>
import axios from 'axios';
import Card from './Card.vue';
export default {
    components: { Card },
    data() {
        return {
            pokemon: []
        }
    },
    created() {
        axios.get('https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?per=10&page=21')
            .then(res => {
                this.pokemon = res.data.docs;
            })
    }
}
</script>

<template>

    <div class="row g-4 row-cols-2 row-cols-md-3 mx-4">
        <card v-for="poke in pokemon" :key="poke.id" class="" :name="poke.name" :image="poke.imageUrl"
            :type="poke.type1" :color="poke.color"> </card>
    </div>

</template>