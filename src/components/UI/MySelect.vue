<template>
    <select :value="modelValue" @change="changeOption" style="width:273px;hight:80px;border-color:#C5358C;padding:10px;padding-left:30px;font-size:18px;font-weight:400;line-height:24.51px;">
        <option disabled value="">Выберите из списка</option>
        <option
            v-for="option in options"
            :key="option.value"
            :value="option.value"
        >
           <span > {{option.name}}</span>
        </option>
    </select>
</template>


<script>
    export default {
        name: 'my-select',
        props:{
            modelValue:{
                type:String
            },
            options:{
                type:Array,
                default:()=>[]

            }
        },
        methods:{
            changeOption(event){
                console.log(event)
                this.$emit('update:modelValue',event.target.value);
            }
        },
        
    }
</script>

<style  scoped>

</style>