<template>
    <nav>
        <img 
            class="tiktok-logo"
            src="../assets/long-logo.png"
            >

        <div class="search">
            <input type="text" name="search" id="search" placeholder="Search">
            <button type="submit"><i class="fa fa-search"></i></button>
        </div>

        <div 
            v-if="isFullScreen"
            class="details"
        >
            <button class="upload"> 
                <span>+</span>
                Upload
            </button>
            <button class="send">
                <img 
                    src="../assets/send.webp" 
                    alt="send"
                    id="send"
                > 
            </button>
            <button class="messages">
                <img 
                    src="../assets/message.png" 
                    alt="messages"
                    id="messages"
                    width="40px"
                >
            </button>
            <img 
                src="../assets/profile.webp" 
                alt="Profile Picture"
                id="profile-picture"
            >               
            
        </div>
        <div 
            v-if="!isFullScreen"
            class="details-mobile"
        >
            <button>
                <img 
                    src="../assets/3-dots.png" 
                    alt="3-dots"
                    width="30px"
                    @click="dropDown"
                >
            </button>
        </div>

    </nav>
    <div
        v-if="showDropDown"
    >
        <div
            class="drop-down"
        >
            <button class="mobile-upload"> 
                <span>+</span>
                Upload
            </button>
            <button class="mobile-send">
                <img 
                    src="../assets/send.webp" 
                    alt="send"
                    id="mobile-send"
                >
                <p>Send</p>
            </button>
            <button class="mobile-messages">
                <img 
                    src="../assets/message.png" 
                    alt="messages"
                    id="mobile-messages"
                    width="40px"
                >
                <p>Chats</p>
            </button>
            <div class="profile">
                <img 
                    src="../assets/profile.webp" 
                    alt="Profile Picture"
                    id="mobile-profile-picture"
                >
                <p>@LeBlanc</p>
            </div>
        </div>           
    </div>
</template>

<script setup>
    import { onMounted, onUnmounted, ref } from 'vue';

    const isFullScreen = ref(true);
    const showDropDown = ref(false);

    const checkViewPort = () => {
        if(window.innerWidth > 1000) {
            isFullScreen.value = true;
        }else{
            isFullScreen.value = false;
        }
    };
    const dropDown = () => {
        return showDropDown.value = !showDropDown.value
    };

    onMounted(() =>{
        window.addEventListener('resize', checkViewPort);
        checkViewPort();
    });

    onUnmounted(() => {
        window.removeEventListener('resize', checkViewPort);
    });
</script>