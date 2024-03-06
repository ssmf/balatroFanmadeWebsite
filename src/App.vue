<script setup>
    import headerSection from '@/components/Sections/HeaderSection.vue'
    import aboutSection from '@/components/Sections/AboutSection.vue'
</script>

<template>
  <div class="backgroundImage"></div>
  <div class="crtFlickerOverlay crt"></div>
  <div class="mainContainer">
    <headerSection></headerSection>
    <aboutSection></aboutSection>
  </div>
</template>

<style scoped>

    .mainContainer {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 100px;
    }

    .backgroundImage {
        background-image: url("@/assets/Images/mainBackground.jpeg");
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
        width: 100%;
        height: 100%;
        position: fixed;
        z-index: -1;
    }

    .crtFlickerOverlay {
        pointer-events: none;
        position: fixed;
        width: 110%;
        height: 100%;
        z-index: 5;
    }

</style>
