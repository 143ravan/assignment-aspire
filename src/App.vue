<template>
  <div id="app">
    <div class="container">
      <sidebar />
      <Cards class="container--cards" />
    </div>
  </div>
</template>

<script>
import Sidebar from './components/Sidebar.vue'
import Cards from './components/Cards.vue'

export default {
  name: 'App',
  components: {
    Sidebar,
    Cards
  }

}
</script>

<style lang="scss">
  @import '@/variables/utilities';
  html, body {
    margin: 0 !important;
    padding: 0 !important;
  }
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    // text-align: center;
    color: #2c3e50;

    .container {
      display: flex;

      @include mobile {
        display: block;
      }

      &--cards {
        width: 60%;

        @include mobile {
          width: 100%;
          background-color: #0C365A;
        }
      }
    }
  }
</style>
