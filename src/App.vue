<script>
import NavBar from './components/NavBar.vue';
import CountriesList from './components/CountriesList.vue';
import CountryDetails from './components/CountryDetails.vue';

export default {
  data(){
    return {

    }
  }, components: {
    NavBar,
    CountriesList,
    CountryDetails
  }
}
</script>

<template>
  <div class="app">
    
    <NavBar></NavBar>
    <router-view></router-view>
  </div>
</template>

<style>

</style> 