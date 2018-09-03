<template lang="pug">
  button(
    :style="{background: options.color, border: 0, color: 'white', padding: (options.size === 'big')? '20px': '10px'}"
    @click="broadcast('click')"
    @mouseover="broadcast('mouseover')"
    @mouseout="broadcast('mouseout')") {{ options.text }}
</template>

<script lang="ts">
export default {
  props: {
    options: Object
  },
  methods: {
    broadcast(event) {
      this.$emit(`my-button-${event}`);
    }
  }
};
</script>
