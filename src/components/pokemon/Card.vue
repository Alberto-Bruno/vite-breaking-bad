<script>
export default {
    props: {
        name: String,
        type: String,
        color: String,
        image: String
    }
};
</script>

<template>
    <div class="table">
        <img :src="image" :alt="name">
        <div class="pokemon-schedule">
            <h4> Name: {{ name }}</h4>
            <h4>Tipo: {{ type }}</h4>
            <h4>Color: {{ color }}</h4>
        </div>

    </div>
</template>


<style scoped lang="scss">
.table {
    margin-top: 30px;

    img {
        height: 100px;
        width: 100px;
        border-radius: 50%;
    }
}
</style>