<script setup>

</script>

<template>
    <div class="NewsletterSection">
        <h2 class="sectionHeader">Sign up for Updates and news about Balatro!</h2>
        <div class="InputContainer">
            <input size="15" placeholder="NAME" class="Input nameInput" type="text" name="name" required minlength="2">
            <input size="25" placeholder="E-MAIL" class="Input EmailInput" type="email" name="email" required>
            <button class="Input SubscribeButton">✓</button>
        </div>
    </div>
</template>

<style scoped>

    .NewsletterSection {
        margin-top: -100px;
        width: 100%;
        padding: 100px 20px;
        background-color: var(--gray);
        display: flex;
        flex-direction: column;
        gap: 20px;
    }

    .sectionHeader {
        font-size: var(--h2Size);
    }

    .InputContainer {
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
        padding: 20px;
        background-color: var(--green);
        box-shadow: 0px 0px 5px 0px var(--green);
        border-bottom: 5px solid var(--darkGreen);
    }

    .SubscribeButton:hover {
        cursor: pointer;
        box-shadow: 0px 0px 15px 3px var(--green);
    }

    .SubscribeButton:focus {
        outline: none;
    }

</style>