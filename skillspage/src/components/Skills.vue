<template>
  <div class="hello">

<div class="holder">
<ul>

<li v-for="(data, index) in skills" :key="index"> {{index}}.{{data.skill}} </li>

</ul>
</div>

   {{name}}
 
     {{btnState ? "Button disabled":"Button enabled!!"}}
<button v-on:click="ModifyName" v-bind:disabled="btnState"> ModifyName </button>


  </div>
   </template>

<script>
export default {
  name: 'HelloWorld',
   data(){

     return {
       name: 'Coffee is Brown',
       btnState: false,

       skills:[ {"skill": "Vue.js"},  
                 { "skill": "Laravel"}, 
                 {"skill": "CodeIgniter"}, 
                  {"skill": "CakePHP" }     
        ]
     }
   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src = "./Skills.css" scoped>

</style>
