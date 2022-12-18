<template>
  <div class="main-container">
    <div class="sub-container">
      <NuxtLink to="/traditional">
        <img class="nav" src="/img/icons-and-links/traditional_header.png" />
      </NuxtLink>  
      <img class="nav" src="img/icons-and-links/alien_icon.png" />
    </div>
    <div class="sub-container">
      <img class="nav" src="img/icons-and-links/blob_icon.png" />
      <NuxtLink to="/digital">
        <img class="nav" src="/img/icons-and-links/digital_header.png" />
      </NuxtLink> 
    </div>
    <div class="sub-container">
      <img class="nav" src="/img/icons-and-links/cone_icon.png" />
      <NuxtLink to="/3d">
        <img class="nav" src="/img/icons-and-links/3d_header.png" />
      </NuxtLink>
     
      <img class="nav" src="/img/icons-and-links/cube_icon.png" />
    </div>
    <div class="sub-container">
      <NuxtLink to="/about">
        <img class="nav" src="/img/icons-and-links/about_header.png" />
      </NuxtLink>
      <img class="nav" src="/img/icons-and-links/face.png" />
    </div>
    <br />
    <div class="sub-container">
      <a href="https://www.instagram.com/uncool_and_uncouth/">
        <img class="icon" src="/img/icons-and-links/instagram_icon.png" />
      </a> 
      <a href="https://github.com/trwiley">
        <img class="icon" src="/img/icons-and-links/github_icon.png" />
      </a>
      <a href="https://uncoolanduncouth.itch.io/">
        <img class="icon" src="/img/icons-and-links/itch_io_icon.png" />
      </a>
      <a href="https://www.redbubble.com/people/uncool-uncouth/shop">
        <img class="icon" src="/img/icons-and-links/redbubble_icon.png" />
      </a>
      <a href="mailto:taylor.r.wiley@gmail.com">
        <img class="icon" src="/img/icons-and-links/e-mail_icon.png" />
      </a>  
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style>
 .main-container {
    display: flex;
    flex-direction: column;
    align-items: center;

  }
  .nav {
    align-self: center;
  }
  .icon {
    align-self: center;
    max-height: 36px;
    max-width: auto;
  }

  @media (min-width: 526px){
    .main-container{
      margin-top: 7%;
    }
    .nav{
      max-height: 100px;
      max-width: auto;
    }
  }

  @media (max-width: 525px){
    .main-container{
      margin-top: 40%;
    }
    .nav{
      max-height: 65px;
      max-width: auto;
    }
  }
</style>

 

