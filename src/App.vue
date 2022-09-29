<template>
  <AppThirteen @response = "msg => childMessage = msg"/>
  <p>Message from child {{childMessage}}</p>
</template>

<script>
import AppThirteen from "@/AppThirteen";

export default {
  components: {AppThirteen},
  data(){
    return {
      childMessage: 'No child message yet'
    }
  }
}
</script>
