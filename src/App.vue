<script setup>
    import MainButton from './components/Button.vue';
    import { ref } from 'vue';

    const trueBool = ref(true);
</script>

<template>
  <div class="backgroundImage"></div>
  <div class="crtFlickerOverlay crt"></div>
  <div class="main">
    <img src="./assets/images/mainLogo.png" class="mainLogo">
    <h1 class="availableHeader">AVAILABLE NOW!</h1>
    <div class="buttonWrapper">
        <MainButton :ifImage="false" buttonContent="NEWSLETTER"/>
        <MainButton :ifImage="false" buttonContent="WHAT IS BALATRO"/>
        <MainButton :ifImage="false" buttonContent="TRAILER"/>
    </div>
    <div class="StoresWrapper">
        <a href="https://www.nintendo.com/us/store/products/balatro-switch/" target="_blank" class="storeLink"><img src="./assets/images/NintendoLogo.png" class="storeLogo"></a>
        <a href="https://store.playstation.com/en-pl/concept/10010334/" target="_blank" class="storeLink"><img src="./assets/images/PlaystationLogo.png" class="storeLogo"></a>
        <a href="https://www.xbox.com/en-CA/games/store/balatro/9pk087lngjc5" target="_blank" class="storeLink"><img src="./assets/images/XboxLogo.png" class="storeLogo"></a>
        <a href="https://store.steampowered.com/app/2379780/Balatro/?utm_source=website" target="_blank" class="storeLink"><img src="./assets/images/SteamLogo.png" class="storeLogo"></a>
    </div>
    <div class="othersWrapper">
        <MainButton :ifImage="true" buttonContent='LocalThunkLogo.png'/>
        <MainButton :ifImage="true" hoverColor="25deg" buttonContent='DiscordLogo.svg'/>
        <MainButton :ifImage="true" buttonContent="PlaystackLogo.png"/>
        <MainButton :ifImage="false" buttonContent="Press Pack!" style="position: relative;"/>
    </div>
  </div>
</template>

<style scoped>



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

    .main {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        height: 100%;
        max-width: 100%;
        flex-direction: column;
        gap: 50px;
    }

    .mainLogo {
        width: 40%;
        min-width: 400px;
        margin-top: 30px;
        transition: all .15s ease-in-out;
    }

    .availableHeader {
        margin: 0px;
        margin-top: -20px;
        color: var(--mainRed);
        font-size: 40px;
        text-shadow: 5px 5px 1px black;
        transition: .15s all ease-in-out;
    }

    .availableHeader:hover {
        text-shadow: -5px 5px 1px black;
    }

    .buttonWrapper {
        position: relative;
        margin-top: 10px;
        display: flex;
        justify-content: center;
        align-items: flex-start;
        flex-wrap: wrap;
        gap: 25px;
    }

    .StoresWrapper {
        background-color: rgba(0, 0, 0, 0.5);
        border-radius: 25px;
        padding: 20px 30px;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 30px;
        box-shadow: 0px 0px 10px 1px black;
        transition: .15s all ease-in-out;
    }

    .StoresWrapper:hover {
        box-shadow: 0px 0px 15px 5px black;
    }

    .storeLogo {
        width: 100%;
        transition: all .15s ease-in-out;
    }

    .storeLogo:hover {
        filter:drop-shadow(0px 0px 10px white);
        cursor: pointer;
    }

    .storeLink {
        width: 100%;
    }

    .othersWrapper {
        display: flex;
        justify-content: center;
        align-items: stretch;
        gap: 20px;
        flex-wrap: wrap;
        width: 400px;
    }

</style>
