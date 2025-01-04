<template>
    <section 
        class="sideBar"
        v-if="isFullScreen"
        >

        <div class="icons">
            <button id="home">
                <img src="../assets/home.png" alt="home icon">
                <p>For You</p>
            </button>
            <button id="following">
                <img src="../assets/followers.png" alt="following icon">
                <p>Following</p>
            </button>
            <button id="live">
                <img src="../assets/video.png" alt="live icon">
                <p>Live</p>
            </button>
        </div>

        <div class="suggested-accounts">
            <h2>Suggested Accounts</h2>

            <button class="contains-suggest-acc">
                <img 
                    src="../assets/profile2.jpeg" 
                    alt="profile picture"
                    id="profile2"
                >
                
                <div>
                    <div id="username">
                        <h3>BlanK</h3>
                        <img 
                            src="../assets/verified.png"    
                            alt="verified-logo"
                            id="verified"
                        >
                    </div>

                    <p>Mediore_ed</p>
                </div>
            </button>

            <button class="see-all">
                    See all
            </button>
        </div>

        <div class="following-accounts">
            <h2>Following Accounts</h2>

            <button class="contains-suggest-acc">
                <img 
                    src="../assets/profile1.jpeg" 
                    alt="profile picture"
                    id="profile1"
                >
                
                <div>
                    <div id="username">
                        <h3>Kiama&lt;3</h3>
                        <img 
                            src="../assets/verified.png"    
                            alt="verified-logo"
                            id="verified"
                        >
                    </div>

                    <p>Kiama@Codm</p>
                </div>
            </button>
            
            <button class="see-all">
                    See more
            </button>
        </div>

        <div class="copywrite">
            <p>
                TikTok respects the intellectual property (IP) rights of others,
                 and we expect you to do the same.
            </p>
            <p>
                 Our Terms of Service and Community Guidelines do not allow posting, 
                 sharing, or sending any content that violates or infringes upon 
                 someone else’s copyrights, trademarks or other IP rights. 
            </p>
            <p>
                <em> © 2024 TikTok </em>
            </p>
        </div>
    </section>

    <section 
        class="sideBar"
        v-if="!isFullScreen"
        id="mobileSideBar"
        >

        <div class="icons">
            <button id="home">
                <img src="../assets/home.png" alt="home icon">
                
            </button>
            <button id="following">
                <img src="../assets/followers.png" alt="following icon">
                
            </button>
            <button id="live">
                <img src="../assets/video.png" alt="live icon">
               
            </button>
        </div>

        <div class="suggested-accounts">
            <h2>Suggested Accounts</h2>

            <button class="see-all">
                    See all
            </button>
        </div>

        <div class="following-accounts">
            <h2>Following Accounts</h2>

            <button class="see-all">
                    See more
            </button>
        </div>

        <div class="copywrite">
            <p>
                © 2024 TikTok
            </p>
        </div>
    </section>

</template>

<script setup>
    import { onMounted, onUnmounted, ref } from 'vue';

    const isFullScreen = ref(true);

    const checkViewPort = () => {
        if(window.innerWidth > 1000) {
            isFullScreen.value = true;
        }else{
            isFullScreen.value = false;
        }
    };

    onMounted(() =>{
        window.addEventListener('resize', checkViewPort);
        checkViewPort();
    });

    onUnmounted(() => {
        window.removeEventListener('resize', checkViewPort);
    });
</script>