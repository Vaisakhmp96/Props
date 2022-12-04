<template>
  <div id="app">
    <app-header v-bind:title="title" v-on:changeTitle="updateTitle($event)"></app-header>
    <app-ninjas v-bind:ninjas="ninjas"></app-ninjas>
    <app-footer></app-footer>
  </div>
</template>

<script>
import HeaderData from './components/HeaderData.vue'
import FooterData from './components/FooterData.vue'
import NinjasData from './components/NinjasData.vue'
export default {
  components: {
     'app-header':HeaderData,
     'app-footer':FooterData,
     'app-ninjas':NinjasData
  },
  data() {
    return{
      ninjas:[
       {name:'Ryu', speciality:'Vue Components', show:false},
       {name:'Cristal', speciality:'HTML Wizardry', show:false},
       {name:'Hitesh', speciality:'Click events', show:false},
       {name:'Tango', speciality:'Conditionals', show:false},
       {name:'Tom', speciality:'Webpack', show:false},
       {name:'Roy', speciality:'Data Diggin', show:false}
      ],
      title: "Vue Ninjas"
    
    }
  },
 methods: {
  changeTitle: function(updatedTitle){
    this.title = updatedTitle; 
  }
 }
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
