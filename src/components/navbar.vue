<template>
  <nav class="navbar navbar-light pb-0">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">
        <img
          src="/docs/5.0/assets/brand/bootstrap-logo.svg"
          alt=""
          width="30"
          height="24"
          class="d-inline-block align-text-top"
        />
      </a>
      <div class="d-flex flex-column col-9 col-md-auto align-items-center">
        <p class="navbar__title text-start text-sm-center">
          MUSEO <span>de</span> PICHILEMU EN LINEA
        </p>
        <p class="navbar__url text-start col-12 text-sm-center">
          www.museopichilemuenlinea.cl
        </p>
        <p class="navbar__punchline text-start me-md-5 me-lg-auto col-12 text-sm-center">
          Deuncuantohay
        </p>
      </div>
      <a class="navbar-brand d-none d-lg-flex" href="#">
        <img
          src="/docs/5.0/assets/brand/bootstrap-logo.svg"
          alt=""
          width="30"
          height="24"
          class="d-inline-block align-text-top"
        />
      </a>
    </div>
    <EditorialSection class="d-none d-sm-flex"/>
    <hr class="d-sm-none" />
  </nav>
</template>

<script>
import EditorialSection from "./editorialSection.vue";

export default {
  name: "NavbarComponent",
  components: {
    EditorialSection,
  },
};
</script>

<style>
.navbar {
  font-family: "Old Standard TT", serif;
  text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.1);
  background-image: url(https://images.unsplash.com/photo-1615800098779-1be32e60cca3?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2020&q=80);
  z-index: 2;
}
.navbar .navbar__title {
  font-size: 30px;
  font-weight: 700;
  line-height: 34px;
  margin-top: 20px;
  margin-bottom: 0px;
}
.navbar .navbar__title span {
  font-style: italic;
}
.navbar .navbar__url {
  font-family: "Roboto Mono", monospace;
  font-size: 14px;
  line-height: 14px;
}
.navbar .navbar__punchline {
  font-size: 24px;
  line-height: 24px;
  margin-bottom: 5px;
}
hr {
  margin: 4px;
  color: #1d1d1d;
  background-color: #1d1d1d;
  border: 1px solid;
  opacity: 1;
}
@media (min-width: 400px) {
  .navbar {
    position: fixed;
  }
  .navbar .navbar__title {
    font-size: 30px;
    font-weight: 700;
    line-height: 34px;
    margin-top: 0px;
    margin-bottom: 0rem;
  }
  .navbar .navbar__url {
    margin-bottom: .5rem;
  }
}
@media (min-width: 768px) {
  .navbar .navbar__title {
    font-size: 40px;
    font-weight: 700;
    line-height: 20px;
    margin-top: 20px;
  }
  .navbar .navbar__title span {
    font-style: italic;
  }
  .navbar .navbar__url {
    font-family: "Roboto Mono", monospace;
    font-size: 16px;
    line-height: 15px;
  }
  .navbar .navbar__punchline {
    font-size: 34px;
    line-height: 20px;
    margin-bottom: 5px;
  }
}
</style>
