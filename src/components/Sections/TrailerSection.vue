<script setup>

</script>

<template>
    <div id="TrailerSection" class="TrailerSection">
        <iframe class="TrailerVideo" src="https://www.youtube-nocookie.com/embed/2n9pkiuSZLU?si=h7TObt3NzwW8jM9y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    </div>
</template>

<style scoped>
    .TrailerSection {
        height: 110vh;
        width: 100%;
        background-color: black;
        display: flex;
        justify-content: center;
        align-items: center;
        background-image: url("/Images/TrailerBackground.png");
        background-size: cover;
        background-position: 50%;
    }

    .TrailerVideo {
        box-shadow: 0px 0px 20px 0px var(--gray);
        border-radius: 25px;
        aspect-ratio: 16 / 9;
        width: max(400px, 50%);
    }
    
</style>