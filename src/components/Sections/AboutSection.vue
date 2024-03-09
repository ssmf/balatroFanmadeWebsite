<script setup>

</script>

<template>
    <div class="aboutSection">
        <img class="gif" :src="'src/assets/images/Aces.gif'" alt="A gif of Ace cards">
        <div class="sectionHeader">
        <img class="cardImage corner" :src="'src/assets/images/GlassCard.png'">
        <img class="cardImage otherCorner" :src="'src/assets/images/AbandonedDeck.png'">
            <h1 class="mainHeader">WHAT IS BALATRO?</h1>
            <p class="paragraph" style="font-size: 19px;"><span style="color: var(--mainRed)">Balatro</span> is a <span style="color: var(--yellow)">poker-inspired roguelike deck builder</span>
                all about creating powerful synergies and winning big.</p>

            <p class="paragraph">Combine valid poker hands with unique Joker cards in order to create varied synergies
                and builds. Earn enough chips to beat devious blinds, all while uncovering hidden bonus hands and decks
                as you progress. You’re going to need every edge you can get in order to reach the boss blind,
                beat the final ante and secure victory.</p>

        </div>
        <div class="detailsSection">
            <img class="cardImage bigCard" :src="'src/assets/images/TarotStar.png'">
            <img class="cardImage chip" :src="'src/assets/images/Chip.png'">
            <div class="infoCard cardsSection">
                <h2 class="secHeader">JOKERS, VOUCHERS AND BOOSTER PACKS!</h2>
                <p class="paragraph">
                    Deftly deploy an array of potent tools: different Decks, Jokers, Tarot cards, Planet cards, Spectral cards,
                    and Vouchers. Use these versatile instruments to ignite a combo frenzy and turbocharge your poker hands,
                    crafting electrifying, adrenaline-fueled synergies.
                </p>
                <img class="gif cardGif" :src="'src/assets/images/Pokers.gif'" alt="A gif of ingame pokers you can use">
            </div>
            <h1 class="X">X</h1>
            <div class="infoCard mechanicsSection">
                <img class="gif cardGif" :src="'src/assets/images/SpectralPack.gif'" alt="A gif of ingame Spectral booster pack being opened">
                <h2 class="secHeader">THINK AHEAD, BET AND HOPE</h2>
                <p class="paragraph">Deftly deploy an array of potent tools: different Decks, Jokers, Tarot cards, Planet cards, Spectral cards,
                    and Vouchers. Use these versatile instruments to ignite a combo frenzy and turbocharge your poker hands,
                    crafting electrifying, adrenaline-fueled synergies.</p>
            </div>
        </div>
    </div>
</template>

<style scoped>

    @media (max-width: 1200px) {
        .detailsSection {
            flex-direction: column;
            
        }

        img.bigCard {
            top: 6%;
            left: 65%;
            rotate: 20deg;
            width: 45%;
        }

        img.chip {
            left: -10%;
            top: 64%;
            width: 45%;
            rotate: -20deg;
        }
    }

    .aboutSection {
        width: 70%;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 30px;
        border-radius: 25px;
    }

    .cardImage {
        position: absolute;
        width: 110px;
        image-rendering: pixelated;
    }

    .bigCard {
        width: 40%;
        left: -35%;
        rotate: -20deg;
        z-index: -1;
        filter: opacity(.6) blur(1px) drop-shadow(0px 0px 50px var(--cardYellow));
    }

    .chip {
        z-index: -1;
        width: 40%;
        left: 98%;
        rotate: 20deg;
        filter: opacity(.8) blur(1px) drop-shadow(0px 0px 40px var(--green));
    }

    .corner {
        top:  -50px;
        left: -40px;
        rotate: 20deg;
        filter: opacity(.7) blur(.4px) drop-shadow(0px 0px 5px white);
    }

    .otherCorner {
        filter: drop-shadow(0px 0px 5px var(--gameRed));
        z-index: -1;
        top:  75%;
        left: 95%;
        rotate: -30deg;
    }

    .gif {
        background-color: rgba(0, 0, 0, 0.5);
        border-radius: 25px;
        box-shadow: 0px 0px 10px 0px black;
        padding: 10px 20px;
    }

    .cardGif {
        background-color: rgba(0, 0, 0, 0.0);
        box-shadow: 0px 0px 0px 0px black;
        filter: drop-shadow(0px 0px 5px white);
        width: 150%;
    }

    .sectionHeader {
        position: relative;
        width: max(80%, 500px);
        background-color: rgba(0, 0, 0, 0.5);
        border-radius: 25px;
        display: flex;
        flex-direction: column;
        gap: 20px;
        padding: 20px 40px;
        border: 3px solid black;
    }

    .secHeader {
        font-size: var(--h2Size);
    }

    .mainHeader {
        font-size: var(--h1Size);
        text-shadow: 7px 7px 2px var(--darkBlue);
    }

    .paragraph {
        font-size: var(--paragraphSize);
    }

    .detailsSection {
        position: relative;
        width: max(80%, 800px);
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-radius: 25px;
        gap: 20px;
    }

    .X {
        text-shadow: 3px 3px 0px black;
    }

    .infoCard {
        border: 2px solid black;
        width: max(400px, 30%);
        padding: 20px 30px;
        border-radius: 40px;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 20px;
    }

    .cardsSection {
        align-self: flex-start;
        background-color: var(--gameRed);
    }

    .mechanicsSection {
        align-self: flex-end;
        background-color: var(--gameBlue);
    }

</style>