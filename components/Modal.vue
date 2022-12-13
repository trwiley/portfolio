<template>
    <div>
        <div class="modal-background" :style="modalShown ? 'display: block' : 'display: none'" @click="hideModal"></div>
      
        <div class="modal border-style" :style="modalShown ? 'display: block' : 'display: none'">
            <div class="close-icon">
                <img src="img/icons-and-links/close.png" alt="close" @click="hideModal"/>
            </div>
            
            
            <div class="container">
                <div class="item">
                    <img :src="require(`../assets/${artInfo.imgUrl}`)" class="image-style"/>
                </div>
                <div class="item">
                    <h2>{{ artInfo.title }}</h2>
                    <h3>Year: {{ artInfo.year }}</h3>
                    <h3>Medium: {{ artInfo.medium }}</h3>
                    <p v-if="descriptionExists">{{ artInfo.description }}</p>
                </div>
            </div>
           
        </div>
    </div>
</template>

<script>
export default{
    name: "Modal",
    props: {
        hideModal: Function,
        modalShown: Boolean,
        artInfo: Object
    },
    methods: {
        descriptionExists() {
            return(this.artInfo.description !== undefined);
        }
    }  
}
</script>
<style scoped>
.modal {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin: auto;
    background-color: #FBF9EA;
    box-sizing: border-box;
    z-index: 9999;
    height: 90%;
    width: 75%;
    overflow-y: scroll;
    scrollbar-width: thin;
    scrollbar-color: #26318A #228D93;
 
}
.modal::-webkit-scrollbar {
    width: 20px;
}

.modal::-webkit-scrollbar-track {
    background: #26318A;
}
  
.modal::-webkit-scrollbar-thumb {
    background-color: #228D93; 
    border-radius: 20px;
    border: 3px solid #26318A;
}

.modal-background {
	width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,0.5);
    position: fixed;
    top: 0;
    left: 0;
    z-index: 9998;
    
}

.close-icon {
    margin: 12px;
}
.close-icon:hover{
    cursor: pointer;
}

.image-style{
    width: 500px;
    height: auto;
}
.container{
    display: flex;
    flex-direction: row;
}
.item{
    margin: 36px;
}


</style>