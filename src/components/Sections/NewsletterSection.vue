<script setup>

</script>

<template>
    <div id="NewsletterSection" class="NewsletterSection">
        <h2 class="sectionHeader">Sign up for Updates and news about Balatro!</h2>
        <div class="InputContainer">
            <div class="UnavailableBox">CURRENTLY UNAVAILABLE!</div>
            <input size="15" placeholder="NAME" class="Input nameInput" type="text" name="name" required minlength="2">
            <input size="20" placeholder="E-MAIL" class="Input EmailInput" type="email" name="email" required>
            <button class="Input SubscribeButton">✓</button>
        </div>
        <p class="NewslettersNote">You can unsubscribe at any time.We use Mailchimp as our marketing platform. By clicking subscribe, you acknowledge
            that your contact information will be transferred to Mailchimp for processing.Learn more about Mailchimp’s
            privacy practices here.</p>
    </div>
</template>

<style scoped>

    .NewsletterSection::before {
        content: '';
        position: absolute;
        height: 100%;
        width: 100%;
        background-color: black;
        opacity: .4;
        top: 0;
    }

    .NewsletterSection {
        position: relative;
        padding: 200px 0px;
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 20px;
        background-color: black;
        background-image: url('/Images/NewsletterBackground.gif');
        background-size: cover;
        background-blend-mode: lighten;
        background-position: center;
    }

    .sectionHeader {
        font-size: var(--h2Size);
        z-index: 2;
        filter: drop-shadow(0px 0px 5px white);
        width: 80%;
    }

    .InputContainer {
        position: relative;
        z-index: 2;
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        justify-content: center;
        align-items: center;
        width: 90%;
    }

    .UnavailableBox {
        z-index: 5;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 25px;
        position: absolute;
        width: 100%;
        height: 100%;
        background-color: black;
        opacity: .8;
        filter: drop-shadow(0px 0px 10px white);
        text-shadow: 0px 0px 4px white;
    }

    .Input {
        font-size: var(--headerParagraphSize);
        padding: 15px 10px;
        background-color: var(--mainBlue);
        box-shadow: 0px 0px 4px 0px var(--mainBlue);
        border: none;
        border-bottom: 5px solid var(--darkBlue);
        border-radius: 10px;
        transition: .15s all ease-in-out;
        transition: .05 s outline;
    }

    .Input:focus {
        outline: 2px solid black;
        box-shadow: 0px 0px 10px 3px var(--mainBlue);
    }

    .EmailInput {
        background-color: var(--mainRed);
        box-shadow: 0px 0px 4px 0px var(--mainRed);
        border-bottom: 5px solid var(--darkRed);
    }

    .EmailInput:focus {
        box-shadow: 0px 0px 10px 3px var(--mainRed);
    }

    .SubscribeButton {
        position: relative;
        padding: 20px;
        background-color: var(--green);
        box-shadow: 0px 0px 5px 0px var(--green);
        border-bottom: 5px solid var(--darkGreen);
    }

    .SubscribeButton:hover {
        cursor: pointer;
        box-shadow: 0px 0px 15px 3px var(--saturatedGreen);
        background-color: var(--saturatedGreen);
    }

    .SubscribeButton:focus {
        outline: none;
    }

    .NewslettersNote {
        z-index: 2;
        font-size: var(--LinkSize);
        width: min(800px, 90%);
        text-shadow: 1px 1px 0px lightBlue;
        color: var(--lightBlue);
    }

</style>