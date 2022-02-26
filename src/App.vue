<template>
<div id="navbar">
  <v-toolbar app fixed :class="{'elevation-0': this.navbar_transparent}">
      <v-toolbar-title>
        App Name
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-toolbar-items>
        <v-btn flat to="/home">Home</v-btn>
        <v-btn flat @click="scrollTop">Login</v-btn>
      </v-toolbar-items>
  </v-toolbar>
</div>
 
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      is_transparent: true
    }
  },
  methods: {
    onScroll(e) {
      this.is_transparent = !(e.target.scrollTop > 0);
    }
  },
}


</script>


<style>



</style>
