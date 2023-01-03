<template>
    <div class="admin">
      <Panel/>
    </div>
</template>

<script>
  import Panel from '../components/Main/Panel.vue'

export default {
    name: 'AdminPanel',
    components: {
        Panel
  }
}
</script>

<style lang="sass" scoped>
  .admin
    background: #F3F3F3
</style>