<template>
    <form  @submit.prevent>
        <h4>Написать комментарий</h4>
        <my-input 
            v-model="comment.name"
            type="text" 
            placeholder="ФИО"
        ></my-input>
        <my-input
            v-model="comment.title"
            type="text" 
            placeholder="Название"
        ></my-input>
        <my-input
            v-model="comment.text"
            type="text" 
            placeholder="Текст"
        ></my-input>
        <my-input
            v-model="comment.data"
            type="text" 
            placeholder="Дата"
        
        ></my-input>

        
        <my-Button2  @click="createComment">

        </my-Button2 >
    </form>
</template>

<script>
    export default {
        data(){
            return{
                comment:{
                    name:'',
                    title:'',
                    text:'',
                    data:'',   
                }
            }
        },
        methods:{
            createComment(){
                this.comment.id= Date.now();
                this.$emit('create',this.comment)
                this.comment={
                    name:'',
                    title:'',
                    text:'',
                    data:'',   
                }


            },
        }
        
    }
</script>

<style  scoped>
form{
    display: flex;
    flex-direction:column;
}
</style>