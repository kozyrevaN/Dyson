<template>
    <div>
        <Header  :tovarsKorzina="tovarsKorzina"></Header>
        <InfoIMG ></InfoIMG>
        <div style="max-width:1900px">
        <div style="font-size:46px;font-weight:900;line-height:50.6px;margin-top:30px;">Спецпредложения </div>
        <my-select
            v-model="selectedSort"
            
            :options="sortOptions"
            style="margin-left:80%;"
            >
            
        </my-select>
        </div>
        <tovar-list
             :tovars="sortedTovars"
        />

        <InfoIMG2 ></InfoIMG2>
        
        <div style="display:flex;background-color:#ffffff;padding-top:150px">
            <h1 style="background-color:#ffffff;color:#111111;font-size:42px;line-height:50.4px;padding-left:280px;padding-bottom:20px;">Отзывы</h1>
            <h1 style="background-color:#ffffff;color:#C5358C;font-size:42px;line-height:50.4px;">151</h1>
        </div>
        <div style="display:flex; background-color:#ffffff;padding-left:280px;padding-right:280px;">

            <comment-title style=" background-color:#ffffff;"></comment-title>
            <my-Button2 class="btn" @click="showDialog" style=":hover {background-color:red;}">
            <p
             style="
                color:#111111;
                weight:400;
                font-size:24px;
                line-height:32.68px;
                margin-top:100px;
             "


            >Написать отзыв</p> 
            </my-Button2>
        </div>
        
        
        <comment-list
            :comments="comments"
            style=" background-color:#ffffff;padding-bottom:150px;"
        />
        <my-dialog v-model:show="dialogVisible">
            <CommentForm   @create="createComment"></CommentForm>
        </my-dialog>
        
    </div>
</template>

<script>
import Header from './components/Header';
import InfoIMG from './components/InfoIMG';
import TovarList from './components/TovarList';
import CommentList from './components/CommentList';
import CommentForm from './components/CommentForm';
import CommentTitle from './components/CommentTitle';
import InfoIMG2 from './components/InfoIMG2';

    export default {
        name:'App',
        components:{
            Header,InfoIMG,TovarList,CommentList,CommentForm,CommentTitle,InfoIMG2
        },
         data() {
        return {
            tovars:[
                {id:1,nalichie:'В наличии',skid:'-15%',price:'59 990 Р',oldprice:'69 990 Р',img:'fen1.png',text:'Фен Dyson Supersonic HD07 синий медный с 5 насадками в чехле и расческамия'},    //от сюда мы получали посты до того как взяли их с сервера
                {id:2,nalichie:'В наличии',skid:'-15%',price:'47 990 Р',oldprice:'51 990 Р',img:'fen2.png',text:'Фен Dyson Supersonic HD07 с 5 насадками и подставкой'},
                {id:3,nalichie:'В наличии',skid:'-15%',price:'46 990 Р',oldprice:' 990 Р',img:'fen3.png',text:'Фен Dyson Supersonic 4 насадки HD03 с чехлом для хранения цвет сирень'},
                {id:4,nalichie:'Нет в наличии',skid:'-15%',price:'59 990 Р',oldprice:'69 990 Р',img:'fen4.png',text:'Фен Dyson Supersonic HD07 синий медный с 5 насадками в чехле и расческамия'},
                {id:5,nalichie:'В наличии',skid:'-15%',price:' 990 Р',oldprice:'51 990 Р',img:'fen5.png',text:'Фен Dyson Supersonic HD07 с 5 насадками и подставкой'},
                {id:6,nalichie:'В наличии',skid:'-15%',price:'46 990 Р',oldprice:'51 990 Р',img:'fen6.png',text:'Фен Dyson Supersonic 4 насадки HD03 с чехлом для хранения цвет сирень'},


            ],
            selectedSort: '',
            dialogVisible:false,
            comments:[
                {id:1,line:'line.png',data:'21/05/2022',name:'Ольга',title:'Это лучший фен!',text:'Пользуюсь около месяца, хочу поделиться впечатлениями. Во-первых, фен очень легкий, удобно лежит в руке, не скользит. Кнопка включения и выключения расположена удобно, а не где-то сбоку. Мощность у фена хорошая, волосы сушит быстро',img:''},
                {id:2,line:'line.png',data:'21/05/2022',name:'Татьяна',title:'Отличный фен',text:'Фен очень понравился. Качественный, стильный: свою цену полностью оправдывает!',img:''},
                {id:3,line:'line.png',data:'21/05/2022',name:'Виктор',title:'Быстро пришел',text:'Фен очень понравился. Качественный, стильный: свою цену полностью оправдывает!',img:''},
            ],
            sortOptions:[
                {value:'text',name:'по тексту'},
                {value: 'price' ,name:'Сначала дешевые'},
                {value: 'nalichie' ,name:'по наличию'},
                {value: 'oldprice' ,name:'по популярности'}
            ],
            
            }
         },
         methods:{
                createComment(comment){
                    this.comments.push(comment);
                },
                showDialog(){
                    this.dialogVisible=true;
                }
         },
         
            computed:{
                sortedTovars(){
                  return[...this.tovars].sort((tovar1,tovar2)=> tovar1[this.selectedSort]?.localeCompare(tovar2[this.selectedSort],undefined,{'numeric':true}))
                
            },
            watch: {
                tovarsKorzina(newValue){
                 return (newValue)
                }
             
        
            }
    
         }
        
    }
</script>

<style  scoped>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    background-color: #F8F8F8;
   
}

</style>