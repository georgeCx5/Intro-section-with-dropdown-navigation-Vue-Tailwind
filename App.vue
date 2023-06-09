<script>
// import logo from '@/assets/images/logo.svg';
import imgMobile from '@/assets/images/image-hero-mobile.png';
import clientData from '@/assets/images/client-databiz.svg?url';
import clientAudio from '@/assets/images/client-audiophile.svg?url';
import clientMeet from '@/assets/images/client-meet.svg?url';
import clientMaker from '@/assets/images/client-maker.svg?url';
export default {
  data() {
    return {
      // imgMobile: 'bg-[url("@/assets/images/image-hero-mobile.png")]',
      logo: 'bg-[url("@/assets/images/logo.svg")]',
      iconMenu: 'bg-[url("@/assets/images/icon-menu.svg")]',
      imgMobile,
      clientData,
      clientAudio,
      clientMeet,
      clientMaker,
    }
  }
}
</script>
<template>
  <body class=" flex flex-col items-center gap-6 font-epilogue">
    <div class=" flex justify-between w-full mt-[16px] px-[16px]">
      <div :class="` w-[87px] h-[28px] bg-contain ${logo}`"></div>
      <div :class="` w-[32px] h-[18px] bg-contain ${iconMenu} cursor-pointer`"></div>
    </div>
    
    <main class=" flex flex-col items-center gap-12 w-fit">
      <img class=" w-[375px]" :src="imgMobile" alt="imgMobile">
      <div class=" flex flex-col gap-12">
        <div class=" flex flex-col items-center w-[343px] text-center">
          <h1 class=" mb-[16px] text-[36px] leading-[42px] tracking-[-.5px] font-bold">Make remote work</h1>
          <p class=" mb-[24px] text-[16px] leading-[26px] font-medium">
            Get your team in sync, no matter your location. Streamline processes,
            create team rituals, and watch productivity soar.
          </p>
          <button
            class=" w-[136px] h-[48px] bg-neo-black hover:bg-neo-white text-neo-white hover:text-neo-black text-[16px] leading-[26px] tracking-[-.22px] font-bold rounded-[15px] outline outline-1 hover:outline-neo-black">Learn
            more</button>
        </div>
        <div class=" flex justify-between items-center">
          <img class=" w-[81px]" :src="clientData" alt="clientData">
          <img class=" w-[53px]" :src="clientAudio" alt="clientAudio">
          <img class=" w-[64px]" :src="clientMeet" alt="clientMeet">
          <img class=" w-[59px]" :src="clientMaker" alt="clientMaker">
        </div>
      </div>
    </main>
  </body>
</template>