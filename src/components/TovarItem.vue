<template>
    <div style="width:440px;background-color: #FFFFFF;">
        <div style="width:440px;background-color: #FFFFFF;" class="tovar">
                <img :src="require(`../assets/${tovar.img}`)">
                <div style="padding:40px">
                <div
                    style="
                        color:#111111;
                        font-size:24px;
                        weight:300;
                        width:360px;
                        line-height:32px;
                        margin-top:40px;
                        margin-bottom:25px;

                    "
                    >{{tovar.text}}
                </div>

                <div style="display:flex;justify-content: space-between;">
                    <div
                        style="
                             color:#68AE5C;
                             font-size:18px;
                             weight:400;
                             width:94px;
                             line-height:24px;
                             padding-top:10px;

                        "
                    >{{tovar.nalichie}}</div>


                    <skidki style="
                        color:#F8F8F8;
                        font-size:24px;
                        weight:400;
                        line-height:32px;
                        margin-bottom:8px;
                        
                        
                     "
                    >{{tovar.skid}}</skidki>
                </div>

                <div style="display:flex;justify-content: space-between;">
                    <div
                    style="
                        color:#111111;
                        font-size:42px;
                        weight:900;
                        width:177px;
                        line-height:50px;
                        margin-bottom:40px;

                    "
                    >{{tovar.price}}</div>

                    <div
                    style="
                        color:#ABABAB;
                        font-size:24px;
                        weight:900;
                        width:109px;
                        line-height:28.8px;
                        margin-top:26px;

                    "
                    >{{tovar.oldprice}}</div>


                </div>
                </div>

        </div>

        <div style="display:flex;justify-content: space-between;margin-bottom:30px;">
            <my-counter></my-counter>
            <my-Button></my-Button>
        </div>
    </div>

</template>

<script>

    export default {
        
        props:{
          tovar:{
            type: Object,
            required:true,
          }
        }
        
    }
</script>

<style  scoped>

</style>