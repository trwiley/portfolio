<template>
     <div>
        <BackArrow />
        <div class="header-align">
            <img src="/img/icons-and-links/digital_header.png" alt="Digital Art" class="header-style"/>
        </div>    
        <ImageGallery filter="digital"/>
    </div>
</template>

<script>
import ImageGallery from '~/components/ImageGallery.vue';
import BackArrow from '~/components/BackArrow.vue';
export default{
    name: 'DigitalPage',
    components: {
        ImageGallery,
        BackArrow
    }
}
</script>

<style scoped>
    .header-style{
        height: 100px;
        width: auto;
    }
    .header-align{
        text-align: center; 
        margin: 16px;
    }
</style>