<template>
    <p>{{imageUrls}}</p>
</template>

<script>
import img from '../assets/data.json';
export default{
    name: 'ImageGallery',
    data () {
        return {
            imageUrls: img.images
        }  
    },
    beforeMount: (() => {
        // images.map((image) => {
        //     this.imageUrls.push(image.imgUrl);
        // })
    })
}
</script>

<style scoped>
</style>