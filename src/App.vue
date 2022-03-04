<template>
<div class="mesBox">
  <header>
    <svg viewBox="0 0 212 212" class="Prof"><path fill="#DFE5E7" class="background" d="M106.251.5C164.653.5 212 47.846 212 106.25S164.653 212 106.25 212C47.846 212 .5 164.654.5 106.25S47.846.5 106.251.5z"></path><g fill="#FFF"><path class="primary" d="M173.561 171.615a62.767 62.767 0 0 0-2.065-2.955 67.7 67.7 0 0 0-2.608-3.299 70.112 70.112 0 0 0-3.184-3.527 71.097 71.097 0 0 0-5.924-5.47 72.458 72.458 0 0 0-10.204-7.026 75.2 75.2 0 0 0-5.98-3.055c-.062-.028-.118-.059-.18-.087-9.792-4.44-22.106-7.529-37.416-7.529s-27.624 3.089-37.416 7.529c-.338.153-.653.318-.985.474a75.37 75.37 0 0 0-6.229 3.298 72.589 72.589 0 0 0-9.15 6.395 71.243 71.243 0 0 0-5.924 5.47 70.064 70.064 0 0 0-3.184 3.527 67.142 67.142 0 0 0-2.609 3.299 63.292 63.292 0 0 0-2.065 2.955 56.33 56.33 0 0 0-1.447 2.324c-.033.056-.073.119-.104.174a47.92 47.92 0 0 0-1.07 1.926c-.559 1.068-.818 1.678-.818 1.678v.398c18.285 17.927 43.322 28.985 70.945 28.985 27.678 0 52.761-11.103 71.055-29.095v-.289s-.619-1.45-1.992-3.778a58.346 58.346 0 0 0-1.446-2.322zM106.002 125.5c2.645 0 5.212-.253 7.68-.737a38.272 38.272 0 0 0 3.624-.896 37.124 37.124 0 0 0 5.12-1.958 36.307 36.307 0 0 0 6.15-3.67 35.923 35.923 0 0 0 9.489-10.48 36.558 36.558 0 0 0 2.422-4.84 37.051 37.051 0 0 0 1.716-5.25c.299-1.208.542-2.443.725-3.701.275-1.887.417-3.827.417-5.811s-.142-3.925-.417-5.811a38.734 38.734 0 0 0-1.215-5.494 36.68 36.68 0 0 0-3.648-8.298 35.923 35.923 0 0 0-9.489-10.48 36.347 36.347 0 0 0-6.15-3.67 37.124 37.124 0 0 0-5.12-1.958 37.67 37.67 0 0 0-3.624-.896 39.875 39.875 0 0 0-7.68-.737c-21.162 0-37.345 16.183-37.345 37.345 0 21.159 16.183 37.342 37.345 37.342z"></path></g></svg>
    <span class="contName">Олег Крылов</span>
    <svg viewBox="0 0 24 24" class="Lupa"><path fill="currentColor" d="M15.9 14.3H15l-.3-.3c1-1.1 1.6-2.7 1.6-4.3 0-3.7-3-6.7-6.7-6.7S3 6 3 9.7s3 6.7 6.7 6.7c1.6 0 3.2-.6 4.3-1.6l.3.3v.8l5.1 5.1 1.5-1.5-5-5.2zm-6.2 0c-2.6 0-4.6-2.1-4.6-4.6s2.1-4.6 4.6-4.6 4.6 2.1 4.6 4.6-2 4.6-4.6 4.6z"></path></svg>
    <svg viewBox="0 0 24 24" class="Menu"><path fill="currentColor" d="M12 7a2 2 0 1 0-.001-4.001A2 2 0 0 0 12 7zm0 2a2 2 0 1 0-.001 3.999A2 2 0 0 0 12 9zm0 6a2 2 0 1 0-.001 3.999A2 2 0 0 0 12 15z"></path></svg>
  </header>
  <div class="mesList">
    <div v-for="item in submitTextArray" v-bind:key="item.mesDateTime">
      <div class="blokMes">
        <div class="textMes">
          {{ item.mes }}
        </div>
        <div class="timeMes">
          {{ item.mesDateTime }}
          <svg viewBox="0 0 16 15" width="16" height="15" class=""><path fill="currentColor" d="m15.01 3.316-.478-.372a.365.365 0 0 0-.51.063L8.666 9.879a.32.32 0 0 1-.484.033l-.358-.325a.319.319 0 0 0-.484.032l-.378.483a.418.418 0 0 0 .036.541l1.32 1.266c.143.14.361.125.484-.033l6.272-8.048a.366.366 0 0 0-.064-.512zm-4.1 0-.478-.372a.365.365 0 0 0-.51.063L4.566 9.879a.32.32 0 0 1-.484.033L1.891 7.769a.366.366 0 0 0-.515.006l-.423.433a.364.364 0 0 0 .006.514l3.258 3.185c.143.14.361.125.484-.033l6.272-8.048a.365.365 0 0 0-.063-.51z"></path></svg>
        </div>
      </div>
    </div>
  </div>
  <footer>
  <div class="footBlock">
    <div class="inpMes">
      <svg class="smiley"><path fill="currentColor" d="M9.153 11.603c.795 0 1.439-.879 1.439-1.962s-.644-1.962-1.439-1.962-1.439.879-1.439 1.962.644 1.962 1.439 1.962zm-3.204 1.362c-.026-.307-.131 5.218 6.063 5.551 6.066-.25 6.066-5.551 6.066-5.551-6.078 1.416-12.129 0-12.129 0zm11.363 1.108s-.669 1.959-5.051 1.959c-3.505 0-5.388-1.164-5.607-1.959 0 0 5.912 1.055 10.658 0zM11.804 1.011C5.609 1.011.978 6.033.978 12.228s4.826 10.761 11.021 10.761S23.02 18.423 23.02 12.228c.001-6.195-5.021-11.217-11.216-11.217zM12 21.354c-5.273 0-9.381-3.886-9.381-9.159s3.942-9.548 9.215-9.548 9.548 4.275 9.548 9.548c-.001 5.272-4.109 9.159-9.382 9.159zm3.108-9.751c.795 0 1.439-.879 1.439-1.962s-.644-1.962-1.439-1.962-1.439.879-1.439 1.962.644 1.962 1.439 1.962z"></path></svg>
      <input @keyup.enter="submitClick" ref="submitText">
      <svg class="clip"><path fill="currentColor" d="M1.816 15.556v.002c0 1.502.584 2.912 1.646 3.972s2.472 1.647 3.974 1.647a5.58 5.58 0 0 0 3.972-1.645l9.547-9.548c.769-.768 1.147-1.767 1.058-2.817-.079-.968-.548-1.927-1.319-2.698-1.594-1.592-4.068-1.711-5.517-.262l-7.916 7.915c-.881.881-.792 2.25.214 3.261.959.958 2.423 1.053 3.263.215l5.511-5.512c.28-.28.267-.722.053-.936l-.244-.244c-.191-.191-.567-.349-.957.04l-5.506 5.506c-.18.18-.635.127-.976-.214-.098-.097-.576-.613-.213-.973l7.915-7.917c.818-.817 2.267-.699 3.23.262.5.501.802 1.1.849 1.685.051.573-.156 1.111-.589 1.543l-9.547 9.549a3.97 3.97 0 0 1-2.829 1.171 3.975 3.975 0 0 1-2.83-1.173 3.973 3.973 0 0 1-1.172-2.828c0-1.071.415-2.076 1.172-2.83l7.209-7.211c.157-.157.264-.579.028-.814L11.5 4.36a.572.572 0 0 0-.834.018l-7.205 7.207a5.577 5.577 0 0 0-1.645 3.971z"></path></svg>
    </div>
    <svg viewBox="-8 -8 40 40" class="mic"><path fill="currentColor" d="M11.999 14.942c2.001 0 3.531-1.53 3.531-3.531V4.35c0-2.001-1.53-3.531-3.531-3.531S8.469 2.35 8.469 4.35v7.061c0 2.001 1.53 3.531 3.53 3.531zm6.238-3.53c0 3.531-2.942 6.002-6.237 6.002s-6.237-2.471-6.237-6.002H3.761c0 4.001 3.178 7.297 7.061 7.885v3.884h2.354v-3.884c3.884-.588 7.061-3.884 7.061-7.885h-2z"></path></svg>
  </div>
  </footer>
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
        //year: "numeric",
        //month: "long",
        //day: "numeric",
        hour: "numeric",
        minute: "numeric",
        //second: "numeric"
      })  
      this.submitTextArray.push({mesDateTime: formatter.format(now), mes: this.$refs.submitText.value})
       // console.log(this.submitTextArray)
      this.$refs.submitText.value = ''
    }
  }
}
</script>

