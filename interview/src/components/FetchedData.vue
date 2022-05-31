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
        const response = await fetch('https://my-json-server.typicode.com/Dmytro-Lukashenko/interview-project/questions')        
        const fetchedQuestions = await response.json()
        fetchedQuestions.forEach(group => console.log(group))
        
    }
}
</script>

<style>

</style>