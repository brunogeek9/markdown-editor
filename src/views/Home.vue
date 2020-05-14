<template>
  <div id="home">
    <div id="md" class="col-md-6">
      <h2 class="text-success text-center">Enter Markdown Text</h2>
      <textarea style="height:auto" rows="16" class="form-control" v-model="md_text"></textarea>
    </div>
    <div id="preview" class="col-md-6">
      <h2 class="text-success text-center">Preview</h2>
      <div class="well well-sm pre-scrollable" v-html="previewText"></div>
    </div>
  </div>
</template>
<script>
let marked = require("marked");
export default {
  name: "app",
  data() {
    return {
      md_text: "# Title"
    };
  },
  computed: {
    previewText() {
      marked.setOptions({
        renderer: new marked.Renderer(),
        gfm: true,
        tables: true,
        breaks: true,
        pedantic: false,
        sanitize: true,
        smartLists: true,
        smartypants: false
      });
      return marked(this.md_text);
    }
  },
  components: {}
};
</script>