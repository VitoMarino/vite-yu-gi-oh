<script>
export default {
        data() {
    return {
        
    }
},
props: {
    caratteri:{
        type: Array,
        required: true
        }
    }
}
</script>

<template>
    <ul>
        <li v-for="item in caratteri" :key="item.id">
            {{ item.name }}
        </li>
    </ul>
</template>

<style lang="scss" scoped>
    @use './style/partials/mixins.scss' as*;
    @use './style/partials/variabili.scss' as*;

</style>