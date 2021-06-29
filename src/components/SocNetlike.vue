<template>
    <div>
       <span>{{title}}</span>
       <button @click="onLike">Like</button>
       <button @click="onDislike">Dislike</button>
       <span>Likes:</span>
       <span>{{likesCounter}}</span>
    </div>
</template>

<script>
    export default {
        name: 'SocNetlike',
        props: {
            title: {
                type: String,
                default: 'no message' 
            },
        },
        data() {
            return {
                likesCounter: 0,
            }
        },
        methods: {
            onLike() {
                this.likesCounter++
            },
            onDislike(){
                this.likesCounter--
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>
