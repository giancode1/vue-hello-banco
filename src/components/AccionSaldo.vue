<template>
  <!-- <button @click="this.$emit('accion')">{{texto}}</button> -->  <!-- no es recomendable asi -->
  <button @click="accion" :disabled='desactivar'>{{texto}}</button>

</template>

<script>
export default {
    props:{
        texto: String,
        //desactivar: Boolean //tambn funca vue es inteligente
        desactivar: {
            type: Boolean,
            default: false
        }
    },
    methods:{
        accion(){
            this.$emit('accion')
        }

    }
}
</script>

<style>

</style>