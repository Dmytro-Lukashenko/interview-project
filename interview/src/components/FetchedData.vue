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
        const responce = await fetch('@db.json')
        const fetchedQuestions = await responce.json()
        console.log(fetchedQuestions)
    }
}
</script>

<style>

</style>