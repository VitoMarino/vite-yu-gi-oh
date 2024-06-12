<script>
import AppFooter from './AppFooter.vue';
import AppHeader from './AppHeader.vue';
import AppMain from './AppMain.vue';

export default {
  data() {
    return {

    }
  },
  components:{
    AppHeader,
    AppMain,
    AppFooter
  }
}
</script>

<template>
  <AppHeader/>

  <AppMain/>

  <AppFooter/>
</template>

<!--Se non inserisco lo scope TUTTE le regole saranno applicate a TUTTA la mia applicazione. 
In questo caso è quello che voglio dato che questa (APP.Vue) è la madre di tutte-->

<!--QUESTO VALE PER IL GENERAL. Se voglio usare le PARTIALS, devo importarlo nel singolo file
dove voglio venga applicata quella regola. Altrimenti non lo importa.-->
<style lang="scss">
  @use '../style/general.scss';
  @use '../style/partials/mixins';
  @use '../style/partials/variabili';
</style>
