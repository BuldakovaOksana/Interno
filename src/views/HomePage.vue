<template>
  <HeaderComponent />
  <BannerComponent />
  <ProjectComponent />
  <CounterComponent />
  <section class="blog center">
    <h2 class="blog__title">Articles & News</h2>
    <p class="blog__text">
      It is a long established fact that a reader will be distracted by the of
      readable content of a page when lookings at its layouts the points of
      using.
    </p>
    <div class="blog__contener">
      <ArticlesComponent :itemPerPage="3" />
    </div>
  </section>
  <FooterComponent />
</template>

<script>
import HeaderComponent from '../components/HeaderComponent.vue';
import BannerComponent from '../components/pagesComponents/homeComponents/BannerComponent.vue';
import ProjectComponent from '../components/pagesComponents/homeComponents/ProjectComponent.vue';
import CounterComponent from '../components/pagesComponents/homeComponents/CounterComponent.vue';
import ArticlesComponent from '../components/ArticlesComponent.vue';
import FooterComponent from '../components/FooterComponent.vue';

export default {
  components: {
    HeaderComponent,
    BannerComponent,
    ProjectComponent,
    CounterComponent,
    ArticlesComponent,
    FooterComponent,
  }
}
</script>

<style lang="scss" scoped>
@import "@/style/vars.scss";

.blog {
  margin-top: 96px;
  display: flex;
  flex-direction: column;
  align-items: center;

  &__title {
    margin-bottom: 12px;
    color: $colorTitles;
    font-family: $fontTitles;
    font-size: 50px;
    font-weight: 400;
    line-height: 125%;
    letter-spacing: 2%;
    text-align: center;
  }

  &__text {
    margin-bottom: 52px;
    max-width: 805px;
    color: $colorText;
    font-family: $fontText;
    font-size: 22px;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 1%;
    text-align: center;
  }

  &__contener {
    margin-bottom: 96px;
  }
}

/* Блок для планшета */

@media (max-width: 1200px) {
  .center {
    padding-left: calc(50% - 370px);
    padding-right: calc(50% - 370px);
  }

  .blog {
    margin-top: 70px;

    &__title {
      font-size: 40px;
    }

    &__text {
      font-size: 20px;
      max-width: 700px;
    }

    &__contener {
      margin-bottom: 70px;
    }
  }
}

/* Блок для мобильной версии */

@media (min-width: 320px) and (max-width: 767px) {
  .center {
    padding-left: calc(50% - 152px);
    padding-right: calc(50% - 152px);
  }

  .blog {
    margin-top: 30px;

    &__title {
      font-size: 35px;
    }

    &__text {
      font-size: 18px;
      max-width: 300px;
      margin-bottom: 30px;
    }

    &__contener {
      margin-bottom: 50px;
    }
  }
}
</style>