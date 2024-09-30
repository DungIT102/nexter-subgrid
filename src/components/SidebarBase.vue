<script setup></script>

<template>
  <div class="sidebar">
    <button class="nav-btn"></button>
  </div>
</template>

<style lang="scss" scoped>
  .sidebar {
    grid-row: 1/ -1;
    grid-column: 1 / 2;
    background-color: $color-primary;

    display: flex;
    justify-content: center;

    @media only screen and (max-width: $bp-largest) {
      grid-row: 1 / 2;
      grid-column: 1 / -1;
      justify-content: flex-end;
      align-items: center;
    }
  }

  .nav-btn {
    width: 4.5rem;
    height: 2px;
    margin-top: 4rem;

    border: none;
    border-radius: 0;
    background-color: $color-white;

    &::before,
    &::after {
      content: '';
      display: block;
      width: 4.5rem;
      height: 2px;

      background-color: $color-white;
      transition: all 0.2s;
    }

    &::before {
      transform: translateY(-1.5rem);
    }

    &::after {
      transform: translateY(1.3rem);
    }

    @media only screen and (max-width: $bp-largest) {
      margin-top: 0;
      margin-right: 3rem;

      &::before {
        transform: translateY(-1.2rem);
      }

      &::after {
        transform: translateY(1rem);
      }
    }
  }
</style>
