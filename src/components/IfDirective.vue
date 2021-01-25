<template>
  <div>
      <div v-if=isZero>This is 0</div>
      <div v-else-if=isZeroToTen>between 0 to 10</div>
      <div v-else>over 10</div>
  <button type="button" @click="onClickButton">
      {{clickCount}}
  </button>
  <div>oldValue : {{oldValue}} newValue : {{newValue}} results : {{results}}</div>
  </div>

</template>

<script>
export default {
    name:"IfDirective",
    data:function(){
        return {
            clickCount:0,
            oldValue: 0,
            newValue: 0,
            results: 'N',
        }
    },
    methods:{
        onClickButton: function(){
            this.clickCount++;
        }
    },
    computed:{
        isZero: function(){
            return (this.clickCount===0);
        },
        isZeroToTen: function(){
            return (this.clickCount > 0 && this.clickCount <=10);
        },
    },
    watch:{
        clickCount:function(newValue, oldValue){
            this.newValue = newValue
            this.oldValue = oldValue

            let result = "";
            if(this.isZero){
                result = "This is 0"
            } else if(this.isZeroToTen){
                result = "between 0 to 10"
            }
            else{
                result = "over 10"
            }
            this.results = result
        }
    }
}
</script>

<style>

</style>