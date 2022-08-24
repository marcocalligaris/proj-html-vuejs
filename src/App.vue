<template>
  <div>
    <HeaderItem :links="headerMenu" />
    <main>
      <!-- Sezione carriere -->
      <section id="careers-section">
        <div class="text-center mb-5 generic-title">
          <p>START LEARNING CODING LANGUAGE</p>
          <h1><strong>Build Your Dream </strong><span>TODAY</span></h1>
        </div>
        <div class="container py-5">
          <div class="row mb-5 d-flex justify-content-between" id="careers-gallery">
              <div 
                v-for="card in careersCards" :key="card.id"
                class="text-center mb-5 col-3"
                >
                  <img class="mb-4" :src="card.url" :alt="card.title">
                  <h5 class="mb-3 fw-bold">{{ card.title }}</h5>
                  <p class="mb-4">{{ card.text }}</p>
                  <a class="fw-bold" href="#">Start now <i class="ms-2 fa-solid fa-arrow-right-long"></i></a>
                </div>
          </div>
          <AboutItem />
        </div>
      </section>
    </main>
  </div>
</template>

<script>
import HeaderItem from './components/HeaderItem.vue';
import AboutItem from './components/AboutItem.vue';


export default {
  name: "App",
  components: { HeaderItem, AboutItem },
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
      careersCards:[
        {id:1,
        title: 'Idea Discussion',
        url: require('./assets/img/home-5-image-box-01.png'),
        text: 'Get teamed up with the specialists who work and teach coding for years at famous universities.',
        },
        {
          id:2,
          title: 'Web Development',
          url: require('./assets/img/home-5-image-box-02.png'),
          text: 'Learn to start building a webpage from scratch. You decide your own pace, course and speed.',
        },
        {
          id:3,
          title: 'Web Development',
          url: require('./assets/img/home-5-image-box-03.png'),
          text: 'Learners are encouraged to study the mechanism and structure of system administration.',
        },
        {
          id:4,
          title: 'Graphic Design',
          url: require('./assets/img/home-5-image-box-04.png'),
          text: 'Have a passion for graphics and arts? Show your talents with confidence and self-assertiveness.',
        },
      ],
    }
  },
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
.generic-title {
  h1 {
    color: $mulled_wine;
    span {
      color: $jungle_green;
    }
  };
  p {
    color: $oslo_gray;
  };
};
#careers-gallery {
  a {
    color: $oslo_gray;
  }
};
</style>
