<script>
import List from './pokemon/List.vue';
export default {
    components: { List }
}
</script>

<template>
    <main class="container m-5 text-center overflow-auto">
        <List></List>
    </main>
</template>

<style lang="scss">
main {
    height: 500px;
}
</style>