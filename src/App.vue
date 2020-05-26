<template>
  <div id="app">
    <thread-list :threads=threads ></thread-list>
  </div>
</template>

<script>
import source from './data.json'
import ThreadList from './components/ThreadList.vue'

export default {
  name: 'App',
  components: {
    ThreadList
  },
  data: () => {
    return {
      threads: source.threads
    }
  }
}
</script>
