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
        <div id="statistics" class="mb-5">
          <div class="container py-5">
            <ul class="d-flex justify-content-between">
              <li class="text-center" v-for="item in statistics" :key="item.id">
                <p class="fs-1 fw-bold">{{ item.text }}</p>
                <span class="fw-semibold">{{ item.description }}</span>
              </li>
            </ul>
          </div>
        </div>
      </section>
      <section id="courses-section" class="pb-5 mb-5">
        <div class="text-center mb-5 generic-title">
          <p>CHOOSE WHERE YOU'D LIKE TO BEGIN</p>
          <h1><strong>Last Featured </strong><span>Courses</span></h1>
        </div>
        <div class="container">
          <div class="row g-5 d-flex justify-content-between mb-5">
            <div v-for="item in courses" :key="item.id" class="col-4">
              <div id="course-card" class="card border-0">
                <div class="position-relative">
                  <div id="course-price" class="text-center py-2 px-3">
                    <span class="text-white fw-bold">{{ item.price }}</span>
                  </div>
                  <img :src="item.url" class="card-img-top" :alt="item.title">
                </div>
                <div class="card-body">
                  <div class="d-flex align-items-center mb-2">
                    <img class="rounded-circle me-2" :src="item.photo" :alt="item.teacher">
                    <span>{{ item.teacher }}</span>
                  </div>
                  <h5 class="card-title fw-bold">{{ item.text }}</h5>
                </div>
                <div class="card-body">
                  <span class="me-5"><i class="fa-regular fa-file-lines me-2"></i>{{ item.lessons }} Lessons</span>
                  <span><i class="fa-regular fa-user me-2"></i>{{ item.students }} Students</span>
                </div>
              </div>
            </div>
          </div>
          <div class="d-flex justify-content-center">
            <button type="button" class="btn fw-bold py-2 px-4 mb-5">
                View all courses <i class="fa-solid fa-arrow-right-long"></i>
            </button>
          </div>
        </div>
      </section>
      <section id="learning-options">
        <div class="container pt-5">
          <div class="row d-flex mb-5">
            <div class="col-4">
              <div class="mb-5 generic-title w-75">
                <p>WHY HESITATE TO REGISTER?</p>
                <h1><strong>Learn At Your Own </strong><span>Pace</span></h1>
              </div>
              <ul class="mb-5">
                <li class="mb-3"><i class="fa-solid fa-check text-success me-2"></i>Select & customize courses to your preferences</li>
                <li class="mb-3"><i class="fa-solid fa-check text-success me-2"></i>Change the tutor and make arrangements</li>
                <li class="mb-3"><i class="fa-solid fa-check text-success me-2"></i>Participate in events to join others</li>
                <li class="mb-3"><i class="fa-solid fa-check text-success me-2"></i>Get the desired certificate delivered at house</li>
              </ul>
              <button type="button" class="btn fw-bold py-2 px-4 mb-5">Get started for free</button>
            </div>
            <div class="col-7">
              <div id="laptop-learning">
                <img class="position-relative" id="laptop" src="./assets/img/home-5-image-01.png" alt="Laptop learning">
                <div class="position-relative">
                  <img class="position-absolute" id="max-circle" src="./assets/img/maxcoach-shape-05.png" alt="Maxcoach shape">
                </div>
              </div>
            </div>
          </div>
          <div class="row pt-5">
            <div class="col-6">
              <div id="mobile-learning" class="position-relative">
                <img id="mobile" class="position-relative" src="./assets/img/home-5-image-02.png" alt="Mobile learning">
                <img id="max-square" class="position-relative" src="./assets/img/maxcoach-shape-01.png" alt="Maxcoach shape">
              </div>
            </div>
            <div class="col-5 d-flex align-items-center">
              <div>
                <div class="mb-4 generic-title">
                  <p>WHAT ARE YOU LOOKING FOR?</p>
                  <h1><strong>Learn on your </strong><span>mobile </span><strong>anytime!</strong></h1>
                </div>
                <p class="mb-5">Save lessons for later and revise or write notes at any time and on multiple devices on your way. Never interfere with activities of enjoyment or other precious moments.</p>
                <button type="button" class="btn fw-bold py-2 px-4 mb-5">Download Our App</button>
              </div>
            </div>
          </div>
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
        {
          id:1,
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
          title: 'System Administration',
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
      statistics:[
        {id:1, text: '1.926', description: 'FINISHED SESSIONS'},
        {id:2, text: '3.092+', description: 'ENROLLED LEARNERS'},
        {id:3, text: '200', description: 'ONLINE INSTRUCTORS'},
        {id:4, text: '100%', description: 'SATISFACTION RATE'},
      ],
      courses: [
        {
          id: 1,
          title: 'Learning to write',
          text: 'Learning to Write as a Professional Author',
          price: '$40.00',
          teacher: 'Blanche Fields',
          photo: require('./assets/img/blanche-2.jpeg'),
          url: require('./assets/img/course-01.jpg'),
          lessons: '20',
          students: '50',
        },
        {
          id: 2,
          title: 'Info-Tech Strategies',
          text: 'Customer-centric Info-Tech Strategies',
          price: 'Free',
          teacher: 'Maggie Strickland',
          photo: require('./assets/img/maggie-2.jpeg'),
          url: require('./assets/img/course-02.jpg'),
          lessons: '24',
          students: '769',
        },
        {
          id: 3,
          title: 'Python',
          text: 'Open Programming Courses for Everyone: Python',
          price: '$19.00',
          teacher: 'Maggie Strickland',
          photo: require('./assets/img/maggie-2.jpeg'),
          url: require('./assets/img/course-03.jpg'),
          lessons: '17',
          students: '62',
        },
        {
          id: 4,
          title: 'Academic listening',
          text:'Academic Listening and Note-taking',
          price: '$26.00',
          teacher: 'Blanche Fields',
          photo: require('./assets/img/blanche-2.jpeg'),
          url: require('./assets/img/course-04.jpg'),
          lessons: '14',
          students: '67',
        },
        {
          id: 5,
          title: 'Master jQuery',
          text:'Master jQuery in a Short Period of Time',
          price: '$39.00',
          teacher: 'Blanche Fields',
          photo: require('./assets/img/blanche-2.jpeg'),
          url: require('./assets/img/course-05.jpg'),
          lessons: '6',
          students: '51',
        },
                {
          id: 6,
          title: 'Javascript',
          text:'Introduction to Javascript for Beginners',
          price: '$59.00',
          teacher: 'Blanche Fields',
          photo: require('./assets/img/blanche-2.jpeg'),
          url: require('./assets/img/course-06.jpg'),
          lessons: '14',
          students: '76',
        },
      ],
    }
  },
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
ul {
  list-style-type: none;
  text-decoration: none;
  padding: 0;
  margin: 0;
}
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
.btn {
  font-size: 12px;
  background-color: $jungle_green;
  color: white;
  &:hover {
    cursor: pointer;
    background-color: $mulled_wine;
    color: white;
  }
};
#careers-gallery {
  a {
    color: $oslo_gray;
  }
};
#statistics {
  background-color: $gallery;
  p.fs-1 {
    color: $jungle_green;
  };
};
#courses-section {
  background-image: linear-gradient(white, $gallery);
  clip-path: ellipse(140% 100% at 50% 0%);
  #course-card {
    background-color: transparent;
    &:hover {
      cursor: pointer;
      box-shadow: 0 0 30px gray;
      transition: 1s;
    }
    span {
      color: gray;
    };
    #course-price {
      position: absolute;
      right: 0;
      background-color: $jungle_green;
      width: 100px;
      border-radius: 0 5px 0 5px;
    };
  };
};
#learning-options {
  li {
    font-size: 12px;
  }
  #laptop-learning {
    background-image: url('./assets/img/underlay-shape-grey.svg');
    background-repeat: no-repeat;
    background-position: left bottom;
    background-size: 400px;
    #laptop {
      left: 100px;
      object-fit: contain;
    };
    #max-circle {
      right: 150px;
      bottom: 90px;
    };
  };
  #mobile-learning {
    background-image: url('./assets/img/underlay-shape-grey.svg'), url('./assets/img/maxcoach-shape-07.png'), url('./assets/img/orange-circle.png');
    background-repeat: no-repeat, no-repeat, no-repeat;
    background-position: left bottom, 400px 300px, 520px 30px;
    background-size: 400px, auto, 50px;
    #mobile {
      bottom: 30px;
      left: 100px;
    };
    #max-square {
      left: -75%;
    }
  }
};
</style>
