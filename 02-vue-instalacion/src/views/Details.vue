<template>
  <form @submit.prevent="onClick">
    <input type="number" step="1" v-model="item" />
    <input type="submit" value="Agregar" />
  </form>
</template>

<script>
export default {
  methods: {
    onClick() {
      if (this.item != 0) {
        this.$emit("agregar", this.item);
      } else {
        alert("El numero no puede ser 0!")
      }
      this.item = 0;
    },
  },
  data() {
    return {
      item: 0,
    };
  },
};
</script>

<style></style>
