<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <button class="btn btn-secondary" @click.prevent="decreasing">Decrease</button>
      </div>
      <div class="col">
        <input type="number" class="form-control" placeholder="0" v-model="counter" readonly>
      </div>
      <div class="col">
        <button class="btn btn-secondary" @click.prevent="increasing">Increase</button>        
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
  },
  computed: {
    counter() {
      return this.$store.state.counter
    }
  },
  methods: {
    increasing() {
      this.$store.dispatch('increaseCounter')
    },
    decreasing() {
      this.$store.dispatch('decreaseCounter')
    }
  },
  
}

//Option API & Composition API
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
