<template>
  <div>

  </div>
</template>

<script>
export default {
    data(){
        return {
            questions: []
        }
    },
    async mounted(){
        const response = await fetch('https://my-json-server.typicode.com/Dmytro-Lukashenko/json-interview/posts')        
        const fetchedQuestions = await response.json()
        console.log(fetchedQuestions)
    }
}
</script>

<style>

</style>