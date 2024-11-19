<template>
     <!-- Top Bar -->
     <nav class="navbar navbar-expand-lg navbar-light bg-light shadow-sm">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Admin Panel</a>
        <button
          class="btn btn-danger ms-auto"
          @click="logout"
        >
          Logout
        </button>
      </div>
    </nav>
    <div class="container mt-5">
        
      <h1 class="text-center">Registered Members</h1>
      <div v-if="loading" class="text-center my-4">
        <div class="spinner-border text-primary" role="status">
          <!-- <span class="sr-only">Loading...</span> -->
        </div>
      </div>
      <div v-else>
        <table class="table table-bordered table-striped">
          <thead class="table-primary">
            <tr>
              <th>#</th>
              <th>Surname</th>
              <th>First Name</th>
              <th>Other Names</th>
              <th>Email</th>
              <th>State</th>
              <th>Payment Status</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(member, index) in members" :key="index">
              <td>{{ index + 1 }}</td>
              <td>{{ member.surname }}</td>
              <td>{{ member.firstname }}</td>
              <td>{{ member.otherNames || 'N/A' }}</td>
              <td>{{ member.email }}</td>
              <td>{{ member.state }}</td>
              <td>
                <span
                  :class="[
                    'badge',
                    member.paymentStatus === 'Paid' ? 'bg-success' : 'bg-warning'
                  ]"
                >
                  {{ member.paymentStatus }}
                </span>
              </td>
            </tr>
            <tr v-if="members.length === 0">
              <td colspan="7" class="text-center">No members registered yet.</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </template>
  
  <script>
  import axios from "axios";
  
  export default {
    data() {
      return {
        members: [], // Holds the members' data
        loading: true, // Indicates loading state
      };
    },
    methods: {
      async fetchMembers() {
        axios({
        method: "get",
        url: process.env.VUE_APP_URL + '/api/bursconn/members',
      })
        .then((response) => {

          
       this.members = response.data

       console.log(this.members);

       this.loading = false
        })
        .catch((err) => {
          console.log(err)
        })
      },
    },
    mounted() {
      this.fetchMembers(); // Fetch members data when the component is mounted
    },
  };
  </script>
  
  <style scoped>
  h1 {
    margin-bottom: 20px;
  }
  .spinner-border {
    width: 3rem;
    height: 3rem;
  }
  </style>
  