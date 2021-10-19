<template>

        <label>
            <p>Age: </p>
            <input type="number" v-model="userAge" @change="addUserAge">
        </label>

</template>

<script>
    export default {

        data(){
            return{
                userAge: ''
            }
        },
      methods: {
        addUserAge(){
          this.$emit('addAge', this.userAge)

        }
      }
    }
</script>

<style scoped>

</style>