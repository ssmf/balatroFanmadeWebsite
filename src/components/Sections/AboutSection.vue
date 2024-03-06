<script setup>

</script>

<template>
    <div class="aboutSection">
        <div class="sectionHeader">
            <h1 class="mainHeader">WHAT IS BALATRO?</h1>
            <p class="paragraph" style="font-size: 19px;"><span style="color: var(--mainRed)">Balatro</span> is a <span style="color: var(--yellow)">poker-inspired roguelike deck builder</span>
                all about creating powerful synergies and winning big.</p>

            <p class="paragraph">Combine valid poker hands with unique Joker cards in order to create varied synergies
                and builds. Earn enough chips to beat devious blinds, all while uncovering hidden bonus hands and decks
                as you progress. You’re going to need every edge you can get in order to reach the boss blind,
                beat the final ante and secure victory.</p>

        </div>
        <div class="detailsSection">
            <div class="infoCard cardsSection">
                <h2 class="secHeader">JOKERS, VOUCHERS AND BOOSTER PACKS!</h2>
                <p class="paragraph">
                    Deftly deploy an array of potent tools: different Decks, Jokers, Tarot cards, Planet cards, Spectral cards,
                    and Vouchers. Use these versatile instruments to ignite a combo frenzy and turbocharge your poker hands,
                    crafting electrifying, adrenaline-fueled synergies.
                </p>
            </div>
            <h1 class="X">X</h1>
            <div class="infoCard mechanicsSection">
                <h2 class="secHeader">THINK AHEAD, BET AND HOPE</h2>
                <p class="paragraph">Deftly deploy an array of potent tools: different Decks, Jokers, Tarot cards, Planet cards, Spectral cards,
                    and Vouchers. Use these versatile instruments to ignite a combo frenzy and turbocharge your poker hands,
                    crafting electrifying, adrenaline-fueled synergies.</p>
            </div>
        </div>
    </div>
</template>

<style scoped>

    .aboutSection {
        width: 70%;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 30px;
        border-radius: 25px;
    }

    .sectionHeader {
        width: 80%;
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
        filter: drop-shadow(0px 0px 5px var(--darkBlue))
    }

    .paragraph {
        font-size: var(--paragraphSize);
    }

    .detailsSection {
        height: 600px;
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