<template>
  <div>
    <div v-for="question in data" :key="question._id" class="question-wrapper">
      <div class="question">
        <p>{{question.title}}</p>
        <span class="user">{{question.user}}</span>
      </div>

      <answer-list :data="question.answers"></answer-list>
    </div>
  </div>
</template>

<script>
import AnswerList from './AnswerList.vue'

export default {
  props: {
    data: {
      required: true
    }
  },
  components: {
    AnswerList
  }
}
</script>

<style scoped>
  .question-wrapper {
    display: flex;

  }
  .question {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin-bottom: 10px;
    padding: 0;
    width: 300px;
    height: 120px;
    border: 1px solid black;
    background-color: cornflowerblue;
    border-radius: 5px;
  }
  .question p {
    flex-grow: 1;
    margin: 0;
    padding: 12px;
  }
  .question .user {
    padding: 4px;
    padding-right: 14px;
    font-weight: 700;
    text-align: right;
    background-color:lavender;
    border-radius: 5px;
  }
</style>
