<template>
  <svg width="400" height="300"></svg>
</template>

<script>
import * as d3 from "d3";

export default {
  props: { n: Number, x: Number },
  mounted() {
    this.init();
  },
  watch: {
    n() {
      this.init();
    },
    x() {
      this.init();
    },
  },
  methods: {
    init() {
      const data = Array(this.n).fill(this.x);
      const svg = d3.select("svg");
      const squares = svg.selectAll("rect").data(data);
      const enterSquares = squares.enter().append("rect");

      squares.attr("x", (d, i) => i * 50 + 40).attr("width", (d) => d);

      enterSquares
        .attr("x", (d, i) => i * 50 + 40)
        .attr("y", 100)
        .attr("width", (d) => d)
        .attr("height", 25)
        .attr("fill", '#f00')

      squares.exit().remove();
    },
  },
};
</script>

<style scoped>
svg {
  background: #dddddd;
}
</style>