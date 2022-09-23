<!--4, two simple counters with full and short syntax -->
<template>
  <div>
    <button v-on:click="increase">Counter {{ count }}</button>
  </div>
  <div>
    <button @click="increase">Counter {{ count }}</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increase() {
      this.count++
    }
  }
}
</script>


