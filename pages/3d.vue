<template>
    <div>
        <BackArrow />
       <div class="header-align">
           <img src="/img/icons-and-links/3d_header.png" alt="3D Art" class="header-style"/>
       </div>    
       <ImageGallery filter="3d"/>
   </div>
</template>

<script>
import ImageGallery from '~/components/ImageGallery.vue';
import BackArrow from '~/components/BackArrow.vue';
export default{
    name: 'ThreeDPage',
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