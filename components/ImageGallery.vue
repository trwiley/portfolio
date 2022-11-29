<template>
    <p>{{filteredImages}}</p>
</template>

<script>
import img from '../assets/data.json';
export default{
    name: 'ImageGallery',
    props: ['filter'],
    data () {
        return {
            imageUrls: img.images,
            filteredImages: []
        }  
    },
   
    methods: {
        filterByTag() {
            const filtered = this.imageUrls.filter(image => image.tag === this.filter);
            console.log(filtered);
            this.filteredImages = [...filtered];
        }
    },
    created () {
        this.filterByTag();
    },
}
</script>

<style scoped>
</style>