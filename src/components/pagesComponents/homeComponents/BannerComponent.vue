<template>
  <section class="banner center">
    <div class="banner__background">
      <div class="banner__content">
        <h1 class="banner__content__title">Let Your Home Be Unique</h1>
        <p class="banner__content__text">
          There are many variations of the passages of lorem Ipsum
          fromavailable, majority.
        </p>
        <a href="#" class="banner__content__btn">Get Started
          <svg width="18.000000" height="16.000000" viewBox="0 0 18 16" fill="none" xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink">
            <desc>Created with Pixso.</desc>
            <defs />
            <path id="Vector" d="M1 7.43L14.72 7.29M9.61 0.91L16.14 7.43L9.48 14.08" stroke="#CDA274"
              stroke-opacity="1.000000" stroke-width="2.000000" stroke-linejoin="round" />
          </svg>
        </a>
      </div>
    </div>


  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import "@/style/vars.scss";

.banner {
  margin-top: 57px;

  &__background {
    background-image: url("@/assets/img/homeBanner.jpeg");
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    height: 758px;
    border-radius: 70px;
    display: flex;
    align-items: center;
  }

  &__content {
    max-width: 434px;
    margin-left: 52px;
    display: flex;
    flex-direction: column;
    gap: 20px;

    &__title {
      color: $colorTitles;
      font-family: $fontTitles;
      font-size: 65px;
      font-weight: 400;
      line-height: 125%;
      letter-spacing: 0%;
      text-align: left;
    }

    &__text {
      color: $colorText;
      font-family: $fontText;
      font-size: 22px;
      font-weight: 400;
      line-height: 150%;
      letter-spacing: 1%;
      text-align: left;
    }

    &__btn {
      color: rgb(255, 255, 255);
      font-family: $fontText;
      font-size: 18px;
      font-weight: 600;
      line-height: 125%;
      letter-spacing: 2%;
      text-align: center;
      border-radius: 18px;
      background: #292f36;
      width: 220.14px;
      height: 75px;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 4px;

      &:hover {
        color: #292f36;
        background: rgb(255, 255, 255);
      }
    }
  }
}

/* Блок для планшета */

@media (max-width: 1200px) {
  .center {
    padding-left: calc(50% - 370px);
    padding-right: calc(50% - 370px);
  }

  .banner {
    margin-top: 40px;

    &__background {
      height: 550px;
    }

    &__content {

      max-width: 380px;

      &__title {
        font-size: 50px;
      }

      &__text {
        font-size: 18px;

      }

      &__btn {
        font-size: 16px;
        width: 180px;
        height: 60px;
      }
    }
  }
}

/* Блок для мобильной версии */

@media (min-width: 320px) and (max-width: 767px) {
  .center {
    padding-left: calc(50% - 152px);
    padding-right: calc(50% - 152px);
  }

  .banner {
    margin-left: 3px;
    margin-right: 2px;
    margin-top: 28px;

    &__background {
      height: 500px;
      background-position: 40% center;
    }

    &__content {
      gap: 35px;
      margin-left: 0;
      align-items: center;

      &__title {
        font-size: 40px;
        text-align: center;
      }

      &__text {
        max-width: 270px;
        font-size: 16px;
        text-align: center;
      }
    }
  }
}
</style>