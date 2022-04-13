<template>
    <div class="container">
        <div class="row">
            <div class="col">
                <p class="h3 fw-bold text-success" >User List</p>
                <p class="fst-italic">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, est et. Facere, nobis! Minus blanditiis eligendi, provident natus assumenda officiis quis ea, nobis repellendus omnis et sit iure quaerat quibusdam.</p>
            </div>
            <div v-if = 'loading'>
                <spinner/>
            </div>
            <div v-if = '!loading && users.length > 0' class="row">
                <div class='col'>
                    <table class='table table-hover text-center table-striped'>
                        <thead class='bg-success text-white'>
                            <tr>
                                <th>Serial Number</th>
                                <th>Name</th>
                                <th>Email</th>
                                <th>Company</th>
                                <th>Website</th>
                                <th>Location</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr v-for='user in users' :key='user.id'>
                                <td>{{user.id}}</td>
                                <td>{{user.name}}</td>
                                <td>{{user.email}}</td>
                                <td>{{user.company.name}}</td>
                                <td>{{user.website}}</td>
                                <td>{{user.address.city}}</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { UserService } from '@/services/UserService'
import Spinner from './Spinner.vue'

export default {
  components: { Spinner },
  name: 'UserList',
  data: function () {
    return {
      loading: false,
      users: [], // UserService.getAllUsers()
      errorMessage: null
    }
  },
  created: async function () {
    try {
      this.loading = true
      const response = await UserService.getAllUsers()
      this.loading = false
      this.users = response.data
    } catch (error) {
      this.loading = false
      this.errorMessage = error
    }
  }
}
</script>

<style scoped>
div.container {
    margin-bottom: 2em;
}
</style>
