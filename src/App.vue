<script setup>
    import headerSection from '@/components/Sections/HeaderSection.vue'
    import aboutSection from '@/components/Sections/AboutSection.vue'
    import trailerSection from '@/components/Sections/TrailerSection.vue'
    import NewsletterSection from '@/components/Sections/NewsletterSection.vue';
    import Footer from '@/components/Sections/Footer.vue';
</script>

<template>
  <div class="backgroundImage"></div>
  <div class="crtFlickerOverlay crt"></div>
  <div class="mainContainer">
    <headerSection></headerSection>
    <aboutSection></aboutSection>
    <trailerSection></trailerSection>
    <NewsletterSection></NewsletterSection>
    <Footer></Footer>
  </div>
</template>

<style scoped>

    .mainContainer {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .backgroundImage {
        background-image: url("/Images/mainBackground.jpeg");
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
        width: 100vw;
        height: 100%;
        position: fixed;
        z-index: -1;
    }

    .crtFlickerOverlay {
        pointer-events: none;
        position: fixed;
        width: 100vw;
        height: 100%;
        z-index: 5;
    }

</style>
