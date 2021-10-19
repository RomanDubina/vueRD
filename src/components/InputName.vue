<template>

        <label>
            <p>Name:</p>
            <input type="text" v-model="userName" @change="addUserName">
        </label>

</template>

<script>
export default {
        props: {

        },
        data(){
            return{
              userName: ''
            }
        },
      methods: {
          addUserName(){
            this.$emit('addName', this.userName)

          }
      }
    }
</script>

<style scoped>

</style>