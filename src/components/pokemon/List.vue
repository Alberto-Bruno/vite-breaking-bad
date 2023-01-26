<script>
import { store } from '../../store/store';
import Card from './Card.vue';
export default {
    components: { Card },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="row row-cols-md row-cols-3 mx-5">
        <card v-for="poke in store.pokemon" :key="poke.id" class="" :name="poke.name" :image="poke.imageUrl"
            :type="poke.type1" :color="poke.color">
        </card>
    </div>
</template>