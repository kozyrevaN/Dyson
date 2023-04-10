<template>
    <div
    style="
    border-color:#111111;
    width:220px;
    height:64px;
    border-radius:3px;
    display:flex;
    
    border-width:3px;
    "
    >
        <button
            @click="removeTovar"
            style="
            
            width:72px;
            height:64px;
            border-radius:3px;
            border:none;
            padding:20px;
            background-color:#ffffff;
            "
        
        ><img  src="../../assets/minus.png" alt=""></button>
        <div 
           style="
            width:72px;
            height:60px;
            border-radius:3px;
            border:none;
            padding: 15px;
            padding-left: 40px;
            font-size:24px;
            "
         >{{tovarsKorzina}}</div>
         
         
           <button
           @click="addTovar"
           
           style="
           
            width:72px;
            height:64px;
            border-radius:3px;
            border:none;
            padding:20px;
            background-color:#ffffff;
            "
        
        ><img src="../../assets/plus.png" alt=""></button>
    </div>
</template>

<script>
    export default {
        name:'my-counter',
        data(){
            return {
               tovarsKorzina:0
            }
        },
        methods: {
            addTovar(){
            this.tovarsKorzina +=1;
            
            },
            removeTovar(){
            this.tovarsKorzina -=1;
            },
            
            
        
        },

        
    }
</script>

<style scoped>

</style>