<template>
  <headTag></headTag>

  <body>
    <topNav></topNav>
    <SideBar></SideBar>
    <mainContent></mainContent>

  </body>  
</template>

<script setup>
  import topNav from './components/topNav.vue';
  import headTag from './components/headTag.vue';
  import SideBar from './components/sideBar.vue';
  import mainContent from './components/mainContent.vue';
</script>