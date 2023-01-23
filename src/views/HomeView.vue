<template>

  <Banner />
  <Catalog />

</template>

<script>
import Banner from '../components/Main/Banner.vue'
import Catalog from '../components/Main/Catalog.vue'

export default {
  name: 'HomeView',
  components: {
    Banner,
    Catalog
  }
}
</script>
