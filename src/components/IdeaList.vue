<template>
  <div>
    <div v-for="idea in data" :key="idea._id" class="idea-wrapper">
      <div class="idea">
        <p>{{idea.title}}</p>
        <span class="user">{{idea.user}}</span>
      </div>

      <reaction-list :data="idea.reactions"></reaction-list>
    </div>
  </div>
</template>

<script>
import ReactionList from './ReactionList.vue'

export default {
  props: {
    data: {
      required: true
    }
  },
  components: {
    ReactionList
  }
}
</script>

<style scoped>
  .idea-wrapper {
    display: flex;

  }
  .idea {
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
  .idea p {
    flex-grow: 1;
    margin: 0;
    padding: 12px;
  }
  .idea .user {
    padding: 4px;
    padding-right: 14px;
    font-weight: 700;
    text-align: right;
    background-color:lavender;
    border-radius: 5px;
  }
</style>
