<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <Button text="Love ❤️" @click="pushHeart"/>
    <p>
      <span v-for="(love, i) in loveArray" :key="i">{{ love }}</span>
    </p>
  </div>
</template>

<script>
import Button from "./Button";

export default {
  components: {
    Button
  },
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to your first Sandbox",
      loveArray: []
    };
  },
  methods: {
    pushHeart() {
      this.loveArray.push("❤️");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
