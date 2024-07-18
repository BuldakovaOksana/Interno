<template>
  <HeaderComponent />
  <BannerComponent />
  <LastPostComponent />
  <section class="articlesNews center">
    <h2 class="articlesNews__title">Articles & News</h2>
    <ArticlesComponent :itemPerPage="6" />
  </section>
  <PaginationComponent />
  <FooterComponent />
</template>

<script>
import HeaderComponent from '@/components/HeaderComponent.vue'
import BannerComponent from '@/components/pagesComponents/blogComponents/BannerComponent.vue'
import LastPostComponent from '@/components/pagesComponents/blogComponents/LastPostComponent.vue'
import ArticlesComponent from '@/components/ArticlesComponent.vue'
import PaginationComponent from '@/components/pagesComponents/blogComponents/PaginationComponent.vue'
import FooterComponent from '@/components/FooterComponent.vue'
export default {
  components: {
    HeaderComponent,
    BannerComponent,
    LastPostComponent,
    ArticlesComponent,
    PaginationComponent,
    FooterComponent,
  }
}
</script>

<style lang="scss" scoped>
@import "@/style/vars.scss";

.articlesNews {
  margin-top: 150px;

  &__title {
    margin-bottom: 30px;
    color: $colorTitles;
    font-family: $fontTitles;
    font-size: 50px;
    font-weight: 400;
    line-height: 125%;
    letter-spacing: 2%;
    text-align: left;
  }
}

/* Блок для планшета */
@media (max-width: 1200px) {
  .center {
    padding-left: calc(50% - 370px);
    padding-right: calc(50% - 370px);
  }

  .articlesNews {
    margin-top: 100px;

    &__title {
      margin-bottom: 30px;
      font-size: 40px;
    }
  }
}

/* Блок для мобильной версии */

@media (min-width: 320px) and (max-width: 767px) {
  .center {
    padding-left: calc(50% - 152px);
    padding-right: calc(50% - 152px);
  }

  .articlesNews {
    margin-top: 50px;

    &__title {
      margin-bottom: 30px;
      font-size: 30px;
      text-align: center;
    }
  }
}
</style>