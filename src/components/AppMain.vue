<script>
    import MainCharacterCard from './MainCharacterCard.vue';
    import axios from 'axios';

    export default {
        components:{
            MainCharacterCard
        },
        
        data() {
    return {
        characters: [],
    }
},
methods:{
    getCharacters(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then((response.data) => {
        console.log(response);
        })
        .catch(function (error) {
        console.log(error);
        })
        .finally(function () {
        });
        }
},
created(){
    this.getCharacters();
}

}
</script>

<template>
    <main>
        <MainCharacterCard/>
    </main>
</template>

<style>

</style>