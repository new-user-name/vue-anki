<!--6, if-else toggle -->
<template>
  <h1 v-if='awesome'>The Vue is awesome</h1>
  <h1 v-else>Oh no</h1>
  <button @click="toggle">Toggle</button>
</template>

<script>
export default{
  data(){
    return {
      awesome: true
    }
  },
  methods: {
    toggle(){
      this.awesome = !this.awesome
    }
  }
}
</script>
