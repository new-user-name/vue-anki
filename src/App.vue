<!--5, two-way binding with full and short syntax -->
<template>
  <input v-bind:value="msg" v-on:input="onInput" placeholder="Enter text">
  <p>{{msg}}</p>
  <input :value="msg" @input="onInput" placeholder="Enter text">
  <p>{{msg}}</p>
  <input v-model="msg" placeholder="Enter text">
  <p>{{msg}}</p>
</template>

<script>
export default{
  data(){
    return {
      msg: ""
    }
  },
  methods: {
    onInput(e){
      this.msg = e.target.value
    }
  }
}
</script>
