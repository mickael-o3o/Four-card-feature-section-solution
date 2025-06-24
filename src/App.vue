<template>
  <header class="p-header">
    <h1 class="p-header__heading">
      <span class="p-header__title">Reliable, efficient delivery </span>
      <span class="p-header__title p-header__title--bold">Powered by Technology</span>
    </h1>
    <p class="p-header__description">
      Our Artificial Intelligence powered tools use millions of project data points to ensure that
      your project is successful
    </p>
  </header>
  <main class="p-main">
    <article class="c-card c-card--two-rows">
      <header class="c-card__heading">
        <h2 class="c-card__title">Supervisor</h2>
      </header>
      <div class="c-card__body">
        <p class="c-card__description">Monitors activity to identify project roadblocks</p>
        <img
          class="c-card__icon"
          width="64px"
          height="64px"
          src="./assets/svgs/icon-supervisor.svg"
          alt=""
        />
      </div>
    </article>

    <article class="c-card c-card--red">
      <header class="c-card__heading">
        <h2 class="c-card__title">Team Builder</h2>
      </header>
      <div class="c-card__body">
        <p class="c-card__description">
          Scans our talent network to create the optimal team for your project
        </p>
        <img
          class="c-card__icon"
          width="64px"
          height="64px"
          src="./assets/svgs/icon-team-builder.svg"
          alt=""
        />
      </div>
    </article>

    <article class="c-card c-card--orange">
      <header class="c-card__heading">
        <h2 class="c-card__title">Karma</h2>
      </header>
      <div class="c-card__body">
        <p class="c-card__description">Regularly evaluates our talent to ensure quality</p>
        <img
          class="c-card__icon"
          width="64px"
          height="64px"
          src="./assets/svgs/icon-karma.svg"
          alt=""
        />
      </div>
    </article>

    <article class="c-card c-card--two-rows-two c-card--blue">
      <header class="c-card__heading">
        <h2 class="c-card__title">Calculator</h2>
      </header>
      <div class="c-card__body">
        <p class="c-card__description">
          Uses data from past projects to provide better delivery estimates
        </p>
        <img
          class="c-card__icon"
          width="64px"
          height="64px"
          src="./assets/svgs/icon-calculator.svg"
          alt=""
        />
      </div>
    </article>
  </main>
  <footer class="p-footer">
    <p class="attribution">
      Challenge by
      <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>.
      Coded by
      <a href="https://github.com/mickael-o3o/Four-card-feature-section-solution.git">mickael-o3o</a
      >.
    </p>
  </footer>
</template>

<style lang="scss">
@use './assets/utils/functions.scss' as *;

.p-header {
  margin-block-start: 1rem;
  padding: calc-rem(34) calc-rem(36);
  display: flex;
  flex-direction: column;
  text-align: center;
  gap: calc-rem(20);
  inline-size: clamp(10rem, 100%, calc-rem(600));
  margin-block-start: clamp(0rem, 0rem + 6vw, calc-rem(70));

  &__heading {
    line-height: clamp(110%, 110% + 30vw, 150%);
    letter-spacing: calc-rem(0.2);
  }

  &__title {
    font : {
      family: var(--font-family-light);
      size: clamp(calc-rem(24), 0rem + 4vw, calc-rem(36));
    }

    &--bold {
      font-family: var(--font-family-semi-bold);
    }
  }

  &__description {
    letter-spacing: calc-rem(0.1);
  }
}

.p-main {
  padding: clamp(calc-rem(18), 1rem + 1.8vw, calc-rem(38)) calc-rem(30);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: calc-rem(30);
  inline-size: clamp(calc-rem(130), 100%, calc-rem(1200));

  @media (min-width: 80rem) {
    display: grid;
    grid-template: auto auto / auto auto auto;
    place-items: center;
    column-gap: 0;
  }
}

.c-card {
  background-color: var(--color-neutral-white);
  box-shadow: 0 calc-rem(15) calc-rem(15)
    color-mix(in srgb, var(--color-neutral-grey-400) 20%, transparent);
  overflow: hidden;
  border-radius: 0.5rem;
  padding: calc-rem(32);
  position: relative;
  inline-size: 100%;

  &::before {
    content: '';
    position: absolute;
    inset-block-start: 0;
    inset-inline-start: 0;
    inline-size: 100%;
    block-size: 0.25rem;
    background-color: var(--color-primary-cyan);
  }

  @media (min-width: 25rem) {
    max-inline-size: calc-rem(350);
  }

  &__title {
    font-size: calc-rem(20);
    font-family: var(--font-family-semi-bold);
    color: var(--color-neutral-grey-500);
  }

  &__body {
    display: grid;
    row-gap: calc(32);
    padding-block-end: calc-rem(16);
  }

  &__description {
    margin-block-start: calc-rem(6);
    font-size: calc-rem(13);
    line-height: 1.6;
    letter-spacing: calc-rem(0.2);
  }

  &__icon {
    display: block;
    place-self: end;
    margin-block-start: 32px;
  }
}

.c-card {
  &--two-rows {
    grid-row: 1 / span 2;
  }

  &--red {
    &::before {
      background-color: var(--color-primary-red);
    }
  }

  &--orange {
    &::before {
      background-color: var(--color-primary-orange);
    }
  }

  &--blue {
    &::before {
      background-color: var(--color-primary-blue);
    }
  }
}

.c-card--two-rows-two {
  grid-row: 1 / span 2;
  grid-column: 3 / 4;
}

.p-footer {
  margin: 1rem;
  margin-block-start: 0;
}

.attribution {
  border: 0.0625rem solid var(--color-neutral-grey-500);
  padding: calc-rem(12);
  margin: auto;
  font-family: monospace;

  a {
    color: var(--color-primary-blue);
  }
}
</style>
