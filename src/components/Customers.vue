<template>
  <div class="customers container">
    <h1 class="page-header">Manage Customers</h1>
  </div>
</template>

<script>
export default {
  name: 'customers',
  data () {
    return {
     customers: []
    }
  },
  methods: {
    fetchCustomers(){
      this.$http.get('http://slimapp/api/customers')
      .then(function(response){
        console.log(response.body);
      });
    }
  },
  created: function(){
    this.fetchCustomers();
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
