<template>
  <div class="app">
    <post-form
      @create="createPost"
    />
    <post-list 
      :posts="posts"
    />
  </div>
</template>

<script>
import PostForm from './components/PostForm';
import PostList from './components/PostList';
export default {
  components: {
    PostForm,
    PostList
  },
  data() {
    return {
      posts: [
        {
          id: 1,
          title: "Пост о JS",
          body: "JavaScript",
        },
        {
          id: 2,
          title: "Пост о JS 1",
          body: "JavaScript 1",
        },
        {
          id: 3,
          title: "Пост о JS 2",
          body: "JavaScript 2",
        },
        {
          id: 4,
          title: "Пост о JS 3",
          body: "JavaScript 3",
        },
      ],
    };
  },

  methods: {
    createPost(post) {
      this.posts.push(post)
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.app {
  padding: 20px;
}
</style>