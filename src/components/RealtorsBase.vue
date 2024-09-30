<script setup></script>

<template>
  <section class="realtors">
    <h3 class="heading-3">Top 3 Realtors</h3>
    <div class="realtors__list">
      <img src="@/assets/img/realtor-1.jpeg" alt="Realtor 1" class="realtors__img" />
      <div class="realtors__details">
        <h4 class="heading-4 heading-4--light">Erik Feinman</h4>
        <p class="realtors__sold">245 houses sold</p>
      </div>

      <img src="@/assets/img/realtor-2.jpeg" alt="Realtor 2" class="realtors__img" />
      <div class="realtors__details">
        <h4 class="heading-4 heading-4--light">Kim Brown</h4>
        <p class="realtors__sold">212 houses sold</p>
      </div>

      <img src="@/assets/img/realtor-3.jpeg" alt="Realtor 3" class="realtors__img" />
      <div class="realtors__details">
        <h4 class="heading-4 heading-4--light">Toby Ramsey</h4>
        <p class="realtors__sold">198 houses sold</p>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  .realtors {
    padding: 3rem;
    grid-column: col-start 7 / full-end;
    background-color: $color-secondary;

    display: grid;
    grid-row-gap: 2rem;
    align-content: center;
    justify-content: center;

    @media only screen and (max-width: $bp-medium) {
      grid-column: 1 / -1;
    }

    &__list {
      display: grid;
      grid-template-columns: min-content max-content;
      grid-column-gap: 2rem;
      grid-row-gap: 5vh;
      align-items: center;

      @media only screen and (max-width: $bp-medium) {
        grid-template-columns: repeat(3, min-content max-content);
      }

      @media only screen and (max-width: $bp-small) {
        grid-template-columns: min-content max-content;
      }
    }

    &__img {
      display: block;
      width: 7rem;
      border-radius: 50%;
    }

    &__sold {
      margin-top: -3px;

      font-weight: 600;
      color: $color-grey-light-2;
      text-transform: uppercase;
    }
  }

  /* Heading */
  .heading-3 {
    font-family: $font-display;
    font-size: 1.6rem;
    font-weight: 400;

    color: $color-primary;
    text-transform: uppercase;
  }

  .heading-4 {
    font-family: $font-display;
    font-size: 1.9rem;
    font-weight: 400;

    &--light {
      color: $color-grey-light-1;
    }
  }
</style>
