<template>
    <div>
       <SocNetlike
       v-for="id in array"
       :key = "id"
       :title = "id.title"
       />
       
       <div>
           <input type="text" v-model="userMessage" placeholder="Введіть повідомлення">
           <button @click="onSend">Відправити</button>
       </div> 

    </div>
</template>

<script>
import SocNetlike from './SocNetlike.vue' 
    export  default {
        name: "SocNet",
        components: {
            SocNetlike
        },
        props: {
            array: {
                type: Array,
                default: ()=>[]
            }
        },
        data () {
            return {
                userMessage: null,
            }
        },
        methods: {
            onSend(){
                //this.messageArray.push({title:this.userMessage});
                this.$emit('push',{
                    id:this.counter++,
                    title:this.userMessage
                })
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>