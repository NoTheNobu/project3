<template>
  <div id="app">
    <div class="fortune-container">
      <h1>Welcome to Exoldran the Great</h1>
      <p>Press the button below to unveil your fortune that I bestow upon you!</p>
      <button @click="revealFortune">Reveal My Fortune</button>
      <p v-if="fortune" class="fortune-display">{{ fortune }}</p>
    </div>
    <h2>About Exoldran</h2>
    <p>Exoldran offers insights and surprises for your daily life. Click the button and enjoy your fortune!</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fortunes: [
        "Today, you will find a coupon for your favorite restaurant.",
        "You can expect your pet to learn a new trick today.",
        "You might lose a match in a competitive game, which in turn will cause your rank to go down.",
        "You may make a new friend in public today; it will honestly depend on your social skills.",
        "Be careful around candy that is solid; the fortune says it's a rock.",
        "Momentary distractions will lead you to not finish your work today.",
        "You will find a new perspective in time, but always stay true to what you think is right.",
        "What a boring day planned for you.",
        "A kind action could lead to some serious reward in the future for you.",
        "There is paper in the pizza."
      ],
      fortune: ''
    };
  },
  methods: {
    revealFortune() {
      const index = Math.floor(Math.random() * this.fortunes.length);
      this.fortune = this.fortunes[index];
    }
  }
};
</script>

<style src="./style.css"></style>
