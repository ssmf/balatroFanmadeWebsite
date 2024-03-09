<script setup>

</script>

<template>
    <div class="NewsletterSection">
        <h2 class="sectionHeader">Sign up for Updates and news about Balatro!</h2>
        <div class="InputContainer">
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
        margin-top: -100px;
        width: 100%;
        padding: 200px 40px;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 20px;
        background-color: black;
        background-image: url('@/assets/Images/NewsletterBackground.gif');
        background-size: cover;
        background-blend-mode: lighten;
        background-position: 100%;
    }

    .sectionHeader {
        font-size: var(--h2Size);
        z-index: 2;
        filter: drop-shadow(0px 0px 5px white);
    }

    .InputContainer {
        z-index: 2;
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        justify-content: center;
    }

    .Input {
        font-size: 18px;
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
        background-image: url('@/assets/Images/newsletterButton.png');
        box-shadow: 0px 0px 5px 0px var(--green);
        border-bottom: 5px solid var(--darkGreen);
    }

    .SubscribeButton::after {
        position: absolute;
        content: '';
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        background-color: var(--green);
        border-radius: 10px;
        mix-blend-mode: color;
    }

    .SubscribeButton:hover {
        cursor: pointer;
        box-shadow: 0px 0px 15px 3px var(--green);
        background-position-y: 100%;
    }

    .SubscribeButton:focus {
        outline: none;
    }

    .NewslettersNote {
        z-index: 2;
        font-size: 13px;
        width: max(400px, 50%);
        text-shadow: 2px 2px 0px lightBlue;
        color: var(--lightBlue);
    }

</style>