<template>
  <headTag></headTag>
  <body>
    <topNav></topNav>
    <SideBar></SideBar>
    <mainContent :video-list="videoList" ></mainContent>

  </body>  
</template>

<script setup>
  import topNav from './components/topNav.vue';
  import headTag from './components/headTag.vue';
  import SideBar from './components/sideBar.vue';
  import mainContent from './components/mainContent.vue';

  const videoList = [
    {profilePic: "https://i.pinimg.com/236x/85/7c/40/857c4052f8fd60303bebf8e372bc2f79.jpg" ,
        video: "https://videos.pexels.com/video-files/29969740/12860951_360_640_30fps.mp4",
        like: 201,
        comments: 311,
        save: 50,
        shares:203
    },
    {profilePic: "https://i.pinimg.com/474x/2b/25/28/2b2528d577b63960e3a30b254b3755c8.jpg" ,
        video: "https://videos.pexels.com/video-files/28167731/12315786_360_640_25fps.mp4",
        like: 2876,
        comments: 389,
        save: 90,
        shares:1093
    },
    {profilePic: "https://i.pinimg.com/236x/1e/ae/67/1eae674712ab8d73f05256951f4fa098.jpg" ,
        video: "https://videos.pexels.com/video-files/17844988/17844988-sd_360_640_30fps.mp4",
        like: 561,
        comments: 39,
        save: 489,
        shares: 233
    },
    {profilePic: "https://i.pinimg.com/236x/e8/e6/41/e8e64141f4c0ae39c32f9701ccea9a2e.jpg" ,
        video: "https://videos.pexels.com/video-files/26256159/11943214_360_640_60fps.mp4",
        like:571,
        comments: 321,
        save: 73,
        shares:85
    },
    {profilePic: "https://i.pinimg.com/236x/6d/3e/b8/6d3eb8147fdcdd571952e667b6690801.jpg",
        video:  "https://videos.pexels.com/video-files/6547499/6547499-sd_360_640_25fps.mp4",
        like: 1334,
        comments: 123,
        save: 520,
        shares: 73
    }
]

</script>