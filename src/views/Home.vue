<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import axios from 'axios'
// import jsonp from 'jsonp'

export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  data() {
    return {
        age: 30
    }
  },
  mounted() {
    let url=" https://easy-mock.com/mock/5e88b16a6e7d856cbee19bc2/example_copy/logon"
    axios.get(url).then(()=>{ })
    // jsonp(url,()=>{

    // })

  },
}
</script>
