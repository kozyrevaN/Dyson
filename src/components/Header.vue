<template>
    <div class="header">
        <img src="../assets/icon_spisok.png" alt="" class="icon_spisok" style="margin:34px">
        <img src="../assets/logo1.png" alt="" class="logo" style="padding:7px 0">
        
        <a href="#" class="text" style="color:#ffffff;text-decoration:none;font-size:20px;font-weight:900; padding:31px 0;line-height:50px;" onmouseover="this.style.color='#C5358C';" onmouseout="this.style.color='#ffffff';">О нас</a>
        <a href="#" class="text" style="color:#ffffff;text-decoration:none;font-size:20px;font-weight:900;padding:31px 0; line-height:50px;" onmouseover="this.style.color='#C5358C';" onmouseout="this.style.color='#ffffff';">Доставка и оплата</a>
        <a href="#" class="text" style="color:#ffffff;text-decoration:none;font-size:20px;font-weight:900; padding:31px 0;line-height:50px;" onmouseover="this.style.color='#C5358C';" onmouseout="this.style.color='#ffffff';">Регистрация продукта</a>
        <a href="#" class="text"  style="color:#ffffff;text-decoration:none;font-size:20px;font-weight:900;padding:31px 0; line-height:50px;" onmouseover="this.style.color='#C5358C';" onmouseout="this.style.color='#ffffff';">Сервис</a>
        <a href="#" class="text"  style="color:#ffffff;text-decoration:none;font-size:20px;font-weight:900;padding:31px 0; line-height:50px;" onmouseover="this.style.color='#C5358C';" onmouseout="this.style.color='#ffffff';">Сертификаты и лицензии</a>
        
        <div>
        <img src="../assets/korzina.png" alt="" class="korzina"  style="margin:38px">
        <div>{{korzina}}</div>
        </div>

    </div>
</template>

<script>
    export default {
        props:{
            korzina:{
                type:Number,
                
            }
        },
        
    }
</script>

<style  scoped>
.header{
    background-color: #111111;
    display: flex;
    justify-content: space-between;
    padding: 0 290px;
    color: #ffffff;
    width: 1920px;
}  


</style>

