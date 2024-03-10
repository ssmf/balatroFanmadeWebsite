<script setup>

</script>

<template>
    <div id="AboutSection" class="aboutSection">
        <div class="sectionHeader">
        <img class="cardImage corner" src="/Images/GlassCard.png">
        <img class="cardImage otherCorner" src="/Images/AbandonedDeck.png">
            <h1 class="mainHeader">WHAT IS BALATRO?</h1>
            <p class="paragraph" style="font-size: var(--headerParagraphSize);"><span style="color: var(--mainRed)">Balatro</span> is a <span style="color: var(--yellow)">poker-inspired roguelike deck builder</span>
                all about creating powerful synergies and winning big.</p>

            <p class="paragraph">Combine valid poker hands with unique Joker cards in order to create varied synergies
                and builds. Earn enough chips to beat devious blinds, all while uncovering hidden bonus hands and decks
                as you progress. You’re going to need every edge you can get in order to reach the boss blind,
                beat the final ante and secure victory.</p>

        </div>
        <div class="detailsSection">
            <div class="infoCard cardsSection">
                <img class="cardImage bigCard" src="/Images/TarotStar.png">
                <h2 class="secHeader">JOKERS, VOUCHERS AND BOOSTER PACKS!</h2>
                <p class="paragraph">
                    Deftly deploy an array of potent tools: different Decks, Jokers, Tarot cards, Planet cards, Spectral cards,
                    and Vouchers. Use these versatile instruments to ignite a combo frenzy and turbocharge your poker hands,
                    crafting electrifying, adrenaline-fueled synergies.
                </p>
                <img class="gif cardGif" src="/Images/Pokers.gif" alt="A gif of ingame pokers you can use">
            </div>
            <h1 class="X">X</h1>
            <div class="infoCard mechanicsSection">
                <img class="cardImage chip" src="/Images/Chip.png">
                <img class="gif cardGif" src="/Images/SpectralPack.gif" alt="A gif of ingame Spectral booster pack being opened">
                <h2 class="secHeader">THINK AHEAD, BET AND HOPE</h2>
                <p class="paragraph">Carefully choose the jokers you are buying, how you are spending your money and whether
                    should you risk discarding your cards! Make use of the in-depth stats screen to study your best hands, 
                    most used Jokers, and more!
                </p>
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
            top: 8%;
            left: 95%;
            rotate: 20deg;
            width: 85%;
        }

        img.chip {
            left: -80%;
            top: 10%;
            width: 85%;
            rotate: -20deg;
        }

        .infoCard {
            width: max(320px, 60%)
        }
    }

    @media (max-width: 500px) {
        body, html {
            overflow: auto !important;
        }
        div > img.bigCard {
            top: 10%;
            left: 80%;
            rotate: 20deg;
            width: max(200px,90%);
        }

        div > img.chip {
            left: -80%;
            top: 10%;
            width: max(200px,90%);
            rotate: -20deg;
        }

        div > .infoCard {
            width: max(50%, 150px);
            padding: 18px 22px;
            gap: 12px;
        }

        div > .detailsSection {
            width: max(100%, 200px);
        }
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
    

    .aboutSection {
        padding: 100px 0px;
        width: 90%;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 30px;
        border-radius: 25px;
        z-index: 2;
    }

    .cardImage {
        position: absolute;
        width: 110px;
        image-rendering: pixelated;
        
    }

    .bigCard {
        width: max(75%, 350px);
        left: -65%;
        rotate: -20deg;
        z-index: -1;
        filter: opacity(.6) blur(1px) drop-shadow(0px 0px 50px var(--cardYellow));
    }

    .chip {
        z-index: -1;
        width: 75%;
        left: 92%;
        top: 12%;
        rotate: 20deg;
        filter: opacity(.8) blur(1px) drop-shadow(0px 0px 40px var(--green));
    }

    .gif {
        background-color: rgba(0, 0, 0, 0.5);
        border-radius: 25px;
        box-shadow: 0px 0px 10px 0px black;
        padding: 10px 20px;
        z-index: 3;
    }

    .cardGif {
        background-color: rgba(0, 0, 0, 0.0);
        box-shadow: 0px 0px 0px 0px black;
        filter: drop-shadow(0px 0px 5px white);
        width: 150%;
    }

    .sectionHeader {
        position: relative;
        width: max(80%, 300px);
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
        width: max(70%, 500px);
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
        height: fit-content;
        position: relative;
        border: 2px solid black;
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