<template>
  <div class="container--col">
    <div class="landing container--row">
      <div class="grid">
        <div class="grid__item container--col">
          <h1 class="header-1">Überschrift</h1>
          <h2 class="header-2">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ex ut quae
            perspiciatis in explicabo unde cumque nihil inventore necessitatibus
            aperiam adipisci, accusamus molestias, porro maxime ratione. Sunt
            inventore commodi eveniet.
          </h2>
          <div class="search container--row">
            <input placeholder="Search" class="search__input" type="text" />
            <button class="search__button">Search</button>
          </div>
        </div>
        <div class="frame">
          <img
            class="frame__img"
            src="https://www.gussek-haus.de/fileadmin/user_upload/Fertighaeuser-Haeuser/Kundenhaeuser/Luxushaus/Cannstatt/luxushaus-cannstatt-001-zeltdach-erker.jpg"
            alt=""
          />
        </div>
      </div>
    </div>
    <div class="container--col carousel">
      <h1 class="header-1" black>Hier ein paar Karten</h1>
      <div class="card-group">
        <b-card
          title="Title"
          img-src="https://picsum.photos/300/300/?image=41"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            This is a wider card with supporting text below as a natural lead-in
            to additional content. This content is a little bit longer.
          </b-card-text>
          <template #footer>
            <small class="text-muted">Last updated 3 mins ago</small>
          </template>
        </b-card>

        <b-card
          title="Title"
          img-src="https://picsum.photos/300/300/?image=41"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            This card has supporting text below as a natural lead-in to
            additional content.
          </b-card-text>
          <template #footer>
            <small class="text-muted">Last updated 3 mins ago</small>
          </template>
        </b-card>

        <b-card
          title="Title"
          img-src="https://picsum.photos/300/300/?image=41"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            This is a wider card with supporting text below as a natural lead-in
            to additional content. This card has even longer content than the
            first to show that equal height action.
          </b-card-text>
          <template #footer>
            <small class="text-muted">Last updated 3 mins ago</small>
          </template>
        </b-card>
      </div>
    </div>
    <div class="container--col footer">
      <p>Footer</p>
    </div>
  </div>
</template>
<script>
import { BCard, BCardText } from "bootstrap-vue";

export default {
  components: {
    "b-card": BCard,
    // "b-card-group": BCardGroup,
    "b-card-text": BCardText,
  },
};
</script>
<style lang="scss" scoped>
.container--col {
  display: flex;
  flex-direction: column;
}
.container--row {
  display: flex;
  flex-direction: row;
}
.grid {
  width: 100%;
  display: grid;
  grid-template-columns: 50% 50%;

  &__item {
    margin: 0 5em;
  }
}
.header-1 {
  align-self: flex-start;
  color: var(--color-white-1);
  font-size: 40px;
  font-weight: bold;
  margin: 1em 0;
}
.header-2 {
  align-self: flex-start;
  color: var(--color-white-2);
  font-size: 15px;
  margin: 0.5em;
  text-align: left;
}
.landing {
  background-color: var(--color-text);
  padding: 3em 10em;
  box-sizing: border-box;
  align-items: center;
}
.search {
  align-self: flex-start;
  background-color: white;
  align-items: center;
  margin: 2rem 0rem;
  padding: 0.5em 1em;
  box-sizing: border-box;
  border-radius: 7px;
  width: 100%;

  &__button {
    background: var(--color-blue-1);
    border: none;
    height: 2.5rem;
    width: 7rem;
    color: var(--color-white-1);
    border-radius: 7px;
    transition: 0.5s background-color ease;
    cursor: pointer;
  }
  &__button:hover {
    background-color: var(--color-blue-2);
  }

  &__input {
    height: 100%;
    width: 100%;
    margin-right: 10px;
    border: none;
    font-size: 1.3em;
    font-weight: 530;
  }
  &__input:focus-visible {
    outline: none;
  }
}

.frame {
  //overflow: hidden;

  &__img {
    border-radius: 100px 10px 100px 10px;
    max-width: 100%;
    margin-bottom: -100px;
  }
}
.carousel {
  padding: 10em 10em;
  box-sizing: border-box;
}

[black] {
  color: var(--color-text);
}
.card-group {
  display: grid;
  grid-template-columns: auto auto auto;
  column-gap: 100px;
}
.footer {
  height: 15vh;
  background: var(--color-text);
  color: var(--color-white-1);
  box-sizing: border-box;
  padding: 3em 10em;
}
</style>
