<template>
  <div id="target-switch-source">
    <h5>This is the content source. The portal is defined below.</h5>
    <portal :to="target">
      This Content was defined on the left,<br />
      and transferred to this target on the right.<br />
      Timestamp updates on each switch:<br />
      {{ getTimeStamp() }}
    </portal>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    target: { type: String },
  },
  methods: {
    getTimeStamp() {
      const date = new Date()
      return date.toUTCString()
    },
  },
})
</script>

<style></style>
