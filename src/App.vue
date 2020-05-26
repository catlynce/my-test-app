<template>
  <div id="app">
    <question-list :questions=questions ></question-list>
  </div>
</template>

<script>
import source from './data.json'
import QuestionList from './components/QuestionList.vue'

export default {
  name: 'App',
  components: {
    QuestionList
  },
  data: () => {
    return {
      questions: source.questions
    }
  }
}
</script>
