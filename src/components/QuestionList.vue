<template>
  <div>
    <div v-for="question in questions" :key="question._id">
      <div class="question">
        <h2>{{question.title}}</h2>
        <p>{{question.description}}</p>
      </div>

      <idea-list :data="question.ideas"></idea-list>

    </div>
  </div>
</template>

<script>
import IdeaList from './IdeaList.vue'

export default {
  name: 'QuestionList',
  components: {
    IdeaList
  },
  props: {
    questions: {
      required: true
    }
  },
  data: () => {
    return {
      number: 0
    }
  }
}
</script>

<style scoped>
  .question {
    display: flex;
    flex-direction: column;
    margin: 0;
    margin-bottom: 40px;
    padding: 10px;
    /* width: 300px; */
    color: #fff;
    font-size: 1rem;
    border: 1px solid #2e3b7d;
    background-color: #81bed5;
    border-radius: 5px;

  }

  .question h2 {
    margin: 0;
  }
</style>
