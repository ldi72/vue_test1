<template>
<div>
    <textarea readonly rows="30" v-model="review"></textarea>
    <br>
    <label>Сообщение:</label>
    <br>
    <input id="submitText" v-model="submitText">
    <!--input type="submit" value="Отпарвить-->
    <br>
    <button v-on:click="submitClick">Отправить</button>
</div>
</template>

<script>
export default {
/* eslint-disable */
  name: 'App',
  data () {
    return {
      review: '',
      submitText: ''
    }
  },
  methods: {
    submitClick () {
      document.getElementById('submitText').focus()
            
      if (this.submitText === '') return

      var now = new Date()      
      const formatDateTime = ('0' + now.getDate().toString()).slice(-2) + '.' +
        ('0' + (now.getMonth() + 1).toString()).slice(-2) + '.' +
        now.getFullYear().toString() + ' ' +
        ('0' + now.getHours().toString()).slice(-2) + ':' +
        ('0' + now.getMinutes().toString()).slice(-2) + ':' +
        ('0' + now.getSeconds().toString()).slice(-2) + '\n'
      
      this.review += formatDateTime + this.submitText + '\n\n'
      this.submitText = ''
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
  }
</style>
