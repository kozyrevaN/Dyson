<template>
<div>
    <div style="
        width:1360px;
        display:flex;
        position:relative;
        padding:20px 280px
    "
    >
       <div style="
       width:288px;
       margin-right:170px;
       font-size:20px;
       font-weight:500;
       line-height:30px;
       font-color:#111111;
       ">{{comment.name}}</div>
       <div>
            <div style="
                font-size:20px;
                font-weight:600;
                line-height:30px;
                font-color:#111111;
            "
            >{{comment.title}}</div>
            <div style="
            width:783px;
            font-size:18px;
            font-weight:300;
            line-height:25.2px;
            font-color:#111111;
            
            ">{{comment.text}}</div>
            
       </div>
       <div style="
        margin-left:251px;
        font-size:18px;
        font-weight:300;
        line-height:27px;
        font-color:#909090;
       
       ">{{comment.data}}</div>
       
       
    </div>
    <img src="../assets/line.png" alt="" style="padding-left:280px;">
</div> 
</template>

<script>
    export default {
        props:{
          comment:{
            type: Object,
            required:true,
          }
        }
    }
</script>

<style  scoped>

</style>