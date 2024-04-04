<template>
  <div  >
    <div v-if="isVisile1">
      <Yihenew :isDarkTheme='isDarkTheme' :isVisile='isVisile' @closes ='hide("first")'>
        <h1 class="active">{{title}}</h1>
        <template v-slot:link>
          <a href="#">first link</a>
          <a href="#">second link</a>
        </template>
      </Yihenew>
    </div>
    <div v-if="isVisile2">
      <Yihenew :isDarkTheme='isDarkTheme' :isVisile='isVisile' @closes ='hide("second")'>
        <h1 class="active">{{title}}</h1>
        <template v-slot:link>
          <a href="#">second link frome here </a>
          <a href="#">third link from here </a>
        </template>
      </Yihenew>
    </div>
    <h1>HELLO this is yihenew page</h1>
    <button @click="hide">
      first Model
    </button>
    <button @click="hide">
      secold Model
    </button>
  </div>
</template>

<script>
  import Yihenew from '../components/Yony.vue'
  export default{
    components:{
    Yihenew,
    },
    data(){
        return {
          count: 0,
          title:'this is the title from slot',
          isDarkTheme:true,
          isVisile1: false,
          isVisile2: false
          }
    },
    methods:{
      hide(val){
        if(val === 'forst'){
          this.isVisile1 = !this.isVisile1
        }else{
            this.isVisile2 = !this.isVisile2
        }
      }
    }
}
  // import {ref} from 'vue'
  // const inputRef = ref(null)
  // const handleClick=()=>inputRef.value.classList.add('active')
  // const props = defineProps(
  //   {
  //     hello:'hello world'
  //   }
  // )
</script>
<style scoped>
.active{
  border-color: red;
}
</style>