<template>
<div>
<div>Default child</div>
  <div>
    FROM PARNENT1 -> {{fromParent1}}
  </div>
  <div>
    FROM PARNENT2 -> {{fromParent2}}
  </div>
  <div>
    FROM Obj PARNENT1 -> {{fromObjParent1}}
  </div>
  <div>
    FROM Obj PARNENT2 -> {{fromObjParent2}}
  </div>
  <button type="button" @click="onClickButton('from_child')">
      ChildButton
  </button>
  <button type="button" @click="onClickButton_event('from_child_event')">
      ChildButton_event
  </button>
  <div>Default child End</div>
</div>
</template>

<script>
export default {
    name:'DataFlowChild',
    props:{
        fromParent1: String,
        fromParent2: String,
        onClickButton: Function,
    },
    methods:{
        onClickButton_event: function(){
            this.$emit('parent-event','from_event_child')
        }
    }
}
</script>

<style>

</style>