<template>
  <div id="app">
  <component :is="layout">
    <router-view/>
    </component>
  </div>
</template>

<style >
@import '~materialize-css/dist/css/materialize.min.css';
@import 'assets/index.css';

</style>

<script>
import EmptyLayout from '@/layouts/EmptyLayput'
import MainLayout from '@/layouts/MainLayout.vue'

export default {
  computed:{
    layout(){
      return (this.$route.meta.layout || 'empty') + '-layout'
    }
  },
  components:{
    EmptyLayout, MainLayout
  }
}
</script>
