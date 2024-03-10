<script setup>
    import { computed } from 'vue';

    const props = defineProps({
        buttonContent: String,
        hoverColor: {
            type: String,
            default: '140deg'
        },
        destination: String
    });

    const ifImage = defineModel('ifImage');
    const imagePath = new URL ('/balatroFanmadeWebsite/Images/' + props.buttonContent, import.meta.url).href; 
    console.log(imagePath);

    const GoTo = () => {
        if (props.destination[0] == "#") {
            window.location.href = props.destination;
        } else {
         window.open(props.destination, "_blank");   
        }
    }
</script>

<template>

<div v-if="!ifImage" class="mainButton" @click="GoTo()">
    {{ buttonContent }}
</div>

<div v-else class="mainButton" @click="GoTo()">
    <img class="buttonImage" :src="imagePath">
</div>


    
</template>

<style scoped>
    .mainButton {
        position: inherit;
        top: 0px;
        padding: 15px 30px;
        font-size: var(--buttonTextSize);
        background-image: url('/Images/newsletterButton.png');
        background-repeat: repeat;
        background-size: 100%;
        border-radius: 15px;
        color: var(--lightBlue);
        border-bottom: 4px solid var(--darkBlue);
        outline: 1px solid black;
        box-shadow: 0px 6px 15px 8px var(--darkBlue);
        transition: all .15s ease-in-out;
        user-select: none;
        display: flex;
        align-items: center;
        justify-content: center;
        max-width: 60%;
        
    }

    .mainButton:hover {
        top: 10px;
        box-shadow: 0px 0px 15px 10px var(--darkBlue);
        cursor: pointer;
        filter: hue-rotate(v-bind(hoverColor));

    }

    .buttonImage {
        width: 50px;
    }
</style>