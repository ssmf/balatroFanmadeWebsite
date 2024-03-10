<script setup>
    import MainButton from '../Button.vue';
</script>

<template>
  <div class="headerSection">
    <img src="/Images/mainLogo.png" class="mainLogo">
    <h1 class="availableHeader">AVAILABLE NOW!</h1>
    <div class="buttonWrapper">
        <MainButton :destination="'#NewsletterSection'" :ifImage="false" buttonContent="NEWSLETTER" />
        <MainButton :destination="'#AboutSection'" :ifImage="false" buttonContent="WHAT IS BALATRO"/>
        <MainButton :destination="'#TrailerSection'" :ifImage="false" buttonContent="TRAILER"/>
    </div>
    <div class="StoresWrapper">
        <a href="https://www.nintendo.com/us/store/products/balatro-switch/" target="_blank" class="storeLink"><img src="/Images/NintendoLogo.png" class="storeLogo"></a>
        <a href="https://store.playstation.com/en-pl/concept/10010334/" target="_blank" class="storeLink"><img src="/Images/PlaystationLogo.png" class="storeLogo"></a>
        <a href="https://www.xbox.com/en-CA/games/store/balatro/9pk087lngjc5" target="_blank" class="storeLink"><img src="/Images/XboxLogo.png" class="storeLogo"></a>
        <a href="https://store.steampowered.com/app/2379780/Balatro/?utm_source=website" target="_blank" class="storeLink"><img src="/Images/SteamLogo.png" class="storeLogo"></a>
    </div>
    <div class="othersWrapper">
        <MainButton :destination="'https://twitter.com/LocalThunk'" :ifImage="true" buttonContent='LocalThunkLogo.png'/>
        <MainButton :destination="'https://discord.com/invite/5mH3dNhjx2'" :ifImage="true" hoverColor="25deg" buttonContent='DiscordLogo.svg'/>
        <MainButton :destination="'https://playstack.com/'" :ifImage="true" buttonContent="PlaystackLogo.png"/>
        <MainButton :destination="'https://www.dropbox.com/scl/fo/lg163t04ifnwekgrqra6y/h?rlkey=0mt8hxmk5avygd8b2ky5ouwww&dl=0'" :ifImage="false" buttonContent="Press Pack!" style="position: relative;"/>
    </div>
    <img class="gif" src="/Images/Aces.gif" alt="A gif of Ace cards">
  </div>
</template>

<style scoped>

    .headerSection {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        flex-direction: column;
        gap: 45px;
    }

    .mainLogo {
        width: 40%;
        min-width: 300px;
        margin-top: 30px;
        transition: all .15s ease-in-out;
    }

    .availableHeader {
        padding: 0px 5px;
        word-break: break-word;
        margin: 0px;
        margin-top: -20px;
        color: var(--mainRed);
        font-size: var(--h1Size);
        text-shadow: 5px 5px 1px black;
        transition: .15s all ease-in-out;
    }

    .availableHeader:hover {
        text-shadow: -5px 5px 1px black;
        filter: drop-shadow(-2.5px -2.5px 5px var(--mainRed))
    }

    .buttonWrapper {
        width: max(80%, 400px);
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
        padding: 20px 20px;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 15px;
        box-shadow: 0px 0px 10px 1px black;
        transition: .15s all ease-in-out;
    }

    .StoresWrapper:hover {
        box-shadow: 0px 0px 15px 5px black;
    }

    .storeLogo {
        width: 80%;
        transition: all .15s ease-in-out;
    }

    .storeLogo:hover {
        filter:drop-shadow(0px 0px 10px white);
        cursor: pointer;
    }

    .storeLink {
        width: 100%;
        display: flex;
        align-items: center;
    }

    .othersWrapper {
        display: flex;
        justify-content: center;
        align-items: stretch;
        gap: 20px;
        flex-wrap: wrap;
        width: 400px;
    }

    .gif {
      width: max(50%, 350px);
      background-color: rgba(0, 0, 0, 0.5);
      border-radius: 25px;
      box-shadow: 0px 0px 10px 0px black;
      padding: 10px 20px;
    }

</style>
