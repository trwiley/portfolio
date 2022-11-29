<template>
    <div class="gallery">
        <figure v-for="(item, index) in filteredImages">
            <img :src="require(`../assets/${item.imgUrl}`)" class="image-style"/>
        </figure>
    </div>  
</template>

<script>
import img from '../assets/data.json';

export default{
    name: 'ImageGallery',
    props: ['filter'],
    data () {
        return {
            imageUrls: img.images,
            filteredImages: [],
        }  
    },
   
    methods: {
        filterByTag() {
            const filtered = this.imageUrls.filter(image => image.tag === this.filter);
            this.filteredImages = [...filtered];
        }
    },
    created () {
        this.filterByTag();
    },
}
</script>

<style scoped>
    .gallery{
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-gap: 15px;
    }
    .image-style{
        width: 200px;
        height: auto;
    }

</style>