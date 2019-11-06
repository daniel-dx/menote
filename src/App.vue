<template>
  <div id="editor">
    <editor />
  </div>
</template>

<script>
import Editor from '@/components/Editor.vue'

// import Editor from '../dist/menote.js'
// import '../dist/static/css/menote.min.css'

export default {
  name: 'app',
  components: {
    Editor
  }
}
</script>

<style>
</style>
