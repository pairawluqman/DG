<template>
  <div
    class="layout-padding layout-container flex items-center justify-between flex-wrap-reverse gap-y-8"
  >
    <div class="flex gap-3 items-center">
      <img
        src="https://www.dubaiglobal-ce.com/images/SKYSCRAPER-EPS-10.png"
        alt=""
        class="w-[60px] ml-11 my-6"
      />
      <div class="">
        <p
          class="text-lg font-extrabold ltr:uppercase tracking-wider uppercase text-[#3a7c94] hidden sm:flex"
        >
          Dubai International
        </p>
        <p
          class="text-sm hidden sm:flex text-[#3a7c94] ltr:uppercase font-medium tracking-[0.4em] uppercase"
        >
          Exchange Company
        </p>
      </div>
    </div>
    <div class="xl:flex gap-10 justify-center items-center hidden">
      <div class="relative px-2">
        <NuxtLink to="/" exact-active-class="font-bold">
          <h6 class="md:text-sm text-xs text-neutral-900 ltr:uppercase">
            HOME
          </h6>
          <div
            class="w-full h-[5px] rounded-full z-[1] bg-yellow-500 absolute start-0 -bottom-[46px]"
            v-if="$route.path === '/'"
          ></div>
        </NuxtLink>
      </div>
      <div class="relative px-2">
        <NuxtLink to="/service" exact-active-class="font-bold">
          <h6 class="md:text-sm text-xs text-neutral-900 ltr:uppercase">
            SERVICE
          </h6>
          <div
            class="w-full h-[5px] rounded-full bg-yellow-500 absolute start-0 -bottom-[46px] z-[1]"
            v-if="$route.path === '/service'"
          ></div>
        </NuxtLink>
      </div>
      <div class="relative px-2">
        <NuxtLink to="/about" exact-active-class="font-bold">
          <h6 class="md:text-sm text-xs text-neutral-900 ltr:uppercase">
            ABOUT US
          </h6>
          <div
            class="w-full h-[5px] rounded-full bg-yellow-500 absolute start-0 -bottom-[46px] z-[1]"
            v-if="$route.path === '/about'"
          ></div>
        </NuxtLink>
      </div>
      <div class="relative px-2">
        <NuxtLink to="/contact" exact-active-class="font-bold">
          <h6 class="md:text-sm text-xs text-neutral-900 ltr:uppercase">
            CONTACT US
          </h6>
          <div
            class="w-full h-[5px] rounded-full bg-yellow-500 absolute start-0 -bottom-[46px] z-[1]"
            v-if="$route.path === '/contact'"
          ></div>
        </NuxtLink>
      </div>
    </div>
    <div class="flex justify-end gap-4 md:gap-6 xl:w-[340px]">
      <NuxtLink
        to="/contact"
        class="w-fit h-11 ps-1 pe-6 rounded-full border border-[#3a7c94]/30 md:flex items-center gap-2 md:gap-3 group hover:bg-[#3a7c94] hover:text-white transition-all duration-300 hidden"
      >
        <div class="w-9 aspect-square rounded-full flex-center">
          <div
            class="w-9 h-9 rounded-full flex items-center justify-center bg-[#3a7c94]/15 group-hover:bg-white/50 transition-all duration-300"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 36 36"
            >
              <path
                fill="#3a7c94"
                d="M15.22 20.64a20.4 20.4 0 0 0 7.4 4.79l3.77-3a.67.67 0 0 1 .76 0l7 4.51a2 2 0 0 1 .33 3.18l-3.28 3.24a4 4 0 0 1-3.63 1.07a35.1 35.1 0 0 1-17.15-9A33.8 33.8 0 0 1 1.15 8.6a3.78 3.78 0 0 1 1.1-3.55l3.4-3.28a2 2 0 0 1 3.12.32L13.43 9a.63.63 0 0 1 0 .75l-3.07 3.69a19.75 19.75 0 0 0 4.86 7.2"
                class="clr-i-solid clr-i-solid-path-1"
              />
              <path fill="none" d="M0 0h36v36H0z" />
            </svg>
          </div>
        </div>

        <h6
          class="md:text-sm text-xs font-black text-[#3a7c94] group-hover:text-white"
        >
          Call us +9647760848796
        </h6>
      </NuxtLink>
      <div class="relative mr-1">
        <div
          class="h-11 w-11 rounded-full border border-[#3a7c94]/30 flex justify-center items-center cursor-pointer"
        >
          <p class="text-xs text-[#3a7c94] font-black uppercase">en</p>
        </div>
      </div>
      <div class="relative mr-3 flex lg:hidden z-999">
        <div
          @click="handleNav"
          class="h-11 w-11 rounded-full border border-[#3a7c94]/30 flex justify-center items-center cursor-pointer"
        >
          <svg
            v-if="!nav"
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            viewBox="0 0 24 24"
          >
            <path
              fill="#3a7c94"
              stroke="#3a7c94"
              stroke-linecap="round"
              stroke-width="1.5"
              d="M20 7H4m16 5H4m16 5H4"
            />
          </svg>
          <svg
            v-if="nav"
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            viewBox="0 0 24 24"
          >
            <path
              fill="#3a7c94"
              stroke="#3a7c94"
              d="m12 13.4l-4.9 4.9q-.275.275-.7.275t-.7-.275t-.275-.7t.275-.7l4.9-4.9l-4.9-4.9q-.275-.275-.275-.7t.275-.7t.7-.275t.7.275l4.9 4.9l4.9-4.9q.275-.275.7-.275t.7.275t.275.7t-.275.7L13.4 12l4.9 4.9q.275.275.275.7t-.275.7t-.7.275t-.7-.275z"
            />
          </svg>
        </div>
      </div>
    </div>
  </div>
  <div class="w-full hidden h-px bg-[#3a7c94] mt-4"></div>

  <div
    v-if="nav"
    class="fixed z-[9999] top-0 left-0 h-screen w-full bg-[#3a7c94] flex"
  >
    <div class="flex flex-col justify-center items-center flex-grow">
      <div class="flex flex-col gap-2 flex-wrap text-center">
        <NuxtLink to="/" exact-active-class="font-bold" class="relative">
          <h6 class="md:text-lg text-lg text-neutral-900 ltr:uppercase">
            HOME
          </h6>
        </NuxtLink>

        <NuxtLink to="/service" exact-active-class="font-bold" class="relative">
          <h6 class="md:text-lg text-lg text-neutral-900 ltr:uppercase">
            SERVICE
          </h6>
        </NuxtLink>

        <NuxtLink to="/about" exact-active-class="font-bold" class="relative">
          <h6 class="md:text-lg text-lg text-neutral-900 ltr:uppercase">
            ABOUT US
          </h6>
        </NuxtLink>

        <NuxtLink to="/contact" exact-active-class="font-bold">
          <h6 class="md:text-lg text-lg text-neutral-900 ltr:uppercase">
            CONTACT US
          </h6>
        </NuxtLink>
      </div>
    </div>

    <div class="absolute top-0 right-0 m-3 flex lg:hidden">
      <div
        @click="handleNav"
        class="h-11 w-11 mt-5 bg-white rounded-full border border-[#3a7c94]/30 flex justify-center items-center cursor-pointer"
      >
        <svg
          v-if="!nav"
          xmlns="http://www.w3.org/2000/svg"
          width="20"
          height="20"
          viewBox="0 0 24 24"
        >
          <path
            fill="#3a7c94"
            stroke="#3a7c94"
            stroke-linecap="round"
            stroke-width="1.5"
            d="M20 7H4m16 5H4m16 5H4"
          />
        </svg>
        <svg
          v-if="nav"
          xmlns="http://www.w3.org/2000/svg"
          width="20"
          height="20"
          viewBox="0 0 24 24"
        >
          <path
            fill="#3a7c94"
            stroke="#3a7c94"
            d="m12 13.4l-4.9 4.9q-.275.275-.7.275t-.7-.275t-.275-.7t.275-.7l4.9-4.9l-4.9-4.9q-.275-.275-.275-.7t.275-.7t.7-.275t.7.275l4.9 4.9l4.9-4.9q.275-.275.7-.275t.7.275t.275.7t-.275.7L13.4 12l4.9 4.9q.275.275.275.7t-.275.7t-.7.275t-.7-.275z"
          />
        </svg>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { ref, watch, onMounted, onUnmounted } from "vue";

export default {
  setup() {
    const nav = ref<boolean>(false);

    const handleNav = () => {
      nav.value = !nav.value;
    };

    const toggleBodyScroll = () => {
      if (nav.value) {
        document.body.classList.add("no-scroll");
      } else {
        document.body.classList.remove("no-scroll");
      }
    };

    watch(nav, toggleBodyScroll);

    onMounted(() => {
      document.body.classList.remove("no-scroll");
    });

    onUnmounted(() => {
      document.body.classList.remove("no-scroll");
    });

    return {
      nav,
      handleNav,
    };
  },
};
</script>
