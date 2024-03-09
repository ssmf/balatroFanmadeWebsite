<script setup>

</script>

<template>
    <div class="Footer">
        <div class="Links">
            <a class="Link">Privacy Policy</a>
            <a class="Link">Terms of Service</a>
            <a class="Link">Cookies Settings</a>
        </div>
        <div class="Creator">
            <p>Made by <a class="CreatorText">sproutness</a></p>
        </div>
        <div class="Copyright"></div>
    </div>
</template>

<style scoped>
    .Footer {
        font-size: 12px;
        margin-top: -100px;
        padding: 40px 0px;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.9);
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 15px;

    }

    .Links {
        display: flex;
        justify-content: space-between;
        width: max(35%, 350px);
    }

    .Link {
        transition: .15s all ease-in-out;
    }

    .Link:hover {
        color: var(--gray);
        cursor: pointer;
    }

    .CreatorText {
        position: relative;
        color: var(--yellow); 
        text-shadow: 0px 0px 1px var(--yellow);
        transition: .15s all ease-in-out;
    }

    .CreatorText:hover {
        text-shadow: 0px 0px 3px var(--yellow);
        cursor: pointer;
    }
</style>