<template>
    <div>
        <Modal :hideModal="hideModal" :modalShown="modalShown" :artInfo="currentObject" />
        <div class="content-parent">
            <div class="gallery">
                <figure v-for="(item, index) in filteredImages">
                    <img :src="require(`../assets/${item.imgUrl}`)" class="image-style img-border" @click="setModalArt(item)"/>
                </figure>
            </div>  
        </div>
        <div style="text-align: left; margin: 36px">
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
            modalShown: false,
            currentObject: {
                'title': 'p',
                'year': 'p',
                'medium': 'p',
                'imgUrl': 'art_img/placeholder.png'
            }
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
        },
        setModalArt(item) {
            this.currentObject = {...item};
            this.showModal();
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
        margin-top: 36px;
    }
    .gallery{
        display: grid;
        grid-template-columns: repeat(3, 350px);
        grid-gap: 36px;
        justify-items: center;
    }

    @media(min-width: 1200px){
        .gallery{
            grid-template-columns: repeat(3, 350px);
        }
        .image-style{
            width: 350px;
            height: 350px;
        }

    }

    @media(max-width: 1199px) and (min-width: 900px){
        .gallery{
            grid-template-columns: repeat(2, 350px);
        }
        .image-style{
            width: 350px;
            height: 350px;
        }
    }

    @media(max-width: 899px) and (min-width: 551px){
        .gallery{
            grid-template-columns: repeat(2, 250px);
        }
        .image-style{
            width: 250px;
            height: 250px;
        }

    }

    @media(max-width: 550px){
        .gallery{
            grid-template-columns: repeat(1, 300px);
        }
        .image-style{
            width: 300px;
            height: 300px;
        }


    }

</style>