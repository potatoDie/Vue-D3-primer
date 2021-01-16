<template>
  Bookkeeping {{ n }} x {{ x }} <br />
  n: <input v-model.number="n" type="number" /> <br />
  x: <input v-model.number="x" type="number" /> <br />
  <Draw :n="n" :x="x" />
</template>

<script>
import Draw from "./Draw.vue";

export default {
  components: { Draw },
  data() {
    return {
      x: 8,
      n: 5,
    };
  },
};
</script>