<template>
  <div class="main-container">
    <div class="sub-container">
      <img class="nav" src="/img/icons-and-links/traditional_header.png" />
      <img class="nav" src="img/icons-and-links/alien_icon.png" />
    </div>
    <div class="sub-container">
      <img class="nav" src="img/icons-and-links/blob_icon.png" />
      <img class="nav" src="/img/icons-and-links/digital_header.png" />
    </div>
    <div class="sub-container">
      <img class="nav" src="/img/icons-and-links/cone_icon.png" />
      <img class="nav" src="/img/icons-and-links/3d_header.png" />
      <img class="nav" src="/img/icons-and-links/cube_icon.png" />
    </div>
    <div class="sub-container">
      <img class="nav" src="/img/icons-and-links/about_header.png" />
      <img class="nav" src="/img/icons-and-links/face.png" />
    </div>
    <div class="sub-container">
      <img class="icon" src="/img/icons-and-links/instagram_icon.png" />
      <img class="icon" src="/img/icons-and-links/github_icon.png" />
      <img class="icon" src="/img/icons-and-links/itch_io_icon.png" />
      <img class="icon" src="/img/icons-and-links/redbubble_icon.png" />
      <img class="icon" src="/img/icons-and-links/email_icon.png" />
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
    margin-top: 5%;
    align-items: center;

  }
  .nav {
    align-self: center;
    max-height: 100px;
    max-width: auto;
  }
  .icon {
    align-self: center;
    max-height: 36px;
    max-width: auto;
  }
</style>

 

