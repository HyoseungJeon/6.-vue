<template>
<div>
  <!-- <for-directive/> -->
  <!-- <if-directive/> -->
  <model-bind/>
</div>
</template>

<script>
// import DataFlowParent from './components/DataFlowParent.vue'
// import MyComponent from './components/MyComponent.vue'
// import ForDirective from './components/ForDirective.vue'
// import IfDirective from './components/IfDirective.vue'
import ModelBind from './components/ModelBind.vue'

export default {
  name: 'App',
  components: {
    // MyComponent,
    // DataFlowParent,
    // ForDirective,
    // IfDirective,
    ModelBind,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
