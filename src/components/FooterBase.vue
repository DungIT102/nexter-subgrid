<script setup></script>

<template>
  <footer class="footer">
    <ul class="nav">
      <li class="nav__item"><a href="#" class="nav__link">Find your dream home</a></li>
      <li class="nav__item"><a href="#" class="nav__link">Request proposal</a></li>
      <li class="nav__item"><a href="#" class="nav__link">Download home planner</a></li>
      <li class="nav__item"><a href="#" class="nav__link">Contact us</a></li>
      <li class="nav__item"><a href="#" class="nav__link">Submit your property</a></li>
      <li class="nav__item"><a href="#" class="nav__link">Come work with us!</a></li>
    </ul>
    <p class="copyright">&copy; Copyright 2017 by Le Dung</p>
  </footer>
</template>

<style lang="scss" scoped>
  .footer {
    padding: 8rem;
    grid-column: full-start / full-end;
    background-color: $color-secondary;
  }

  .nav {
    list-style: none;

    display: grid;
    align-items: center;
    grid-template-columns: repeat(auto-fit, minmax(15rem, 1fr));
    grid-gap: 2rem;

    &__link:link,
    &__link:visited {
      display: block;
      padding: 1.5rem;

      font-family: $font-display;
      font-weight: 500;
      font-size: 1rem;
      text-align: center;
      text-transform: uppercase;
      text-decoration: none;

      color: $color-white;
      transition: all 0.2s;
    }

    &__link:hover,
    &__link:active {
      background-color: rgba($color-white, 0.05);
      transform: translateY(-3px);
    }
  }

  .copyright {
    width: 70%;
    margin: 10rem auto 0 auto;

    font-size: 1.4rem;
    font-weight: 500;
    text-align: center;
    color: $color-grey-light-2;
  }
</style>
