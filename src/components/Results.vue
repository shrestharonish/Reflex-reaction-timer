<template>
  <p>Reaction Time: {{ score }}</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 250) {
      this.rank = "Ninja Reflex";
    } else if (this.score < 400) {
      this.rank = "Rapid Reflex";
    } else {
      this.rank = "Turtle pace ....!";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.6rem;
  color: #0faf87;
  font-weight: bold;
}
button {
  background: #0faf87;
  color: white;
  border: none;
  padding: 8px 16px;
  border-radius: 4px;
  font-size: 16px;
  letter-spacing: 1px;
  cursor: pointer;
  margin: 10px;
}
button[disabled] {
  opacity: 0.2;
  cursor: not-allowed;
}
</style>
