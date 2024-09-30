<script setup></script>

<template>
  <header class="header">
    <img src="@/assets/img/logo.png" alt="Nexter Logo" class="header__logo" />
    <h3 class="heading-3">Your own home</h3>
    <h1 class="heading-1">The ultimate personal freedom</h1>
    <button class="btn header__btn">View our properties</button>
    <div class="header__seenon-text">Seen on</div>
    <div class="header__seenon-logos">
      <img src="@/assets/img/logo-bbc.png" alt="Seen on logo 1" />
      <img src="@/assets/img/logo-forbes.png" alt="Seen on logo 2" />
      <img src="@/assets/img/logo-techcrunch.png" alt="Seen on logo 3" />
      <img src="@/assets/img/logo-bi.png" alt="Seen on logo 4" />
    </div>
  </header>
</template>

<style lang="scss" scoped>
  .header {
    padding: 8rem;
    padding-top: 4rem;
    grid-column: full-start / col-end 6;

    background-image: linear-gradient(rgba($color-secondary, 0.93), rgba($color-secondary, 0.93)),
      url('@/assets/img/hero.jpeg');
    background-size: cover;
    background-position: center;
    background-color: $color-grey-dark-1;

    display: grid;
    grid-template-rows: 1fr min-content minmax(6rem, min-content) 1fr;
    grid-template-columns: minmax(min-content, max-content);
    grid-row-gap: 1.5rem;
    justify-content: center;

    @media only screen and (max-width: $bp-medium) {
      grid-column: 1 / -1;
    }

    @media only screen and (max-width: $bp-small) {
      padding: 5rem;
    }

    &__logo {
      height: 3rem;
      justify-self: center;
    }

    &__btn {
      align-self: start;
      justify-self: start;
    }

    &__seenon-text {
      display: grid;
      grid-template-columns: 1fr max-content 1fr;
      align-items: center;
      grid-column-gap: 1.5rem;

      font-size: 1.6rem;
      color: $color-grey-light-2;

      &::before,
      &::after {
        content: '';
        height: 1px;
        background-color: currentColor;
      }
    }

    &__seenon-logos {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      grid-column-gap: 3rem;
      justify-items: center;
      align-items: center;

      img {
        max-height: 2.5rem;
        max-width: 100%;
        filter: brightness(70%);
      }
    }
  }

  /* Heading */
  .heading-1 {
    font-family: $font-display;
    font-size: 4.5rem;
    font-weight: 400;
    line-height: 1;

    color: $color-grey-light-1;
  }

  .heading-3 {
    font-family: $font-display;
    font-size: 1.6rem;
    font-weight: 400;

    color: $color-primary;
    text-transform: uppercase;
  }

  /* Button */
  .btn {
    padding: 1.8rem 3rem;
    border: none;
    border-radius: 0;

    font-family: $font-display; /* Because the font-family seem like effect to the text of the button */
    font-size: 1.5rem;
    text-transform: uppercase;

    color: $color-white;
    background-color: $color-primary;
    cursor: pointer;
    transition: all 0.2s;

    &:hover {
      background-color: $color-primary-dark;
    }
  }
</style>
