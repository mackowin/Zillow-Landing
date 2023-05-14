<template>
    <router-view></router-view>
</template>
<script>

  import { mapActions } from 'vuex'

  export default {
  name: 'app',
  components: {

  },
    methods: {
      ...mapActions({
        clearAlert: 'alert/clear'
      })
    },
    watch: {
      $route (){
        this.clearAlert();
      }
    },
    metaInfo() {
    return {
      title: "Find cash flow on Zillow",
      meta: [
        { vmid: 'description', name: 'description', content:  'Get rents in one click and screen properties with the highest returns. Say goodbye to extracting Zillow data manually, and entering property details in your excel spreadsheet. Get average asking rent in the neighborhood and returns in one click and sort by price, rent and returns to screen ONLY the best listings.'},
        { vmid: 'ogtitle', property: 'og:title', content: "Find cash flow on Zillow"},
        { vmid: 'ogsite', property: 'og:site_name', content: 'Find cash flow on Zillow'},
        { vmid: 'ogtype', property: 'og:type', content: 'Find cash flow on Zillow'},
      ]
    }
  }
}
</script>
