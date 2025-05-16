<template>
  <footer class="footer section-dark font-small text-center">
    <ul class="list-inline">
      <li class="list-inline-item">
        <a class="nav-item nav-link active" href="#">
          Accueil
        </a>
      </li>
      <li class="list-inline-item">
        <a class="nav-item nav-link" href="#about">À propos</a>
      </li>
      <li class="list-inline-item">
        <a class="nav-item nav-link" href="#skills">Compétences</a>
      </li>
      <li class="list-inline-item">
        <a class="nav-item nav-link" href="#portfolio">Réalisation</a>
      </li>
      <li class="list-inline-item">
        <a class="nav-item nav-link" href="#contact">Contact</a>
      </li>
    </ul>

    <ul class="list-inline">
      <li
        v-for="(item, i) in social"
        :key="i"
        class="social-item list-inline-item"
      >
        <a :href="item.url" :alt="item.name">
          <i :class="item.faClass"> </i>
        </a>
      </li>
    </ul>

    <div class="copyright">
      <p>
        Copyright © {{ new Date().getFullYear() }}
        {{ text.main.name.last  }}.
        {{ text.footer.copyrightText }}
      </p>
    </div>
    <!-- <div class="credit">
      <p>
        Designed with 👽 by
        <a
          id="username"
          href="https://www.github.com/darnocer"
          alt="Darian's Github"
          >darnocer</a
        >
      </p>
    </div> -->
  </footer>
</template>

<script>
import data from "../../data/data.json";

export default {
  name: "Footer",
  components: {},
  props: {},
  data() {
    return {
      text: data,
      social: data.contact.social,
    };
  },
};
</script>

<style lang="scss"></style>
