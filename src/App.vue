<template>
  <main class="container-fluid main">
    <ModalPatrimonio  class="d-none"/>
    <NavbarComponent
      @wheel="riseIndex"
      class="d-sm-none p-0 mb-0 mobile-navbar"
    />
    <FAB />
    <NavbarComponent class="fixed-top d-none d-sm-flex" />
    <GallerySection></GallerySection>
    <FooterComponent></FooterComponent>
  </main>
</template>

<script>
import NavbarComponent from "./components/navbar.vue";
import GallerySection from "./components/gallery.vue";
import FooterComponent from "./components/footerComponent.vue";
import FAB from "./components/FAB.vue";
import ModalPatrimonio from "./components/ModalPatrimonio.vue";

export default {
  name: "App",
  components: {
    NavbarComponent,
    GallerySection,
    FooterComponent,
    FAB,
    ModalPatrimonio,
  },
  methods: {
    riseIndex: function () {
      console.log("riseNav");
      document
        .querySelector(".main .navbar")
        .classList.add("mobile-navbar--vanish");
      document.querySelector(".main .FAB").classList.add("show-FAB");
    },
  },
};
</script>
<style>
.mobile-navbar {
  height: 80vh;
  animation: vanish-header 3s ease;
}
.main .mobile-navbar--vanish {
  height: 0vh;
  top: -75vh;
  animation: riseGallery 2s ease;
}

@keyframes riseGallery {
  from {
    height: 30vh;
  }
  to {
    height: 0vh;
    top: -30vh;
  }
}
</style>
