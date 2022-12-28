<template>
    <h1 class="font-bold text-2xl text-center py-10" >Top 10 Jokes Page</h1>

    <ul>
        <div class="flex  flex-wrap">
                <li  class="w-1/3 px-4 py-5 w-30 border bg-gray-300 border-gray-100 p-4 mb-4 " v-for="joke in jokes">
                    <h4 class="font-bold">{{joke.setup}}</h4>
                    <p>{{ joke.punchline }}</p>
                </li>
        </div>
    </ul>
</template>



<script>
// import SinglePost from "../components/SinglePost.vue";

  export default {
    name: "HomePage",
    data() {
        return {
            university: []
        }
    },

    mounted() {
    fetch('https://official-joke-api.appspot.com/random_ten')
      .then(response => response.json())
      .then(json => this.jokes = json )
    }
}
</script>




<style scoped>

</style>
