<template>
<div>
    <textarea readonly rows="30" v-model="review"></textarea>
    <br>
    <label>Введите сообщение:</label>
    <br>
    <input  @keyup.enter="submitClick" ref="submitText">
</div>
</template>

<script>
export default {
/* eslint-disable */
  name: 'App',
  data () {
    return {
      review: ''
    }
  },
  methods: {
    submitClick () {
      this.$refs.submitText.focus();
      
      if (this.$refs.submitText.value === '') return

      let now = new Date()    
      let formatter = new Intl.DateTimeFormat("ru", {
        year: "numeric",
        month: "long",
        day: "numeric",
        hour: "numeric",
        minute: "numeric",
        second: "numeric"
      })  
      const formatDateTime = formatter.format(now) + '\n';
      this.review += formatDateTime + this.$refs.submitText.value + '\n\n'
      this.$refs.submitText.value = null
    }
  }
}
</script>

<style>
html, body, #app {
  padding: 0;
  margin: 0;
  width: 100%;
  height: 100%;
}
  textarea, input {
    width: 50%;
    border-radius: 8px;
  }
</style>
