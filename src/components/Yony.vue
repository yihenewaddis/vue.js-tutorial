<template>
    <div class="name" :class="{darkTheme:isDarkTheme}"  @click="close" >
        addis kassa yallew and the title is {{title}}
        <br>
        <div>
        <button>
            show
        </button>
        </div>
    </div>
  
</template>
<script>
export default{
    props:['title','isDarkTheme','isVisile','hide'],
    methods:{
        close(){
            this.$emit('close')
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