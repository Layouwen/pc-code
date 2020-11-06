<template>
  <Header/>
</template>

<script>
import Header from '../components/Header.vue'

export default {
  name: 'Home',
  components: { Header },
  props: {
    msg: String
  },
  data () {
    return {
      count: 0
    }
  }
}
</script>
