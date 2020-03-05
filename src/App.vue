<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <div class="form">
      <small>Choisissez une moto:</small>
      <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
      <Multiselect :options="selectOptions" placeholder="Choisissez une moto"/>
    </div>
    
  </div>
</template>

<script>
import Multiselect from './components/Multiselect.vue'

const MultiselectOptions = ['Suzuki GSXR 1000', 'Yamaha MT07', 'Yamaha MT09', 'Kawasaki Z1000', 'BMW K1200S'];

export default {
  name: 'App',
  components: {
    Multiselect
  },
  computed: {
    selectOptions() {
      return MultiselectOptions;
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  .form {
    width: 300px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin: auto;
  }
}

</style>
