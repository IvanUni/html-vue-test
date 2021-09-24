<template>
  <ul class="border fold" v-on:click="visible=!visible">
    <FolderView name="LIST$" :folders="folders" :files="files" visible="true"/>
  </ul>
</template>

<script>
import FolderView from './components/FolderView.vue'
import data from './data/list';

export default {
  name: 'App',
  components: {
    FolderView
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
  border-left: 1px dotted lightgray;
  border-radius: 5px;
  margin-bottom: 20px;
  margin-top: 20px;
}
</style>
