<script setup>
  import {
    RouterLink,
    RouterView
  } from 'vue-router'
  import Personal from './components/Personal.vue'
</script>

<template>
<div class="navbar">
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Navbar</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup"
        aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <!-- <a class="nav-link active" aria-current="page" href="#">Home</a> -->
          <a class="nav-link" href="/personal">Personal</a>
          <a class="nav-link" href="/skills">Skills</a>
          <!-- <a class="nav-link disabled">Disabled</a> -->
        </div>
      </div>
    </div>
  </nav>
  </div>
  <div class="pembungkus">
      <header>
    <img alt="Vue logo" class="logo" src="@/assets/ilham.jpeg" width="125" height="125" />

    <div class="wrapper">
      <Personal msg="Ilham Adriansyah" />

      <!-- <nav>
        <RouterLink to="/">Profile</RouterLink>
        <RouterLink to="/about">Skills</RouterLink>
      </nav> -->
    </div>
  </header>

  </div>
  <RouterView />

</template>

<style scoped>
  header {
    line-height: 1.5;
    max-height: 100vh;
  }

  .logo {
    display: block;
    margin: 0 auto 4rem;
    width: 200px;
    height: 250px;
    border-radius: 15px;
    border: 2px solid gray;
  }

  nav {
    width: 100%;
    font-size: 12px;
    text-align: center;
    margin-top: 2rem;
  }

  nav a.router-link-exact-active {
    color: var(--color-text);
  }

  /* nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
} */

  nav a:first-of-type {
    border: 0;
  }

  @media (min-width: 1024px) {
    header {
      display: flex;
      place-items: center;
      padding-right: calc(var(--section-gap) / 2);
    }

    .logo {
      margin: 0 2rem 0 0;
    }

    header .wrapper {
      display: flex;
      place-items: flex-start;
      flex-wrap: wrap;
    }

    nav {
      text-align: left;
      margin-left: -1rem;
      font-size: 1rem;

      padding: 1rem 0;
      margin-top: 1rem;
    }

    .navbar {
      margin-top: -0.5rem;
    }
  }
</style>