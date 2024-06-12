<script>
    import MainCaratteri from './MainCaratteri';
    import axios from 'axios';

    export default {
        components:{
            MainCaratteri
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
        console.log(response.data);
        this.characters = response.data;
        })
        .catch( function (error) {
        console.log(error);
        })
        .finally(function (){
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
        <MainCaratteri :characters="characters"/>
    </main>
</template>

<style lang="scss" scoped>

</style>
