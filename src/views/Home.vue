<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
// import axios from 'axios'
import jsonp from 'jsonp'

export default {
  name: 'Home',
  components: {
    // HelloWorld
  },
  data() {
    return {
        age: 30
    }
  },
  mounted() {
    let url="https://www.imooc.com/activity/newcomer"
    // axios.get(url).then(()=>{ })
    jsonp(url,(err,res)=>{
      let result = res
      this.data = result
    })

  },
}
</script>
