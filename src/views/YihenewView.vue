<template>
  <div  >
    <div v-if="isVisile">
      <Yihenew :isDarkTheme='isDarkTheme' :isVisile='isVisile' @closes ='hide'>
        <h1 class="active">{{title}}</h1>
      </Yihenew>
    </div>
    <h1>HELLO this is yihenew page</h1>
    <button @click="hide">
      hide
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
          isVisile: false
          }
    },
    methods:{
      hide(){
        this.isVisile = !this.isVisile
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