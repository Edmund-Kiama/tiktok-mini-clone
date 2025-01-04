<template>
    <section>
        <div 
        class="reels-container"
        v-for="(video, index) in props.videoList"
        :key="index"
        >
            <div class="container">
                <video 
                    :src="video.video"
                    class="car1-video"
                    autoplay
                    loop
                    muted
                ></video>
                <div class="interact-icons">
                    <div class="profile">
                        <img 
                            :src="video.profilePic"
                            alt="profile-picture"
                            class="profile-pic"
                        >
                        <p><strong>+</strong></p>
                    </div>
                    <div class="like">
                        <div class="image">
                            <img 
                                src="../assets/heart.png" 
                                alt="like-logo"
                                class="like-logo"
                            >
                        </div>
                        <p>{{ video.like }}</p>
                    </div>
                    <div class="comment">
                        <div class="image">
                            <img 
                                src="../assets/chat-bubble.png" 
                                alt="comment-logo"
                                class="comments"
                            > 
                            </div>
                        <p>{{ video.comments }}</p>
                    </div>
                    <div class="save">
                        <div class="image">
                            <img 
                                src="../assets/bookmark.png" 
                                alt="save-logo"
                                class="saves"
                            > 
                            </div> 
                        <p>{{ video.save }}</p>
                    </div>
                    <div class="share">
                        <div class="image">
                            <img 
                                src="../assets/share.png" 
                                alt="share-logo"
                                class="shares"
                            > 
                            </div> 
                        <p>{{ video.shares }}</p>
                    </div>
                </div>
            </div> 
        </div> 
    </section>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    videoList:{
        type: Array,
        Required: true
    }
});
</script>