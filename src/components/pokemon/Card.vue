<script>
export default {
    name: 'Card',
    props: {
        name: String,
        type: String,
        color: String,
        image: String
    }
};
</script>

<template>
    <div class="card-table">
        <img class="shadow-lg" :src="image" :alt="name">
        <div class="type-neme-color">
            <h4> Name: {{ name }}</h4>
            <h4>Tipo: {{ type }}</h4>
            <h4>Color: {{ color }}</h4>
        </div>

    </div>
</template>


<style scoped lang="scss">
.card-table {
    margin-top: 30px;
    border-radius: 20px;

    &:hover {
        cursor: url('../../assets/img/Pokeball.png'), ("https: //freesvg.org/img/Pokeball.png"),
            default;
        cursor: url("https: //freesvg.org/img/Pokeball.png"), auto;
        ;
        filter: grayscale(1);
        box-shadow: 6px 3pz gray;
    }

    .type-name-color {
        background-color: gray;
        border-radius: 15px;
    }

    img {
        height: 150px;
        width: 150px;
        border-radius: 50%;
    }

}
</style>