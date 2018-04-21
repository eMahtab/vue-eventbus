<template>
  <div id="child2" class="component">
    
    <h2>Child 2 Component</h2>
    <span>{{message}}</span>
    <br/><br/>
    <button @click="changeMessage">Change Message</button>
  </div>
</template>

<script>
import {EventBus} from '../main.js'

export default {
  props:['message'],
  methods:{
    changeMessage(){
      this.message = "A day of worry is more exhausting than a week of work - John Lubbock"
      EventBus.updateMessage(this.message)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#child2 {
  background-color: lightcoral;
}

</style>
