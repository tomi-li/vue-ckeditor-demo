<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <ckeditor :editor="editor" v-model="editorData" :config="editorConfig"></ckeditor>
  </div>
</template>

<script>
import BalloonEditor from '@ckeditor/ckeditor5-build-balloon';

import CKEditor from "@ckeditor/ckeditor5-vue2";

export default {
  name: 'App',
  components: {
    ckeditor: CKEditor.component
  },
  data() {
    return {
      editor: BalloonEditor,
      editorData: '<p>Tomi Test.</p>',
      editorConfig: {
        // The configuration of the editor.
      }
    }
  }
}
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
