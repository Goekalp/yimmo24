<template>
  <div id="app">
    <nav class="navbar">
      <router-link class="navbar__brand" to="/">Home</router-link>
      <ul class="navbar__links">
        <li class="navbar__links__item">
          <router-link to="/" class="navbar__links__item__a">Home</router-link>
        </li>
        <li class="navbar__links__item">
          <router-link to="/" class="navbar__links__item__a">Home</router-link>
        </li>
        <li class="navbar__links__item">
          <router-link to="/" class="navbar__links__item__a">Home</router-link>
        </li>
        <li class="navbar__links__item">
          <router-link to="/" class="navbar__links__item__a">Home</router-link>
        </li>
        <li class="navbar__links__item">
          <router-link to="/" class="navbar__links__item--highlight"
            >Contact</router-link
          >
        </li>
      </ul>
    </nav>

    <router-view />
  </div>
</template>

<style lang="scss">
:root {
  --color-primary: #ff731d;
  --color-text: #2c3e50;
  --color-white-1: #ffffff;
}

body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  height: 4.5rem;
  background: #fff7e9;
  padding: 0 2rem;
  box-sizing: border-box;

  &__links {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    width: 40%;
    height: 100%;

    &__item {
      display: inline-block;
      width: 10rem;
      margin: 3rem;

      &__a {
        color: var(--color-text);
        font-size: 1rem;
        font-weight: bold;
        text-decoration: underline 0.1em rgba($color: #000000, $alpha: 0);
        text-underline-offset: 0.1em;
        transition: 0.5s all ease;
      }
      &__a:visited {
        color: var(--color-text);
      }
      &__a:hover {
        color: var(--color-primary);
        text-decoration-color: rgba($color: var(--color-primary), $alpha: 1);
      }

      &--highlight {
        background: #5f9df7;
        margin-left: 10px;
        padding: 15px 40px;

        border-radius: 10px;
        transition: 0.5s background-color ease;
        cursor: pointer;
        color: var(--color-white-1);
        font-size: 1rem;
        font-weight: bold;
        text-decoration: none;
      }
      &--highlight:hover {
        background-color: #1746a2;
      }
    }
  }

  &__brand {
    color: var(--color-text);
    font-size: 3em;
    text-decoration: none;
    font-family: Georgia, "Times New Roman", Times, serif;
    font-weight: bold;
    margin: 0 3rem;
  }
  &__brand:visited {
    color: var(--color-text);
    text-decoration: none;
  }
}
</style>
