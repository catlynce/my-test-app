<template>
  <div class="answer-wrapper">
    <div v-for="answer in data" :key="answer._id">
      <div class="answer">
        <p>{{answer.description}}</p>
        <span class="user">{{answer.user}}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['data']
}
</script>

<style scoped>
  .answer-wrapper {
    display: flex;
    margin-left: 30px;
    flex-direction: row;
  }
  .answer {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin-right: 10px;
    margin-bottom: 10px;
    padding: 0;
    width: 300px;
    height: 120px;
    border: 1px solid black;
    background-color: lightgray;
    border-radius: 5px;
  }
  .answer p {
    flex-grow: 1;
    margin: 0;
    padding: 12px;
  }
  .answer .user {
    padding: 4px;
    padding-right: 14px;
    font-weight: 700;
    text-align: right;
    background-color:lavender;
    border-radius: 5px;
  }
</style>
