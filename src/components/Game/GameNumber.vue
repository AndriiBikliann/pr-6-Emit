<template>
  <div>
    <div class="wrapper">
      <div>Число</div>
      <div
        class="number1"
        :class="{
          right: right === true,
        }"
      >
        {{ number1 }}
      </div>
      <div :class="number2" 
      >{{ number2 }}</div>
      <div :class="number3">{{ number3 }}</div>
    </div>
    <div class="container">
      <div>
        <player-1 @userAnswer1="checkAnswer1" />
      </div>
      <div>
        <player-2 @userAnswer2="checkAnswer2"/>
      </div>
    </div>
  </div>
</template>
<script>
import Player1 from "./Player1";
import Player2 from "./Player2";
export default {
  name: "GameNumber",
  components: {
    Player1,
    Player2,
  },
  data() {
    return {
      number1: Math.floor(Math.random() * 9),
      number2: Math.floor(Math.random() * 9),
      number3: Math.floor(Math.random() * 9),
      randomArrayNumbers: [],
      right: false,
    };
  },
  methods: {
    checkAnswer1(value) {
      this.randomArrayNumbers.push(this.number1, this.number2, this.number3);
      if (this.randomArrayNumbers.some((item) => item === value))
        this.right = true;
    },
    checkAnswer2(value) {
      this.randomArrayNumbers.push(this.number1, this.number2, this.number3);
      if (this.randomArrayNumbers.some((item) => item === value))
        this.right = true;
    },
  },
};
</script>
<style lang="css" scoped>
.wrapper div {
  display: inline-block;
  margin: 20px;
  width: 30px;
  height: 30px;
  text-align: center;
  border-color: black;
}
.number1 {
  background-color: white;
}
.number2 {
  background-color: white;
}
.number3 {
  background-color: white;
}
.container div {
  display: inline-block;
  width: 170px;
  margin: 20px;
  border-color: black;
}
.right {
  background-color: red;
}
</style>