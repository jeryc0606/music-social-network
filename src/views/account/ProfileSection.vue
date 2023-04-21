
<template>
    <div class="container flex max-w-4xl mx-auto mt-10">
       <div class="w-1/3">
        <img class="w-full h-auto rounded-lg shadow-lg" src="https://via.placeholder.com/500" alt="">
       </div> 
       <div class="w-full pl-4">
            <div class="flex">
                <div class="w-1/2">
                    <h1 class="text-2xl text-left text-gray-900 md:text-4xl" > 
                        Jeryc
                    </h1>
                    <span class="text-gray-700 text-md">
                        <i><b>london UK</b></i>
                    </span>
                </div>
                <div class="w-1/2 mt-2">
                   <RouterLinkButton
                    btnText="Edit Profile"
                    color="green"
                    url="/account/edit-profile"
                   />
                </div>
            </div>
            <ProfileInfoSection/>
            <ProfileAboutSection/>
       </div>
    </div>
    <SongsSection />
    <YoutubeVideoSection />
    <PostSection/>
</template>
<script setup>
    import RouterLinkButton from '../../components/global/RouterLinkButton';
    import ProfileInfoSection from '../../components/Partials/profile/ProfileInfoSection.vue';
    import ProfileAboutSection from '../../components/Partials/profile/ProfileAboutSection.vue';
    import SongsSection from '../../components/Partials/profile/SongsSection.vue';
    import YoutubeVideoSection from '../../components/Partials/profile/YoutubeVideoSection.vue';
    import PostSection from '../../components/Partials/profile/PostSection.vue';
    

</script>