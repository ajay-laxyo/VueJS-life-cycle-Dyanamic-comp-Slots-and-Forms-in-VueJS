<template>
  <div align="center" style="background-color: gray; padding: 10px">
    <!--<student v-bind:myMsg="msg">
       <div slot="myNew" style="background-color: gray">
        <h1>this is a slot</h1>
        <h3> this slot is arriving from parant component</h3>
      </div> -->

      <!-- <div slot="form-header">
        <h2 style="background-color: gray">This is form Header</h2>
      </div>
      <div slot="form-element">
        <p> <input type="text" placeholder="Enter name"> </p>
        <p> <input type="text" placeholder="Enter email"> </p>
      </div>
      <div slot="form-button">
        <button v-on:click="submitDetails">Submit</button>
      </div>
      <div slot="form-footer">
        <h2 style="background-color: gray">This is form Footer</h2>
      </div> 
    </student>

    <h3> {{ simpleText }} </h3>

    <button @click="updateMessage()">Click here to update</button>-->

    <!-- component tag is pre defined by the Vue JS -->
    <!-- keep-alive tag is also pre defined by the Vue JS and used to reserve our input values as well -->
    <keep-alive>
      <component v-bind:is="component"></component>
    </keep-alive>

    <button v-on:click="component = 'student'">Student Form</button>
    <button v-on:click="component = 'employee'">Employee Form</button>
  </div>
</template>

<script>

import Student from './components/Student.vue'
import Employee from './components/Employee.vue'

export default {
  components:{
    "student" : Student,
    "employee" : Employee
  },
  data () {
    return {
      simpleText : "this is simple message",
      msg : "this message passed from Parant to Child",
      component : "student"
    }
  },
  methods:{
    updateMessage(){
        this.simpleText = "message updated successfully, Now I'm updated  .........!!!"
      }
  },
    // beforeCreate(){
    //   alert("before create");
    // },
    // created(){
    //   alert("created");
    // },
    // beforeMount(){
    //   alert("before Mount");
    // },
    // mounted(){
    //   alert("mounted");
    // },
    // beforeUpdate(){
    //   alert("before updated");
    // },
    // updated(){
    //   alert("updated");
    // }
}
</script>

