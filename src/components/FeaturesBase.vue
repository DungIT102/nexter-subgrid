<script setup></script>

<template>
  <section class="features">
    <div class="feature">
      <svg class="feature__icon">
        <use href="@/assets/img/sprite.svg#icon-global"></use>
      </svg>
      <h4 class="heading-4 heading-4--dark">World's best luxury homes</h4>
      <p class="feature__text">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Tenetur distinctio necessitatibus pariatur
        voluptatibus
      </p>
    </div>
    <div class="feature">
      <svg class="feature__icon">
        <use href="@/assets/img/sprite.svg#icon-trophy"></use>
      </svg>
      <h4 class="heading-4 heading-4--dark">Only the best properties</h4>
      <p class="feature__text">
        Voluptatum mollitia quae. Vero ipsum sapiente molestias accusamus rerum sed a eligendi aut quia.
      </p>
    </div>
    <div class="feature">
      <svg class="feature__icon">
        <use href="@/assets/img/sprite.svg#icon-map-pin"></use>
      </svg>
      <h4 class="heading-4 heading-4--dark">All homes in top locations</h4>
      <p class="feature__text">Tenetur distinctio necessitatibus pariatur voluptatibus quidem consequatur harum.</p>
    </div>
    <div class="feature">
      <svg class="feature__icon">
        <use href="@/assets/img/sprite.svg#icon-key"></use>
      </svg>
      <h4 class="heading-4 heading-4--dark">New home in one week</h4>
      <p class="feature__text">
        Vero ipsum sapiente molestias accusamus rerum. Lorem, ipsum dolor sit amet consectetur adipisicing elit.
      </p>
    </div>
    <div class="feature">
      <svg class="feature__icon">
        <use href="@/assets/img/sprite.svg#icon-presentation"></use>
      </svg>
      <h4 class="heading-4 heading-4--dark">Top 1% realtors</h4>
      <p class="feature__text">
        Quidem consequatur harum, voluptatum mollitia quae. Tenetur distinctio necessitatibus pariatur voluptatibus.
      </p>
    </div>
    <div class="feature">
      <svg class="feature__icon">
        <use href="@/assets/img/sprite.svg#icon-lock"></use>
      </svg>
      <h4 class="heading-4 heading-4--dark">Secure payments on nexter</h4>
      <p class="feature__text">Pariatur voluptatibus quidem consequatur harum, voluptatum mollitia quae.</p>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  .features {
    margin: 15rem 0;
    grid-column: center-start / center-end;

    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(25rem, 1fr));
    grid-gap: 6rem;
    align-items: start;

    @media only screen and (max-width: $bp-small) {
      grid-template-columns: 1fr;
    }
  }

  .feature {
    display: grid;
    grid-template-columns: min-content 1fr;
    grid-row-gap: 1.5rem;
    grid-column-gap: 2.5rem;

    width: auto;
    margin-bottom: 0;

    &__icon {
      width: 4.5rem;
      height: 4.5rem;
      fill: $color-primary;
      grid-row: 1 / span 2;

      transform: translateY(-1rem);
    }

    &__text {
      font-size: 1.7rem;
    }
  }

  /* Heading */
  .heading-4 {
    font-family: $font-display;
    font-size: 1.9rem;
    font-weight: 400;

    &--dark {
      color: $color-grey-dark-1;
    }
  }
</style>
