<template>
  <div id="child1" class="component">
    
    <h2>Child 1 Component</h2>
    <span>{{message}}</span>
    
  </div>
</template>

<script>
import {EventBus} from '../main.js'

export default {
  props: ['message'],
  created(){
    EventBus.$on('messageUpdate',(newMessage) => {
        this.message = newMessage
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#child1 {
  background-color: lightseagreen;
  
}
</style>
