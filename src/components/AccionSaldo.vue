<template>
    <!-- this.$emit('accion') es una alternativa para activar la funcionalidad, pero no
    es la más recomendable-->
  <button @click="this.$emit('accion')">{{ texto }}</button>
</template>

<script>
export default {
  props: {
    texto: String,
  },
};
</script>

<style>
</style>