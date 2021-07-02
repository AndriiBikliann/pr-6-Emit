<template>
   <div>
      <div>
         Гравець 1
      </div>
      <div>
         <label>
            Цифра
            <input type="number" v-model.number="user1Number">
         </label>
      </div>
      <div>
         <button @click="checkNumber1">Зробити хід</button>
      </div>
   </div>
</template>
<script>
   export default {
      name: "Player1",
      data() {
         return {
            user1Number: null
         }
      },
      methods: {
         checkNumber1() {
            this.$emit('userAnswer1', this.user1Number)
         }
      },
   }
</script>
<style lang="scss" scoped>
</style>