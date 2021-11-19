<template>
  <!-- <h1> form </h1>
  <p>{{Form}}</p>  -->
 <form> 
   <label> Id :  </label>
    <input type="text" placeholder="enter address" v-model="form.id" />
    <br /> <br />

   <label> First Name : </label>
    <input type="text" placeholder="enter first name" v-model="form.firstname" />
    <br /> <br />

    <label>Last Name : </label>
    <input type="text" placeholder="enter last name" v-model="form.lastname" />
    <br /> <br />

    <label> Email : </label>
    <input type="text" placeholder="enter email" v-model="form.email" />
    <br /> <br />

    <label> Address : </label>
    <input type="text" placeholder="enter address" v-model="form.address" />
    <br /> <br />

    <button v-on:click="addData" type="button">Add</button><br />
    <button v-on:click="getData" type="button">Get</button><br />
    <button v-on:click="updateData" type="button">Update</button><br />
    <button v-on:click="deleteData" type="button">Delete</button><br />

</form>
</template>

<script>
 import axios from 'axios'
 export default {
    name: "Home",
    
    data() {
        return {
            form: {
                firstname: '',
                lastname: '',
                email: '',
                address: ''
               
            }
        }
    },
    methods: {
     submit() {
  return {
    results: []
  }
},

  // mounted: function(

  getData(){
  axios
  .get('http://localhost:3000/sampletable', this.form)
  .then(()=> console.log(this.form))
  .catch((error) => console.log(error))
},

addData(){
  axios
  .post('http://localhost:3000/sampletable', this.form)
  .then(()=> console.log(this.form))
  .catch((error) => console.log(error))
},

updateData() {
  axios
  .put('http://localhost:3000/sampletable', this.form)
  .then(()=> console.log(this.form))
  .catch((error) => console.log(error))
},

deleteData() {
  axios
  .delete('http://localhost:3000/sampletable', this.form)
  .then(()=> console.log(this.form))
  .catch((error) => console.log(error))
    
//  updateData()  {
//   fetch('http://localhost:3000/sampletable/:id', 
//   {
//     method: 'put',
//     body: JSON.stringify({
//       firstname: '',
//                 lastname: '',
//                 email: '',
//                 address: ''
//     }),
//     Headers:{
//       "content-Type": "application/json",
//     },
//   })
//   .then((response) => {
//     //  console.log(response.json())
//    return response.json()})
//   .then ((jsonData) => {
//     //this.results = jsonData
//     this.results = jsonData
//     console.log(this.jsonData)
//   })
  }
 }}

     
</script>
