<template>
  <AppFourteen>Message {{message}}</AppFourteen>
</template>

<script>
import AppFourteen from "@/AppFourteen"

export default {
  components : {
    AppFourteen
  },
  data() {
    return {
      message: 'Hippos!'
    }
  }
}
</script>
