<template>
  <header>
    <div class="navbar navbar-default">
      <div class="navbar-header">
        <h1>
          <router-link :to="{name: 'iMain'}"> {{sitename}} </router-link>
        </h1>
      </div>
      <div class="nav navbar-nav navbar-rigth cart">
        <button type="button" class="btn btn-default btn-lg" v-on:click="showCheckout">
          <span class="glyphicon glyphicon-­shopping ­cart">
            {{cartItemCount}}
          </span> Checkout
        </button>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'my-header',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      sitename: "Vue.js Pet Depot"
    }
  },
  props: ['catrtItemCount'],
  methods: {
    showCheckout() {
      this.$router.push({name: 'Form'});
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a {
  text-decoration: none;
  color: #000000;
}
</style>
