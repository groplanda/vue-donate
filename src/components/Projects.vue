<template>
  <section class="projects">
    <div class="wrapper">
      <h3 class="projects__title title">проекты, которым  необходимо помочь </h3>
        <carousel :perPageCustom="[[320, 1], [768, 2], [1024, 3]]" :scrollPerPage="true">
          <!--item start-->
          <slide v-for="(project, index) in projects" :key="index">
            <ProjectItem :project="project" />
          </slide>
          <!--item end-->
        </carousel>
    </div>
    <!--all projects start--->
    <div class="wrapper">
      <div class="projects__line">
        <div class="projects__line-center">
          <a href="#!" class="projects__line-link">Смотреть все проекты</a>
        </div>
      </div>
    </div>
    <!--all projects end--->
  </section>
</template>
<script>
import { Carousel, Slide } from 'vue-carousel';
import ProjectItem from './ProjectItem.vue';

export default {
  name: 'Projects',
  components: { Carousel, Slide, ProjectItem },
  data() {
    return {
      projects: [
        {
          title: 'Сбор средств для постойки школ в Индонезии',
          description: 'Диана — единственная и долгожданная! У нее сложный порок сердца и ей нужно провести еще одну операцию Фонтена',
          poster: 'image-1.jpg',
          logo: 'logo-1.svg',
          city: 'Омск',
          counter: {
            percent: 37,
            image: '37-percent.svg'
          },
          showBtn: false,
        },
        {
          title: 'Поможем дедушке построить пекарню',
          description: 'Диана — единственная и долгожданная! У нее сложный порок сердца и ей нужно провести еще одну операцию Фонтена',
          poster: 'image-2.jpg',
          logo: 'logo-2.svg',
          city: 'Омск',
          counter: {
            percent: 84,
            image: '84-percent.svg'
          },
          showBtn: true,
        },
        {
          title: 'Сбор для Арифулиной Дианы',
          description: 'Диана — единственная и долгожданная! У нее сложный порок сердца и ей нужно провести еще одну операцию Фонтена',
          poster: 'image-3.jpg',
          logo: 'logo-2.svg',
          city: 'Омск',
          counter: {
            percent: 10,
            image: '10-percent.svg'
          },
          showBtn: false,
        },
      ]
    }
  }
}
</script>
