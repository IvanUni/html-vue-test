<template>

    <li class="file">
      <i class="fas fa-file-image" v-if="type == 'image/svg' || type == 'image/jpeg' || type == 'image/png'"></i> 
      <i class="fas fa-file-alt" v-if="type == 'application/octet-stream' || type == 'text/plain'"></i> 
      <i class="fas fa-file-code" v-if="type == 'application/javascript' || type == 'application/json'"></i> 
      
      {{name}}
    </li>

</template>

<script>
export default {
  name: 'FileView',
  props: {
    name: String,
    type: String,
  }
}
</script>

<style scoped lang="scss">
.file{
  color: green;
  margin-left: 50px;
}

</style>
