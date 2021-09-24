<template>
  <SearchView/>
  <ul class="border fold">
    <FolderView name="LIST$" :folders="folders" :files="files"/>
  </ul>
</template>

<script>
import FolderView from './components/FolderView.vue'
import SearchView from './components/SearchView.vue'
import data from './data/list';

export default {
  name: 'App',
  components: {
    FolderView,
    SearchView
  },
  data: () => data
}
</script>

<style lang="scss">
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}
.fold {
    list-style: none;
    padding: 0;
    border-left: 1px dotted lightgray;
    border-radius: 5px;
    margin-bottom: 20px;
    margin-top: 20px;
}
li {
    cursor: pointer;
}
li:hover .fas  {
    transform: scale(1.1);
    transition: 0.1s all linear;
}
</style>