<style>
:root {
  --primary: #3b4a54;
  --app-background: #eae6df;
  --app-background-deeper: #d1d7db;
}
  * {
    box-sizing: border-box;
    padding: 0px;
    margin: 0px;
  }
  #app, body, html {
    width: 100%;
    height: 100%;
    overflow: hidden;
  }
    .mesBox {
    margin: 5px;
    border: 2px solid;
    width: 40%;
    height: calc(100vh - 10px);
    border-radius: 10px;
    font-Family: Segoe UI,Helvetica Neue,Helvetica,Lucida Grande,Arial,Ubuntu,Cantarell,Fira Sans,sans-serif;
    color: var(--primary);
    user-Select: none;
    text-Rendering: optimizeLegibility;
    font-Feature-Settings: "kern";
    background-Color: var(--app-background);
    background-Image: linear-gradient(180deg,var(--app-background),var(--app-background-deeper));
  }

  header {
    display: flex;
    width: 100%;
    height: 70px;
    background-color:seagreen; 
    color: var(--app-background);   
  }
  .Prof {
    width: 60px;
    height: 60px;
    margin: 5px;    
  }
  .contName {
    margin-top: 25px;
    width: 100%;
  }
  .Lupa, .Menu {
    width: 40px;
    height: 40px;
    margin-right: 5px;    
    margin-top: 20px;
  }
  
  .mesList{
    background-color: #efeae2;
    background-Image: url(./assets/background-whatsapp.png);
    overflow: hidden auto;
    width: 100%;
    height: calc(100vh - 140px);
  }
  .blokMes {
    background-color:lightgreen;
    margin-left: 100px;
    margin-bottom: 10px;
    width: calc(40vw - 140px);
    overflow-wrap: break-word;
    border-radius: 8px;
  }
  .textMes {
    margin: 8px;
  }
  .timeMes {
    text-align: right;
    margin-right: 8px;
    font-size: small;
    padding-bottom: 5px;
  }

  footer {
    height: 60px;
    width: 100%;
  }
  .footBlock { 
    display: flex;
    height: 40px;
    margin: 8px;
  }
  .inpMes{
    display: flex;
    background-color:white;
    border-radius: 20px;
    width: calc(40vw - 70px);
    height: 40px;
  }
  input {
    width: 100%;
    border: none;
    outline: none;    
    font-size: large;
    font-family: Segoe UI,Helvetica Neue,Helvetica,Lucida Grande,Arial,Ubuntu,Cantarell,Fira Sans,sans-serif;
  }
  .clip, .smiley {
    width: 40px;
    margin: 8px;
  }
  .mic {
    width: 40px;
    margin-left: 8px;
    color: lightgrey;
    background-color:seagreen;    
    border-radius: 20px;
  }
</style>
