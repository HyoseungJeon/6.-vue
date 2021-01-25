<template>
    <div>
        <input type="text" v-model="inputValue"/>
        <div>{{inputValue}} </div>
    </div>
</template>

<script>
export default {
    name:"ModelBind",
    data:function(){
        return{
            inputValue : ''
        }
    },
}
</script>

<style>

</style>