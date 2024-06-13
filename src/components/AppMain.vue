<script>
    import MainCaratteri from './MainCaratteri.vue';
    import MainSearch from './MainSearch.vue';
    import axios from 'axios';
    import { store } from '../store.js'

    export default {
        components:{
            MainCaratteri,
            MainSearch
        },
        
        data() {
    return {
        store
    }
},
methods:{
    getCharacters(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then((response) => {
        console.log(response.data.data);
        this.store.caratteri = response.data.data
        })
        .catch(function (error) {
        console.log(error);
        });
        },
    
    funzioneDiProva() {
        console.log('ciao vito')
    }
},
created(){
    this.getCharacters();
    this.funzioneDiProva();
}

}
</script>

<template>
    <main>
        <MainSearch @cerca="funzioneDiProva"/>
        <MainCaratteri :caratteri="store.caratteri"/>
    </main>
</template>

<style lang="scss" scoped>
    @use './style/partials/mixins.scss' as*;
    @use './style/partials/variabili.scss' as*;
</style>
