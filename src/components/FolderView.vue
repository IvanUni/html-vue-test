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

.fold li:hover {border-left: 10px solid transparent;}
.fold .file {border-left: 10px solid green;}
.fold .folder {border-left: 10px solid orangered;}
.fold .file:hover {border-right: 10px solid green;}
.fold .folder:hover {border-right: 10px solid orangered;}
.fold li {
    font-family: "Trebuchet MS", "Lucida Sans";
    padding: 7px 20px;
    margin-bottom: 10px;
    border-radius: 5px;
    border-left: 10px solid #f05d22; 
    box-shadow: 2px -2px 5px 0 rgba(0,0,0,.1),
            -2px -2px 5px 0 rgba(0,0,0,.1),
        2px 2px 5px 0 rgba(0,0,0,.1),
        -2px 2px 5px 0 rgba(0,0,0,.1);
    font-size: 20px;
    letter-spacing: 2px;
    transition: 0.1s all linear;
}

.folder{
    color: orangered;
}
.fold:nth-child(2){
    margin-left: 50px;
}
.fold:nth-child(3){
    margin-left: 50px;
}
.fold {
    border-left: 1px dotted lightgray;
    border-radius: 5px;
    margin-bottom: 20px;
    margin-top: 20px;
}
</style>
