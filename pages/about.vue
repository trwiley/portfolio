<template>
    <div>
        <BackArrow />
        <div class="header-align">
            <img src="/img/icons-and-links/about_header.png" alt="About" class="header-style"/>
            <p>Taylor Wiley is a programmer and artist who experiments in different analog and digital mediums. She is inspired by things such as, but not limited to: virtual pets, retro video games (the more obscure the better), 90s Japanese multimedia programs, weird thrift store finds, endless music rabbit holes, and random art books found in libraries and local bookstores. She lives in South Bend, IN with her cat. </p>
        </div>  
    </div>
   
</template>

<script>
import BackArrow from '~/components/BackArrow.vue';
export default{
    name: 'AboutPage',
    components: {
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
