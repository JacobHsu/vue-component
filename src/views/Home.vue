<template>
  <div class="home">
    pass props function fromChildId: {{fromChildId}}
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <HelloWorld msg="Welcome to Your Vue.js App" :cb="parentFn" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
  },
  data() {
    return {
      fromChildId: 0
    }
  },
  methods: {
    parentFn(id) {
     this.fromChildId = id
    }
  }
}
</script>