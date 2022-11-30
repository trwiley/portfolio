<template>
    <div>
        <div class="header-align">
            <img src="/img/icons-and-links/traditional_header.png" alt="Traditional Art" class="header-style"/>
        </div>    
        <ImageGallery filter="traditional"/>
    </div>

</template>

<script>
import ImageGallery from '../components/ImageGallery.vue'
export default{
    name: 'TraditionalPage',
    components: {
        ImageGallery,
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