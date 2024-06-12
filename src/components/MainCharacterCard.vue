<script>
    export default {
        components:{
            MainCharacterCard
        },
        data() {
            return {

        }
    },
    props:{
        characters: {
            type: Array,
            required: true
        }
    }
}
</script>

<template>
    <main>
        <p>
            {{ characters.lenght }}
        </p>
    </main>
</template>

<style>

</style>