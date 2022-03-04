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
  <div class="inpMes">
    <input  @keyup.enter="submitClick" ref="submitText">
    <i class="icon-smile">😊</i>
    <i class="icon-attach">
      <img src="https://www.pngrepo.com/png/7884/180/attachment.png" intrinsicsize="512 x 512" width="20" height="20">
    </i>
    </div>
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
       // console.log(this.submitTextArray)
      this.$refs.submitText.value = ''
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

  input {
    width: 90%;
    border-radius: 8px;
    background-color: aquamarine;
    font-size: large;
  }
  .mesBox {
    border: 2px solid;
    width: 50%;
    height: 95%;
    border-radius: 8px;
    background-color: lightgrey;
  }
  .mesList{
    overflow: hidden auto;
    padding: 0;
    margin: 0;
    width: 100%;
    height: 90%;
  }
  .icon-attach {
    margin-left: 10px;
  }
</style>
