<script>
export default {
        data() {
    return {
        store
    }
},

}
</script>

<template>
    <div v-for="item in store.caratteri" :key="item.id">
        <img :src="item.card_images[0].image_url" alt="Card">
        <h3>
            {{ item.name }}
        </h3>
    </div>
</template>

<style lang="scss" scoped>
    @use './style/partials/mixins.scss' as*;
    @use './style/partials/variabili.scss' as*;

    div{
        margin: 2rem;
        padding: .5rem;
        width: (100% / 5);
    }
    img{
        width: 200px;
    }

</style>