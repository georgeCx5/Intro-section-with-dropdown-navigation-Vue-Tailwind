<script>
import imgMobile from '@/assets/images/image-hero-mobile.png';
import imgDesktop from '@/assets/images/image-hero-desktop.png';
import UpperButtons from '@/components/UpperBtn.vue';
import BrandLogo from '@/components/BrandLogo.vue';

export default {
  data() {
    return {
      logo: 'bg-[url("@/assets/images/logo.svg")]',
      iconMenu: 'bg-[url("@/assets/images/icon-menu.svg")]',
      iconCloseMenu: 'bg-[url("@/assets/images/icon-close-menu.svg")]',
      imgMobile,
      imgDesktop,
      showBar: false,
    }
  },
  components: {
    UpperButtons,
    BrandLogo,
  },
  methods: {
    barState() {
      this.showBar = !this.showBar;
    }
  }
}
</script>
<template>
  <body class=" relative flex flex-col items-center gap-6 font-epilogue">
    <!-- Close Menu -->
    <div v-show="showBar"
      class=" DT:hidden absolute right-0 flex flex-col gap-8 w-[240px] h-screen pt-[78px] px-6 bg-neo-white text-neo-gray text-[16px] leading-[26px] font-medium z-10">
      <div @click="barState()"
        :class="` absolute top-[22px] right-[22px] w-[24px] h-[24px] bg-contain ${iconCloseMenu} cursor-pointer`">
      </div>
      <div class=" flex flex-col items-start gap-4">
        <UpperButtons />
        <button class=" hover:text-neo-black">Careers</button>
        <button class=" hover:text-neo-black">About</button>
      </div>
      <div class=" flex flex-col items-center gap-4 text-[14px] leading-[16px]">
        <button class="hover:text-neo-black">Login</button>
        <button
          class=" w-full h-[42px] hover:text-neo-black outline outline-[1.5px] outline-neo-gray hover:outline-neo-black rounded-[14px]">Register</button>
      </div>
    </div>
    <!-- - -->
    <!-- Shadow when menu is open -->
    <div v-show="showBar" class=" DT:hidden absolute w-screen h-screen bg-neo-black bg-opacity-[.75] pointer-events-none">
    </div>
    <!-- - -->
    <nav class=" flex justify-between items-center w-full h-[35px] mt-[16px] px-[16px]">
      <div :class="` w-[87px] h-[28px] bg-contain ${logo}`"></div>
      <!-- Open Menu -->
      <div @click="barState()" v-show="!showBar"
        :class="` DT:hidden w-[28px] h-[18px] bg-cover ${iconMenu} cursor-pointer`">
      </div>
      <!-- - -->
    </nav>
    <main class=" flex flex-col DT:flex-row-reverse items-center DT:items-end gap-12 w-fit">
      <img class=" DT:hidden w-[375px]" :src="imgMobile" draggable="false" alt="imgMobile">
      <img class=" hidden DT:block w-[480px]" :src="imgDesktop" draggable="false" alt="imgDesktop">
      <div class=" flex flex-col gap-12 DT:gap-[108px] w-[343px] DT:w-[540px]">
        <div class=" flex flex-col items-center DT:items-start text-center DT:text-left">
          <h1
            class=" DT:w-[95%] mb-[16px] DT:mb-[48px] text-[36px] DT:text-[80px] leading-[42px] DT:leading-[80px] tracking-[-.5px] DT:tracking-[-1.11px] font-bold">
            Make remote work</h1>
          <p
            class=" DT:w-[445px] mb-[24px] DT:mb-[51px] text-[16px] DT:text-[18px] leading-[26px] DT:leading-[28px] font-medium">
            Get your team in sync, no matter your location. Streamline processes,
            create team rituals, and watch productivity soar.
          </p>
          <button
            class=" w-[136px] DT:w-[163px] h-[48px] DT:h-[56px] bg-neo-black hover:bg-neo-white text-neo-white hover:text-neo-black text-[16px] DT:text-[18px] leading-[26px] DT:leading-[28px] tracking-[-.22px] DT:tracking-[-.25px] font-bold rounded-[15px] outline outline-1 hover:outline-neo-black">Learn
            more</button>
        </div>
        <div class=" flex justify-between items-center DT:w-[478px]">
          <BrandLogo index="0" wSize="w-[81px] DT:w-[113px]" />
          <BrandLogo index="1" wSize="w-[53px] DT:w-[73px]" />
          <BrandLogo index="2" wSize="w-[64px] DT:w-[89px]" />
          <BrandLogo index="3" wSize="w-[59px] DT:w-[82px]" />
        </div>
      </div>
    </main>
  </body>
</template>