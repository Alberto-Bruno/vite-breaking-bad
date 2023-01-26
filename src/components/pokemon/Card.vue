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
        <img :src="image" :alt="name">
        <div class="type-neme-color">
            <h5> Name: {{ name }}</h5>
            <h5>Tipo: {{ type }}</h5>
            <h5>Color: {{ color }}</h5>
        </div>

    </div>
</template>


<style scoped lang="scss">
.card-table {
    margin-top: 100px;
    border-radius: 15px;

    &:hover {
        filter: grayscale(1);
        box-shadow: 0 0 4px 4px gray;
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