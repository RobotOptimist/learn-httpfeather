<template>
  <div class="p-10 pt-0">
    <h1 class="mt-6 h1 leading-tight text-center">Learn .NET Feather HTTP</h1>
    <div class="lg:flex lg:justify-center w-full">
      <div class="lg:max-w-md lg:w-1/5 hidden lg:block">
        <topics-list></topics-list>
      </div>
      <div class="lg:w-2/3 mt-6">
        <section>
          <div class="ml-10">
            <h2 class="text-4xl text-green-600 text-center">Getting Started</h2>
            <h3 class="text-3xl text-green-600 text-center">Download VS Code</h3>
            <p>We recommend using VS Code in order to get a consistent experience with what we describe in these docs.
            You can get VS Code by clicking the link. It will open to the VS Code download page in a new tab.</p>
            <p class="text-center">
              <a class="underline" href="https://code.visualstudio.com/" target="_blank" rel="noreferrer">Download VS Code</a>
            </p>            
            <p>Once you've installed VS Code you may want to get some extensions so you can have a better editing experience while working with C#.</p>
            <h3 class="text-3xl text-green-600 text-center">Download .NET Core 3.1</h3>
            <p>The .NET Core runtime is required in order to run .NET applications.</p>
            <h3>Get the dotnet CLI</h3>
            <h3>(optional) Copy and add the dotnet feather template repository</h3>
            <h3>Next steps - try Hello World</h3>
          </div>
        </section>
        <section class="lg:flex flex-wrap justify-center">
          <card class="lg:w-64 w-full" v-for="topic in topics" :key="topic.title" :title="topic.title" :description="topic.description"></card>
        </section>
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
