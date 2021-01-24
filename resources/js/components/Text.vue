<template>
  <h1 class="text-class" :style="textMergedStyles">
    Componente text
  </h1>
</template>

<script>
export default {
  props:{
    textStyles:{
      type: String,
      default: "red"
    },
    fontStyle:{
      type: String,
      default: "italic"
    },
    

  },

  computed:{
    textMergedStyles(){
      return {
        '--text-color' : this.textStyles,
        '--font-style' : this.fontStyle
      }
    }
  }





}
</script>

<style lang="scss">
  .text-class{
    color:var(--text-color);
    font-style:var(--font-style);
  }
</style>