<template>
  <aside class="sidebar">
    <img
      class="logo m-t-40"
      src="https://global-uploads.webflow.com/5ed5b60be1889f546024ada0/5ed8a32c8e1f40c8d24bc32b_Aspire%20Logo%402x.png" />
    <div class="font-14 m-t-20 color-indigo-4">
      Trusted way of banking for 3000+ SMEs and startups in Singapore
    </div>
    <div class="options color-white-hard m-t-40">
      <div class="padding-20 flex cursor-pointer">
        <img
          class="b-r-10"
          src="logo.jpeg"
          alt="user"
          height="20px"
          width="20px">
        <div class="m-l-10">
          Home
        </div>
      </div>
      <div class="padding-20 flex cursor-pointer">
        <img
          class="b-r-10"
          src="logo.jpeg"
          alt="user"
          height="20px"
          width="20px">
        <div class="m-l-10 active">
          Cards
        </div>
      </div>
      <div class="padding-20 flex cursor-pointer">
        <img
          class="b-r-10"
          src="logo.jpeg"
          alt="user"
          height="20px"
          width="20px">
        <div class="m-l-10">
          Payment
        </div>
      </div>
      <div class="padding-20 flex cursor-pointer">
        <img
          class="b-r-10"
          src="logo.jpeg"
          alt="user"
          height="20px"
          width="20px">
        <div class="m-l-10">
          Credit
        </div>
      </div>
      <div class="padding-20 flex cursor-pointer">
        <img 
          class="b-r-10"
          src="logo.jpeg"
          alt="user"
          height="16px"
          width="16px">
        <div class="m-l-10">
          Setting
        </div>
      </div>
    </div>
  </aside>
</template>

<script>
  export default {
    name: 'Sidebar'
  }
</script>

<style lang="scss" scoped>
  @import '@/variables/utilities';
  .sidebar {
    background-color: #0C365A;
    height: 100vh;
    padding: 0 40px;
    width: 17%;
    position: fixed;

    @include mobile {
      display: none;
    }

    .logo {
      height: 30px;
      width: 120px;
    }
    .active {
      color: #01D167;
      font-weight: 600;
    }
  }
</style>