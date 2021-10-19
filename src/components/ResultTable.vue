<template>
    <div>
        <table class="table">
            <thead>
            <tr>
                <th scope="col">#</th>
                <th scope="col">Name</th>
                <th scope="col">Age</th>
            </tr>
            </thead>
            <tbody>
            <tr v-for="user in users">
                <th>{{user.id}}</th>
                <td>{{user.name}}</td>
                <td>{{user.age}}</td>

            </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
    export default {
        props: {
            users: {
                type: Array,
                required: true
            }
        }
    }
</script>

<style scoped>

</style>