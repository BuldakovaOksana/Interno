<template>
  <section class="banner center">
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.banner {
  background-image: url("@/assets/img/blogDetailsBanner.png");
  height: 351px;
  margin-top: 45px;
}

/* Блок для планшета */

@media (max-width: 1200px) {
  .center {
    padding-left: calc(50% - 370px);
    padding-right: calc(50% - 370px);
  }

  .banner {
    height: 280px;
    background-position: right bottom;
  }
}

/* Блок для мобильной версии */

@media (min-width: 320px) and (max-width: 767px) {
  .center {
    padding-left: calc(50% - 152px);
    padding-right: calc(50% - 152px);
  }

  .banner {
    margin-top: 20px;
    height: 180px;
    background-position: 70% 80%;
  }
}
</style>