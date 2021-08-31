<template>
<div>
  <side-bar/>
  <home/>
</div>
</template>

<script>
import sideBar from '../components/side-bar.vue'
import home from '../pages/home.vue'
export default {
  components: { sideBar, home},
  }
</script>
