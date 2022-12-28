<template>
    <li class="my-5 list-none" >{{ post.title }} | <button class="bg-gray-200 py=5 px-6 ml-4">Add Post</button> <button class="bg-gray-200 py=5 px-6 ml-4">Add Fav</button> </li>
</template>

<script>
    export default {
        name: "SinglePost",
        props: ['post']
    }
</script>