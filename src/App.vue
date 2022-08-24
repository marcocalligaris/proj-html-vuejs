<template>
  <div>
    <HeaderItem :links="headerMenu" />
  </div>
</template>

<script>
import HeaderItem from './components/HeaderItem.vue';

export default {
  name: "App",
  components: { HeaderItem },
  data() {
    return {
      headerMenu:[
        {id:1, url:'#', text:'Home'},
        {id:2, url:'#', text:'Pages'},
        {id:3, url:'#', text:'Courses'},
        {id:4, url:'#', text:'Features'},
        {id:5, url:'#', text:'Blog'},
        {id:6, url:'#', text:'Shop'},
        ],
    }
  },
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
</style>
