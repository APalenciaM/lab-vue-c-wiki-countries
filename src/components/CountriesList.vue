<script>
export default {
    name: 'CountriesList',
    data(){
        return{
            id:'',
            id2: '',
        }
    },
    created() {
        
        const  ssss  = this.$route.params.id;
        console.log(ssss);
        this.id = "ABW";
        this.id2 = "AFG"
    }
    
}

</script>

<template>
    <div>
        <div class="container">
        <!-- Bootstrap row wrapper div -->
        <div class="row">
          <!-- Countries List (Bootstrap column) -->
          <div class="col-5" style="max-height: 90vh;">
            <div class="list-group" style="overflow: hidden;">
                <router-link :to="`/list/${id}`">A</router-link>
                <router-link :to="`/list/${id2}`">B</router-link>
                <router-link :to="`/list/${id}`">
                    <a class="list-group-item list-group-item-action">
                        <img src="https://flagpedia.net/data/flags/icon/72x54/aw.png" />
                        <p>Aruba</p>
                    </a>
                </router-link>
                <router-link :to="`/list/${id2}`">
                    <a class="list-group-item list-group-item-action">
                        <img src="https://flagpedia.net/data/flags/icon/72x54/af.png" />
                        <p>Afghanistan</p>
                    </a>
                </router-link>
                <router-link to="/list/AGO">
                    <a class="list-group-item list-group-item-action">
                        <img src="https://flagpedia.net/data/flags/icon/72x54/ao.png" />
                        <p>Angola</p>
                    </a>
                </router-link>


            </div>
          </div>
          <router-view></router-view>


        </div>
      </div>
    </div>
</template>

<style lang="scss" scoped>

</style>