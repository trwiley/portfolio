<template>
    <div class="header-align">
        <img src="/img/icons-and-links/about_header.png" alt="About" class="header-style"/>
        <p>Taylor Wiley is a programmer and artist who experiments in different analog and digital mediums. She is inspired by things such as, but not limited to: virtual pets, retro video games (the more obscure the better), 90s Japanese multimedia programs, weird thrift store finds, endless music rabbit holes, and random art books found in libraries and local bookstores. She lives in South Bend, IN with her cat. </p>
        <div style="text-align: left; margin: 36px">
            <NuxtLink to="/">
                <h2>back</h2>
            </NuxtLink>
        </div>
    </div>  
</template>

<script>
export default{
    name: 'AboutPage'
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
