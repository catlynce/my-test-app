<template>
  <div class="reaction-wrapper">
    <div v-for="reaction in data" :key="reaction._id">
      <div class="reaction">
        <p>{{reaction.description}}</p>
        <span class="user">{{reaction.user}}</span>
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
  .reaction-wrapper {
    display: flex;
    margin-left: 30px;
    flex-direction: row;
  }
  .reaction {
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
  .reaction p {
    flex-grow: 1;
    margin: 0;
    padding: 12px;
  }
  .reaction .user {
    padding: 4px;
    padding-right: 14px;
    font-weight: 700;
    text-align: right;
    background-color:lavender;
    border-radius: 5px;
  }
</style>
