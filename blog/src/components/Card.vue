<template>
<div class="card">
  <div class="card-header">
    {{ title }}
  </div>
  <div class="card-body">
    <blockquote class="blockquote mb-0">
      <p>{{ body }}</p>
      <footer class="blockquote-footer">created at : <cite title="Source Title">{{ created }}</cite></footer>
    </blockquote>
  <div>
      <strong>Comments</strong>
      <comment 
      v-for="(comment,i) in comments"
      :key="comment.id"
      :num="i + 1"
      :body="comment.body"></comment>
  </div>
  </div>
</div>
</template>

<script>
import Comment from "./Comment.vue";
export default {
    props: ['title','body','created','comments'],
    components :{
        Comment
    }
}
</script>

<style>

</style>
