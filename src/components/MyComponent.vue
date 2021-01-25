<template>
  <div>
      <div>Default Component</div>
      
      <div>인사 : {{greeting}}</div>
      <div>이름 : {{name}}</div>

  <div>
      <button type="button" v-on:click="onClickButton">
          {{buttonName}}
      </button>
  </div>

  <data-flow-parent/>
  </div>

</template>

<script>
export default {
    name:'my-component',
    props:[
        'greeting', 'name'
    ],
    data:function(){
        return {
            buttonName:'before-changed'
        }
    },
    methods:{
        onClickButton: function(){
            this.buttonName = 'after-changed';    
        }
    }
}
</script>

<style>

</style>