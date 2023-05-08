<script>
const countries = [
    {
        id: 'ABW',
        name: "Aruba",
        capital: "Oranjestad",
        area: "180",
    }, {
        id: 'AFG',
        name: "Afghanistan",
        capital: "Kabul",
        area: "652.860",
    }, {
        id: 'AGO',
        name: "Angola",
        capital: "Luanda",
        area: "1.247.000.000",
    }];

export default {

    name: 'CountryDetails',
    data() {
        return {
            id: '',
            name: '',
            capital: '',
            area: '',

        }
    },created() {
        this.$watch(
      () => this.$route.params,
      (newParams, oldParams) => {
        const   ssss  = this.$route.params.id;
        this.id = ssss;
        for(let country of countries){
        if(country.id == this.id){
            this.name = country.name;
            this.capital = country.capital;
            this.area = country.area;
        }
    }

      }
    );

    }
    
}
</script>

<template>
    <div>
          <div class="col-7">
            <img src="https://restcountries.eu/data/fra.svg" alt="country flag" style="width: 300px"/>
            <h1>{{ name }}</h1>
            <table class="table">
              <thead></thead>
              <tbody>
                <tr>
                  <td style="width: 30%">Capital</td>
                  <td>{{ capital }}</td>
                </tr>
                <tr>
                  <td>Area</td>
                  <td>
                    {{ area }} km <sup>2</sup>
                  </td>
                </tr>
              </tbody>
            </table>
          </div>
    </div>
</template>

<style lang="scss" scoped>

</style>