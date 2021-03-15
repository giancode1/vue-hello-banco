<template>
  <h1>Mi banco 2.0 por Gian Culcay</h1>
  <h2>{{texto}}</h2>
</template>

<script>
export default {
    name:'Titulo',
    props: {
        texto: String
    }
}
</script>

<style scoped> /* scoped: estilos solo para ese componente */
    h2{
    color: royalblue;
    }
</style>