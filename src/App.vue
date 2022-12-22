<template>
  <DefaultNavbar />
  <div id="content">
    <SearchField class="search" :handleSearch="handleSearch" />
  </div>
</template>

<script>
import SearchField from './components/SearchField.vue'
import DefaultNavbar from './components/DefaultNavbar.vue'

export default {
  name: 'App',
  components: {
    SearchField,
    DefaultNavbar
  },
  methods: {
    handleSearch(e) {
      this.query = e.target.value;

      if (this.query && !this.query.match(/(?:(?:https?|ftp):\/\/|\b(?:[a-z\d]+\.))(?:(?:[^\s()<>]+|\((?:[^\s()<>]+|(?:\([^\s()<>]+\)))?\))+(?:\((?:[^\s()<>]+|(?:\(?:[^\s()<>]+\)))?\)|[^\s`!()[\]{};:'".,<>?«»“”‘’]))?/)) {
        e.target.parentElement.style.transform = 'translateY(-800%)';
        e.target.parentElement.style.marginBottom = '-4px';
      } else {
        e.target.parentElement.style.transform = '';
        e.target.parentElement.style.marginBottom = '72px';
      }     
    }
  },
  data() {
    return {
      query: ''
    }
  },
  mounted() {}
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
  font-family: sans-serif;
  background: #000;
  color: #fff;
  height: 100vh;
  width: 100vw;
  margin: 0 auto;
}

#app {
  height: 100%;
  width: 100%;
}

#content {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;

  display: flex;
  flex-direction: column;
  justify-content: center;
  
  height: 90%;
  width: 50%;
  margin: 0 auto;
}

</style>
