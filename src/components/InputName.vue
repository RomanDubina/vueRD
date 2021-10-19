<template>

        <label>
            <p>Name:</p>
            <input type="text" :value="name" @change="addUserName($event.target.value)">
        </label>

</template>

<script>
export default {
        props: {
          name:{
            type: String
          }
        },
      methods: {
          addUserName(e){
            this.$emit('addName', e)

          }
      }
    }
</script>

<style scoped>

</style>