<!--6, if-else toggle -->
<template>
  <h1 v-if="fat">Hippos are fat</h1>
  <h1 v-else>Oh no</h1>
  <button @click="toggle">Toggle</button>
</template>

<script>
export default {
  data(){
    return {
      fat: true
    }
  },
  methods : {
    toggle(){
      this.fat = !this.fat
    }
  }
}
</script>
