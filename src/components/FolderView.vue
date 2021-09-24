<template>
  <li class="folder"><i class="fas fa-folder-open"></i> {{name}}</li>


  <template v-for="folder in folders" :key="folder">
    <div class="fold">
    <FolderView :name="folder.name" :folders="folder.folders" :files="folder.files"/>
    </div>
  </template> 
  <template v-for="file in files" :key="file" >
    <FileView :name="file.name" :type="file.type"/>
  </template>
</template>

<script>
import FileView from "./FileView";
export default {
  name: 'FolderView',
  components: {FileView},
  props: {
    name: String,
    folders:Array,
    files:Array,
    type: String,
    visible: Boolean,
  },
  data(){
    return {
      visiable: true,
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.folder{
  color: orangered;
}


.fold:nth-child(2){
  margin-left: 50px;
}
.fold:nth-child(3){
  margin-left: 50px;
}



</style>
