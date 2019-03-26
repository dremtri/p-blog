<template>
  <div id="app">
      <header class="mb-15">
          <dremtri-header></dremtri-header>
      </header>
      <div class="content mb-15">
          <router-view/>
      </div>
      <footer>
          <dremtri-footer></dremtri-footer>
      </footer>
  </div>
</template>

<script>
import DremtriHeader from '@/components/common/DremtriHeader'
import DremtriFooter from '@/components/common/DremtriFooter'
export default {
  name: 'App',
  components: {
    DremtriFooter,
    DremtriHeader
  }
}
</script>

<style scoped>
#app {
    display: flex;
    flex-direction: column;
    min-height: 100%;
}
.content {
    flex: 1;
}
</style>
