<script setup></script>

<template>
  <div class="story__pictures">
    <img src="@/assets/img/story-1.jpeg" alt="Couple with new house" class="story__img--1" />
    <img src="@/assets/img/story-2.jpeg" alt="New house" class="story__img--2" />
  </div>

  <div class="story__content">
    <h3 class="heading-3 mb-sm">Happy Customers</h3>
    <h2 class="heading-2 heading-2--dark mb-md">&ldquo;The best decision of our lives&rdquo;</h2>
    <p class="story__text">
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Tenetur distinctio necessitatibus pariatur voluptatibus.
      Quidem consequatur harum volupta!
    </p>
    <button class="btn">Find your own home</button>
  </div>
</template>

<style lang="scss" scoped>
  .story {
    &__pictures {
      grid-column: full-start / col-end 4;
      background-image: linear-gradient(rgba($color-primary, 0.5), rgba($color-primary, 0.5)),
        url('@/assets/img/back.jpg');
      background-size: cover;
      background-color: $color-primary;

      display: grid;
      grid-template-rows: repeat(6, 1fr);
      grid-template-columns: repeat(6, 1fr);
      align-items: center;

      @media only screen and (max-width: $bp-medium) {
        grid-column: 1 / -1;
        padding: 6rem;
      }
    }

    &__img--1 {
      width: 100%;
      grid-row: 2 / 6;
      grid-column: 2 / 6;
      box-shadow: 0 2rem 5rem rgba(#000, 0.1);

      @media only screen and (max-width: $bp-medium) {
        grid-column: 1 / 5;
        grid-row: 1 / -1;
      }
    }

    &__img--2 {
      width: 115%;
      grid-row: 4 / 6;
      grid-column: 4 / 7;

      z-index: 20;
      box-shadow: 0 2rem 5rem rgba(#000, 0.2);

      @media only screen and (max-width: $bp-medium) {
        grid-row: 1 / -1;
        width: 100%;
      }
    }

    &__content {
      grid-column: col-start 5 / full-end;
      padding: 6rem 8vw;
      background-color: $color-grey-light-1;

      display: grid;
      align-content: center;
      justify-items: start;

      @media only screen and (max-width: $bp-medium) {
        grid-row: 5 / 6;
        grid-column: 1 / -1;
      }
    }

    &__text {
      font-style: italic;
      font-size: 1.5rem;
      margin-bottom: 4rem;
    }
  }

  /* Heading */
  .heading-2 {
    font-family: $font-display;
    font-size: 4rem;
    font-weight: 400;

    font-style: italic;
    line-height: 1;

    &--dark {
      color: $color-grey-dark-1;
    }
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

    font-family: $font-display;
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

  /* Some custom styles */
  .mb-sm {
    margin-bottom: 2rem;
  }

  .mb-md {
    margin-bottom: 3rem;
  }
</style>
