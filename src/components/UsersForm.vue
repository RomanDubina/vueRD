<template>
  <form @submit.prevent>
    <input-name @addName = "addNewUserName" :name="user.name"></input-name>
    <input-age @addAge = "addNewUserAge"></input-age>

    <hr>
    <sub-btn @click="addUser">ADD</sub-btn>
  </form>
</template>

<script>

import InputName from "@/components/InputName";
import InputAge from "@/components/InputAge";
import SubBtn from "@/components/UI/SubBtn";
export default {
  components:{
    InputName, InputAge, SubBtn
  },
  name: "UsersForm.vue",

  data(){
    return{
      user: {
        name: '',
        age: '',
      }
    }
  },
  methods: {
    addNewUserName(name){
      this.user.name = name;
    },
    addNewUserAge(age){
      this.user.age = age;
    },
    addUser(){
      console.log('addUser')
      this.user.id = Date.now();
      this.$emit('addNewUser', this.user)
      this.user = {
        name: '',
        age: ''
      }
    }


  }
}


</script>

<style scoped>

</style>