<template>
    <div>
        <comment-item
             v-for="(comment) in comments" 
             :comment="comment"
             :key="comment.id"
        />   
        
    </div>
</template>

<script>
  import CommentItem from './CommentItem.vue'
    export default {
      data(){
            return {
               commentOtz:5
            }
        },  
      components: { CommentItem },
        props:{
            comments:{
                type:Array,
                required:true
            }

        }
          
    }
</script>

<style  scoped>

</style>