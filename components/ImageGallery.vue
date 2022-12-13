<template>
    <div>
        <Modal :hideModal="hideModal" :modalShown="modalShown" />
        <button @click="showModal">temp</button>
        <div class="content-parent">
            <div class="gallery">
                <figure v-for="(item, index) in filteredImages">
                    <img :src="require(`../assets/${item.imgUrl}`)" class="image-style border-style"/>
                </figure>
            </div>  
        </div>
        <div style="text-align: right; margin: 36px">
            <NuxtLink to="/">
                <h2>back</h2>
            </NuxtLink>
        </div>
    </div>
   
</template>

<script>
import img from '../assets/data.json';
import Modal from './Modal.vue'

export default{
    name: 'ImageGallery',
    props: ['filter'],
    components: {
        Modal
    },
    data () {
        return {
            imageUrls: img.images,
            filteredImages: [],
            modalShown: false
        }  
    },
   
    methods: {
        filterByTag() {
            const filtered = this.imageUrls.filter(image => image.tag === this.filter);
            this.filteredImages = [...filtered];
        },
        showModal() {
            this.modalShown = true;
        },
        hideModal() {
            this.modalShown = false;
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