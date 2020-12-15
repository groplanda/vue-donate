<template>
    <div class="projects__slider-item">
      <!--image start-->
      <div class="projects__slider-item-pic">
        <img
          class="projects__slider-item-thumb"
          :src="require(`@/assets/images/${project.poster}`)"
          :alt="project.title"
        />
        <!--logo projects start-->
        <div class="projects__slider-item-logo">
          <img class="projects__slider-item-logo__thumb"
            :src="require(`@/assets/images/${project.logo}`)"
            alt="logo"
          />
        </div>
        <!--logo projects end-->
        <div class="projects__slider-item-city">{{ project.city }}</div>
      </div>
      <!--image end-->
      <p class="projects__slider-item-title">{{ project.title }}</p>
      <p class="projects__slider-item-description">
        {{ project.description }}
      </p>
      <!--projecrs info start-->
      <div class="projects__slider-item-info">
        <div class="projects__slider-item-info__counter">
          <img class="percent-thumb"
            :class="fuelClass"
            :src="require(`@/assets/images/icon/${project.counter.image}`)"
            :alt="project.counter.percent"
          />
          <span class="percent">{{ project.counter.percent }}%</span>
        </div>
        <div class="projects__slider-item-info__content">
          <p class="projects__slider-item-info__title">необходимо собрать</p>
          <p class="projects__slider-item-info__description"><span>45 194</span> из 1 000 000 RUB</p>
        </div>
        <div class="projects__slider-item-info__end">
          <p class="projects__slider-item-info__title">конец</p>
          <p class="projects__slider-item-info__description">Завтра</p>
        </div>
      </div>
      <!--projecrs info end-->
      <!--tags start-->
      <ul class="projects__slider-item-tags">
        <li class="projects__slider-item-single-tag">помощь нуждающимся</li>
        <li class="projects__slider-item-single-tag">закят</li>
      </ul>
      <!--tags end-->
      <button v-if="project.showBtn" class="projects__slider-button">
        <img src="@/assets/images/icon/hand.svg" alt="hand" />
      </button>
    </div>
</template>
<script>

export default {
  name: 'ProjectItem',
  props: {
    project: {
      type: Object,
      required: true
    }
  },
  computed: {
    fuelClass() {
      return {
        fuel: this.project.counter.percent > 75
      }
    }
  }
}
</script>