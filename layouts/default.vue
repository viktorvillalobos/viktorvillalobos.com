<template>
  <section class="container">
    <b-navbar>
      <template slot="start">
        <b-navbar-item tag="nuxt-link" to="/" exact>
          Projects
        </b-navbar-item>
        <b-navbar-item tag="nuxt-link" to="/about" exact>
          About
        </b-navbar-item>
        <b-navbar-item href="https://pythonist.dev/" target="_blank">
          Blog
        </b-navbar-item>
      </template>
    </b-navbar>
    <header class="section columns is-desktop is-multiline">
      <div class="column is-half-desktop is-full-mobile">
        <h1 class="header-title">
          Víctor Villalobos is a
          <vue-typed-js
            :type-speed="60"
            :start-delay="100"
            :back-delay="1000"
            :back-speed="50"
            :loop="true"
            :strings="['Backend Developer.', 'Frontend Developer.', 'DevOps.']"
          >
            <span class="typing" />
          </vue-typed-js>
        </h1>
      </div>
      <div class="column header-image is-half-desktop">
        <picture>
          <source
            srcset="
              /img/header-2x.webp ,
              /img/header-2x.webp 2x,
              /img/header-3x.webp 3x,
              /img/header-4x.webp 4x,
            "
            alt="people-working"
            type="image/webp"
          >
          <img
            src="/img/header.png"
            srcset="
              /img/header-2x.png 2x,
              /img/header-3x.png 3x,
              /img/header-4x.png 4x,
            "
            alt="people-working"
          >
        </picture>
      </div>
    </header>
    <main class="content">
      <nuxt />
    </main>
    <footer>
      <a href="mailto:viktor@adslab.io">viktor@adslab.io</a>
    </footer>
  </section>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' }
        }
      ]
    }
  }
}
</script>

<style lang="scss">

@import '~/assets/scss/pages/home.scss';

</style>
