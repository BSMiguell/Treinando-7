<template>
  <div id="app">
    <NavbarView />
    <HeaderView />
    <AboutView />
    <ServiceView />
    <ProjectsView />
    <FooterView />
  </div>
</template>

<script>
import NavbarView from "./components/NavbarView.vue";
import HeaderView from "./components/HeaderView.vue";
import AboutView from "./components/AboutView.vue";
import ServiceView from "./components/ServiceView.vue";
import ProjectsView from "./components/ProjectsView.vue";
import FooterView from "./components/FooterView.vue";

export default {
  name: "App",
  components: {
    NavbarView,
    HeaderView,
    AboutView,
    ServiceView,
    ProjectsView,
    FooterView,
  },
};
</script>

<style>
@import "~@fortawesome/fontawesome-free/css/all.css";
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap");

:root {
  --primary-color: #000000;
  --secondary-color: #ff4e05;
  --secondary-color-dark: #bf3900;
  --text-dark: #0d1319;
  --text-light: #9ca3af;
  --white: #ffffff;
  --max-width: 1200px;
}
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.section__container {
  max-width: var(--max-width);
  margin: auto;
  padding: 5rem 1rem;
}
.section__title {
  font-size: 2rem;
  font-weight: 600;
  text-align: center;
}
.section__title span {
  color: var(--secondary-color);
}
.section__subtitle {
  font-size: 1rem;
  font-weight: 500;
  text-align: center;
}
img {
  width: 100%;
}
.btn {
  padding: 1rem;
  font-size: 0.9rem;
  font-weight: 600;
  outline: none;
  border: none;
  border-radius: 5px;
  color: var(--white);
  background-color: var(--secondary-color);
  cursor: pointer;
  transition: 0.3s;
}
.btn:hover {
  background-color: var(--secondary-color-dark);
}
a {
  text-decoration: none;
  color: var(--white);
}
body {
  color: var(--white);
  font-family: "Poppins", sans-serif;
}

/* Media queries */

@media (min-width: 640px) {
  .section__title {
    font-size: 2.5rem;
  }

  .header__container p {
    margin: 2rem 0;
  }

  .header__container h1 {
    font-size: 4rem;
    line-height: 4rem;
  }

  .action__btns {
    gap: 2rem;
  }

  .about__content {
    align-items: flex-start;
  }

  .about__details {
    text-align: left;
  }

  .footer__container {
    grid-template-columns: repeat(2, 1fr);
  }
}
@media (min-width: 768px) {
  .header__container h1 {
    font-size: 5rem;
    line-height: 5rem;
  }
}
@media (max-width: 430px) {
  .section__title {
    font-size: 1.5rem;
  }
}
</style>
