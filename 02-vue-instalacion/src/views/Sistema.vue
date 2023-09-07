<template>
  <div>
    <h2>Sistema</h2>
    <h3>Lista:</h3>
    <ul>
      <li v-for="item in lista" :key="item">
        {{ item }}
      </li>
    </ul>

    <Details @agregar="agregar" />
    <hr />
  </div>
</template>

<script>
import Details from "./Details.vue";

export default {
  components: {
    Details,
  },
  data() {
    return {
      lista: [0],
    };
  },
  methods: {
    agregar(num) {
      this.lista.push(num);
    },
  },
};
</script>

<style></style>
