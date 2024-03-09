<script setup>

</script>

<template>
    <div class="Footer">
        <div class="Links">
            <a class="Link" href="https://playstack.com/privacy-policy/" target="_blank">Privacy Policy</a>
            <a class="Link" href="https://playstack.com/terms-and-conditions/" target="_blank">Terms of Service</a>
            <a class="Link">Cookies Settings</a>
        </div>
        <div class="Creator">
            <p>Website made by <a class="CreatorText" href="https://github.com/ssmf" target="_blank">sproutness</a></p>
        </div>
        <div class="Copyright">
            <p class="CopyrightText">© 2023 LocalThunk and Playstack Games. All Rights reserved</p>
        </div>
    </div>
</template>

<style scoped>
    .Footer {
        font-size: var(--LinkSize);
        padding: 40px 0px;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.9);
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        gap: 15px;

    }

    .Links {
        display: flex;
        justify-content: space-between;
        width: max(35%, 350px);
    }

    .Link {
        transition: .15s all ease-in-out;
        text-decoration: none;
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
        text-decoration: none;
    }

    .CreatorText:hover {
        text-shadow: 0px 0px 3px var(--yellow);
        cursor: pointer;
    }

    .CopyrightText {
        color: var(--gray);
        font-size: var(--SmallNoteSize);
        text-shadow: 0px 0px 1px var(--gray);
    }
</style>