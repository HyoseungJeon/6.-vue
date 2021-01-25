<template>
  <div>
      <!-- 동적매핑 -->
      <!-- <data-flow-child :fromParent="1"/> -->

    <!-- 정적매핑 -->
      <!-- <data-flow-child : :fromParent="1"/> -->

      <data-flow-child
        :fromParent1="fromParent1"
        :fromParent2="fromParent2"

        v-bind="propsObj"

        :onClickButton="handleClickButton"

        @parent-event="handleClickButton"
      />
      <div>
          fromChild = {{fromChildButton}}
      </div>
  </div>
</template>

<script>
import DataFlowChild from './DataFlowChild.vue'
export default {
    components:{DataFlowChild},
    name :'DataFlowParent',
    data: function(){
        return{
            fromParent1: "1",
            fromParent2: "2",
            propsObj:{
                fromObjParent1: "Obj 1",
                fromObjParent2: "Obj 2",
            },
            fromChildButton: '',
        }
    },
    methods:{
        handleClickButton: function(data){
            this.fromChildButton = data
        }
    }
}
</script>

<style>

</style>