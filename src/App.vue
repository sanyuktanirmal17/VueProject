<template>

<div id="app">
    <nav class="navbar navbar-expand navbar-dark bg-dark">
      <!-- <router-link to="/" class="navbar-brand">Portal</router-link> -->
      <div class="navbar-nav mr-auto">
        <li class="nav-item">
          <!-- <router-link to="/add" class="nav-link">Form </router-link> -->
        </li>
      </div>
    </nav>
  <!-- //<div id="app"> -->
    <!-- <Header />  -->

<b-container class="bv-example-row">
  <b-row>
    <b-col sm ="6" offset= "3"></b-col>
     <Box />
     <Operation />

  </b-row>
</b-container>
</div>
</template>

<script>
// import Header from './components/Header.vue'
import Box from './components/Box.vue'
import Operation from './components/Operation.vue'
// import axios from 'axios'
export default {
  name: 'App',
  components: {
    // Header,
    Box,
    Operation
  },

data () {
  return {
    results: [],
     form: {
                firstname: '',
                lastname: '',
                email: '',
                address: ''
               
            }
  }
},
//   mounted: function()
//  {
//   fetch('http://localhost:3000/sampletable', 
//   {
//     method: 'get'
//   })
//   .then((response) => {
//     //  console.log(response.json())
//     return response.json()
//   })
//   .then ((jsonData) => {
  
//     this.results = jsonData
//     console.log(this.results[0].firstname)
//   })
//   },

// addData(){
//   fetch('http://localhost:3000/sampletable', 
//   {
//     method: 'post'
//   })
//   .then((response) => {
//     //  console.log(response.json())
//     return response.json()
//   })
//   .then ((jsonData) => {
  
//     this.results = jsonData
//     console.log(this.results[0].firstname)
//   })
//   }


// methods: {
  // addData(){
  // axios
  // .post('http://localhost:3000/sampletable', this.form)
  // .then((response)=> console.log(response))
  // .catch((error) => console.log(error))
  // }
  // }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
