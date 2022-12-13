<template>
    <div>
        <div class="modal-background" :style="modalShown ? 'display: block' : 'display: none'"></div>
        <div class="modal" :style="modalShown ? 'display: block' : 'display: none'">
            <button @click="hideModal">close</button>
        </div>
    </div>
</template>

<script>
export default{
    name: "Modal",
    props: {
        hideModal: Function,
        modalShown: Boolean
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
    height: 200px;
    width: 200px;
}
.modal > p {
	padding: 15px;
    margin: 0;
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

.modal-show {
    display: block
}
</style>