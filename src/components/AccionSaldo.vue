<template>
  <!-- this.$emit('accion') es una alternativa para activar la funcionalidad, pero no
    es la más recomendable-->
  <button @click="accion" :disabled="desactivar">{{ texto }}</button>
</template>

<script>
export default {
  props: {
    texto: String,
    desactivar: {
        type: Boolean,
        default: false
    }
  },
  methods: {
    accion() {
      this.$emit("accion");
    },
  },
};
</script>

<style>
</style>