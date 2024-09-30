<template>
  <div class="relative flex w-full h-[85vh] overflow-hidden z-0">
    <div class="absolute inset-0 flex justify-between items-center">
      <div
        class="bg-gradient-to-r from-[#3a7c94] to-transparent w-1/6 h-full"
      ></div>
      <div
        class="bg-gradient-to-l from-[#3a7c94] to-transparent w-1/6 h-full"
      ></div>
    </div>

    <div class="w-full h-full">
      <img
        v-if="!isVideoPlaying"
        class="object-cover w-full h-full"
        src="https://asset.dubaiglobal-ce.com/images/blond-woman-texting-on-her-phone-2023-11-27-05-08-38-utc.png"
        alt=""
      />
      <video
        v-if="isVideoPlaying"
        class="object-cover w-full h-full"
        autoplay
        muted
        loop
      >
        <source
          src="https://asset.dubaiglobal-ce.com/videos/Handshake-Thank-You-And-Business-People-Meeting-F-2023-11-27-05-09-22-Utc.mp4"
          type="video/mp4"
        />
        Your browser does not support the video tag.
      </video>
      <div
  class="absolute inset-0 -top-10 flex items-center justify-center text-white text-lg lg:text-4xl font-bold"
>
  <div class="lg:w-[45rem] w-full">
    <p class="text-center">
      Navigate global markets with our
      <span class="text-yellow-300"> trusted </span>
      <div class="text-center">
        <span>currency exchange services</span>
      </div>
    </p>&nbsp;
    <p class="text-center text-sm z-1">
      We strive to provide efficient solutions tailored to your financial needs.
    </p>
    <div class="flex justify-center self-center mt-4 text-lg group">
      <NuxtLink to="/" class="flex flex-nowrap w-48 items-center p-2  bg-white border-[#3a7c94] text-[#3a7c94] rounded-full">
        <p class="ml-6 text-sm">Our Mission</p> &nbsp; <span class="bg-[#3a7c94] ml-10 scale-125 rounded-full  transform transition-all group-hover:scale-100 group-hover:opacity-70"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="white" d="M8.025 22L6.25 20.225L14.475 12L6.25 3.775L8.025 2l10 10z"/></svg></span>
      </NuxtLink>
    </div>
  </div>
</div>
    </div>

    <button
      @click="showPrevious"
      class="absolute left-5 top-1/2 transform -translate-y-1/2 bg-[#3a7c94] bg-opacity-30 text-white w-12 h-12 flex items-center justify-center backdrop-brightness-125 hover:bg-opacity-50 hover:opacity-100 rounded-full"
    >
      <svg
        class=""
        xmlns="http://www.w3.org/2000/svg"
        width="32"
        height="32"
        viewBox="0 0 24 24"
        opacity="100"
      >
        <path
          fill="currentColor"
          d="M16 22L6 12L16 2l1.775 1.775L9.55 12l8.225 8.225z"
        />
      </svg>
    </button>
    <button
      @click="showNext"
      class="absolute right-5 top-1/2 transform -translate-y-1/2 bg-[#3a7c94] bg-opacity-30 text-white w-12 h-12 flex items-center justify-center backdrop-brightness-125 hover:bg-opacity-50 hover:opacity-100 rounded-full"
    >
      <svg
        class=""
        xmlns="http://www.w3.org/2000/svg"
        width="32"
        height="32"
        viewBox="0 0 24 24"
        opacity="100"
      >
        <path
          fill="currentColor"
          d="M8.025 22L6.25 20.225L14.475 12L6.25 3.775L8.025 2l10 10z"
        />
      </svg>
    </button>
  </div>
</template>

<script lang="ts">
import { ref, onMounted, onBeforeUnmount } from "vue";

export default {
  setup() {
    const isVideoPlaying = ref<boolean>(false);
    let sliderInterval: ReturnType<typeof setInterval> | null = null;
    const timerDuration = ref<number>(isVideoPlaying.value ? 14000 : 5000);

    const startSlider = (): void => {
      sliderInterval = setInterval(() => {
        isVideoPlaying.value = !isVideoPlaying.value;
        timerDuration.value = isVideoPlaying.value ? 14000 : 5000;
        resetInterval();
      }, timerDuration.value);
    };

    const resetInterval = (): void => {
      if (sliderInterval) {
        clearInterval(sliderInterval);
      }
      startSlider();
    };

    const showNext = (): void => {
      isVideoPlaying.value = !isVideoPlaying.value;
      timerDuration.value = isVideoPlaying.value ? 14000 : 5000;
      resetInterval();
    };

    const showPrevious = (): void => {
      isVideoPlaying.value = !isVideoPlaying.value;
      timerDuration.value = isVideoPlaying.value ? 14000 : 5000;
      resetInterval();
    };

    onMounted((): void => {
      startSlider();
    });

    onBeforeUnmount((): void => {
      if (sliderInterval) {
        clearInterval(sliderInterval);
      }
    });

    return {
      isVideoPlaying,
      showNext,
      showPrevious,
    };
  },
};
</script>
