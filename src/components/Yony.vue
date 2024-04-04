<template>
    <div class="name" :class="{darkTheme:isDarkTheme}">
        <slot>

        </slot>
        <slot name="link">

        </slot>
        <br>
        <div>
        <button  @click="close" >
            hide this page
        </button>
        </div>
    </div>
  
</template>
<script>
export default{
    props:['isDarkTheme','isVisile','hide'],
    methods:{
        close(){
            this.$emit('closes')
        }
    }
}
// import {ref} from 'vue'
// // const hello = ref(props.hello)
// const count = ref(0)
// const title = ref('this is yihenew addis kassa yalew')
// const handleclick = ()=>count.value +=1
</script>

<style>
.name {
color: black;
position: fixed;
width: 100%;
height: 100%;
margin: 0;
top: 0;
opacity: .7;
}
.darkTheme{
    color: white;
    background-color: black;
}
.button{
    color: white;
}
</style>