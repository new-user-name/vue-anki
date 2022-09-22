<!--2, exemplary simple binding-->
<template>
  <h1>The message is {{ message }}</h1>
  <h1>The counter is {{ counter + 1 }}</h1>
</template>

<script>
export default {
  data() {
    return {
      message: "Hippopotamus",
      counter: 1
    }
  }
}
</script>
