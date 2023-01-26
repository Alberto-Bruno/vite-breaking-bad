<script>
import { store } from '../../store/store';
export default {
    name: 'Pokemon',
    data() {
        return {
            store,
        }
    },
}
</script>


<template>
    <div class="container d-flex justify-content-end shadow  w-25 form-floating">
        <select class="form-select">
            <option selected>Tutti</option>
            <option v-for="poke in store.type" :key="poke" :value="poke">{{ poke }}</option>
        </select>

    </div>

</template>

<style>

</style>