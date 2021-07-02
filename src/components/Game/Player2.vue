<template>
   <div>
      <div>
         Гравець 2
      </div>
      <div>
         <label>
            Цифра
            <input type="number" v-model.number="user2Number">
         </label>
      </div>
      <div>
         <button @click="checkNumber2">Зробити хід</button>
      </div>
   </div>
</template>
<script>
   export default {
      name: "Player2",
      data() {
         return {
            user2Number: null
         }
      },
      methods: {
         checkNumber2() {
            this.$emit('userAnswer2', this.user2Number)
         }
      },
   }
</script>
<style lang="scss" scoped>
</style>