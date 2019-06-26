<template>
  <div class="editor">
    <textarea v-model="path" cols="50" rows="30"></textarea>
    <svg>
      <path :d="path"/>
    </svg>
  </div>
</template>

<script>
import Path from "../assets/Path";

export default {
  name: "Editor",
  data() {
    return {
      pa: '',
    }
  },
  computed: {
    path: {
      get() {
        return this.pa;
      },
      set(newValue) {
        this.pa = newValue;
      }
    }
  },
  created() {
    this.pa = Path;
  }
};
</script>

<style>
svg {
  height: 600px;
  width: 800px;
}

path {
  fill: transparent;
  stroke-width: 4px;
  stroke:#157fc4;
}
</style>
