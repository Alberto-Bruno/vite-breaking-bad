<script>
import List from './pokemon/List.vue';
export default {
    components: { List }
}
</script>

<template>
    <main class="container-fluid m-4 text-center overflow-auto">
        <List></List>
    </main>
</template>

<style lang="scss">
main {
    height: 700px;
}
</style>