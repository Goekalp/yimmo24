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
          <router-link to="/" class="navbar__links__item__a">Home</router-link>
        </li>
      </ul>
    </nav>

    <router-view />
  </div>
</template>

<style lang="scss">
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
  height: 5rem;
  background: orange;
  padding: 0 10%;
  box-sizing: border-box;

  &__links {
    list-style-type: none;
    margin: 0;
    padding: 0;

    &__item {
      display: inline-block;
      padding: 2rem;

      &__a {
        color: #ffffff;
        font-size: 1rem;
        font-weight: bold;
        text-decoration: underline 0.1em rgba($color: #000000, $alpha: 0);
        text-underline-offset: 0.1em;
        transition: 2s all ease;
      }
      &__a:visited {
        color: #ffffff;
      }
      &__a:hover {
        color: #ff0000;
        text-decoration-color: rgba($color: #ff0000, $alpha: 1);
      }
    }
  }
}
</style>
