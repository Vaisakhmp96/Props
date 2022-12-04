<template>
<header>
    <h1 v-on:click="changeTitle">{{ title }}</h1>
</header>
    

</template>

<script>
export default {
   
        data() {
        return {
            title: 'Vue Ninjas'
        }
    },
   methods: {
    changeTitle: function() {
        this.title = "Vue Wizards"
    }
   } 
}
</script>

<style scoped>

</style>
