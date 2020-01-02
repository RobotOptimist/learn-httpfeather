<template>
  <div class="p-10 pt-0">
    <h1 class="mt-6 text-5xl text-green-600 font-semibold leading-tight text-center">Learn .NET Feather HTTP</h1>
    <div class="lg:flex">
      <div class="lg:max-w-sm lg:w-full">
        <topics-list></topics-list>
      </div>
      <div class="lg:flex flex-wrap">
        <card class="lg:max-w-xs w-full" v-for="topic in topics" :key="topic.title" :title="topic.title" :description="topic.description"></card>
      </div>
    </div>
  </div>
</template>

<script>
import card from '../components/card'
import topicsList from '../components/topicsList'
export default {
  components: {
    card,
    topicsList
  },
  computed: {
    topics() {
      return this.$store.getters['topics/list'];
    }
  }
}
</script>
