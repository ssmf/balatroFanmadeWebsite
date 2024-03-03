<script setup>
    import { ref } from 'vue';
    
    const props = defineProps({
        buttonContent: String,
        hoverColor: {
            type: String,
            default: '140deg'
        }
    });

    const ifImage = defineModel('ifImage');
    const imagePath = 'src/assets/images/' + props.buttonContent;

    console.log(props.hoverColor)
</script>

<template>

<div v-if="!ifImage" class="mainButton">
    {{ buttonContent }}
</div>

<div v-else class="mainButton">
    <img class="buttonImage" :src="imagePath">
</div>


    
</template>

<style scoped>
    .mainButton {
        position: inherit;
        top: 0px;
        padding: 15px 30px;
        font-size: 25px;
        background-image: url('../assets/Images/newsletterButton.png');
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