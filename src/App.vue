<template>
<div class="mesBox">
  <div class="mesList">
    <!--div v-if="submitTextArray && submitTextArray.length"-->
    <p v-for="item in submitTextArray" v-bind:key="item.mesDateTime">
      {{ item.mesDateTime }} <br> {{ item.mes }} <br><br>
    </p>
    <br><br>
    <!--/div-->
  </div>
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
      submitTextArray: []
    }
  },
  methods: {
    submitClick () {
      this.$refs.submitText.focus();
      
      if (this.$refs.submitText.value === '') return

      const now = new Date()    
      const formatter = new Intl.DateTimeFormat("ru", {
        year: "numeric",
        month: "long",
        day: "numeric",
        hour: "numeric",
        minute: "numeric",
        second: "numeric"
      })  
      this.submitTextArray.push({mesDateTime: formatter.format(now), mes: this.$refs.submitText.value})
       console.log(this.submitTextArray)
      this.$refs.submitText.value = ''
    }
  }
}
</script>

<style>
html, body, #app, .mesBox {
  padding: 0;
  margin: 0;
  width: 100%;
  height: 100%;
}

  input {
    width: 50%;
    border-radius: 8px;
  }
  .mesList{
    border: 2px solid lightgray;
    overflow: hidden auto;
    width: 50%;
    height: 80%;
    border-radius: 8px;
  }
</style>
