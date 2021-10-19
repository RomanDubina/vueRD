<template>
    <div>
        <users-form @addNewUser="saveUser"></users-form>
      <hr>
        <result-table :users="users"></result-table>
    </div>
</template>

<script>

import UsersForm from "@/components/UsersForm";
import ResultTable from "@/components/ResultTable";


export default {
    components:{
     ResultTable, UsersForm
    },
    data: function () {
        return {
            users: [

            ]
        }
    },
  methods:{
  saveUser(user){
    this.users.push(user);
  }
  }
}
</script>

<style lang="scss">

</style>
