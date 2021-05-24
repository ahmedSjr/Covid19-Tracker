<template>
  <Header />
  <div class="container">
  <router-view/>
  </div>
</template>

<script>

import Header from '@/components/Header'
import axios from 'axios'

export default {
  components: {
    Header,
  },
  async created() {
    const {data} = axios.get
  }
}
</script>
