<template>
  <header class="header center">
    <router-link to="/" class="header__logo">
      <img src="@/assets/img/Logo.png" alt="logo" />
      <p>Interno</p>
    </router-link>
    <nav class="header__nav">
      <router-link class="header__nav__link" to="/">Home</router-link>
      <router-link class="header__nav__link" to="/Project">Project</router-link>
      <router-link class="header__nav__link" to="/Blog">Blog</router-link>
    </nav>
  </header>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
@import "@/style/vars.scss";

.header {
  margin-top: 44px;
  display: flex;
  justify-content: space-between;


  &__logo {
    display: flex;
    align-items: center;
    gap: 8px;
    color: $colorTitles;
    font-family: $fontTitles;
    font-size: 40px;
    font-weight: 400;
    line-height: 125%;
    letter-spacing: 0%;
    text-align: left;
  }

  &__nav {

    display: flex;
    gap: 48px;
    align-items: center;

    &__link {
      color: $colorText;
      font-family: $fontText;
      font-size: 20px;
      font-weight: 400;
      line-height: 125%;
      letter-spacing: 0%;
      text-align: center;
      display: block;

      &:hover {
        color: #292F36;
        text-shadow: 0.5px 0.5px #c2c4c7;
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
}

/* Блок для мобильной версии */

@media (min-width: 320px) and (max-width: 767px) {
  .center {
    padding-left: calc(50% - 152px);
    padding-right: calc(50% - 152px);
  }

  .header {
    margin-top: 10px;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px;
  }
}
</style>