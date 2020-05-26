<template>
  <div>
    <div v-for="thread in threads" :key="thread._id">
      <div class="thread">
        <h2>{{thread.title}}</h2>
        <p>{{thread.description}}</p>
      </div>

      <question-list :data="thread.questions"></question-list>

    </div>
  </div>
</template>

<script>
import QuestionList from './QuestionList.vue'

export default {
  name: 'ThreadList',
  components: {
    QuestionList
  },
  props: {
    threads: {
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
  .thread {
    display: flex;
    flex-direction: column;
    margin: 0;
    margin-bottom: 40px;
    padding: 10px;
    width: 300px;
    font-size: 1rem;
    border: 1px solid #2e7d32;
    background-color: #AED581;
    border-radius: 5px;

  }

  .thread h2 {
    margin: 0;
  }
</style>
