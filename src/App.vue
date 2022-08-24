<template>
  <div>
    <HeaderItem :links="headerMenu" />
    <main>
      <section id="careers-section">
        <div class="text-center">
          <p>START LEARNING CODING LANGUAGE</p>
          <h1><strong>Build Your Dream </strong><span>TODAY</span></h1>
        </div>
      </section>
    </main>
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
h1 {
  color: $mulled_wine;
  span {
    color: $jungle_green;
  }
};
p {
  color: $oslo_gray;
}
</style>
