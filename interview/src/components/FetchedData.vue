<template>
  <div>
    <ul>
        <li 
            v-for="question in questions"
            :key="question.id"
        >
        {{question.theme}}
        </li>        
    </ul>
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
        console.log(fetchedQuestions)  
        this.questions = {...fetchedQuestions}
        console.log(this.questions)
    }
}
</script>

<style>

</style>