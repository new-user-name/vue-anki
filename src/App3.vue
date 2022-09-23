<!--3, two strings in headers, blue and red, without counters, reverse and join-->
<template>
  <h1 :class="blue">{{ firstName.split('').reverse().join('')}}</h1>
  <h2 v-bind:class="red">{{ secondName + 1 }}</h2>
</template>

<script>
export default {
  data() {
    return {
      firstName: 'Hippo',
      secondName: 122,
      blue: 'blue',
      red: 'red'
    }
  }
}
</script>

<style>
  .red {
    color: red
  }
  .blue {
    color: blue
  }
</style>
