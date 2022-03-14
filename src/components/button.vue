<template>
  <button class="my-button"><slot></slot></button>
</template>

<script>
export default {
  props:{
    type:{
      type:String
    },
    size:{
      type:String
    },
    round:{
      type:Boolean
    },
    circle:{
      type:Boolean
    }
  }

}
</script>

<style>

</style>