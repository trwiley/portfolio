<template>
    <div class="content-parent">
        <div class="gallery">
            <figure v-for="(item, index) in filteredImages">
                <img :src="require(`../assets/${item.imgUrl}`)" class="image-style border-style"/>
            </figure>
        </div>  
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
    .content-parent{
        display: grid;
        justify-content: center;
    }
    .gallery{
        display: grid;
        grid-template-columns: repeat(3, 400px);
        grid-gap: 36px;
        justify-items: center;
    }
    .image-style{
        width: 400px;
        height: auto;
    }

</style>