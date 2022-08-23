<template>
  <div>
    <HeaderItem />
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
        {id:1, url:'#', text:'CHARACTERS', active: false},
        ],
    }
  },
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
</style>
