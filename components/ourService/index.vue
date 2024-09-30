<template>
  <div class="mb-20 w-full h-full">
    <p
      class="uppercase text-[#3a7c94] flex justify-center items-center text-2xl font-bold"
    >
      Our Service
    </p>
    <swiper
      :slidesPerView="3"
      :spaceBetween="10"
      :pagination="{ clickable: true }"
      :loop="true"
      <!--
      Enable
      looping
      --
    >
      :modules="modules" class="mySwiper" >
      <swiper-slide v-for="(slide, index) in slideURLs" :key="index">
        <div class="relative w-full h-full group">
          <img
            class="w-full h-full rounded-xl scale-90 group-hover:scale-95 transition-transform duration-300"
            :src="slide.image"
            alt=""
          />
          <div
            class="absolute inset-0 bg-gradient-to-l from-[#3a7c94] to-transparent opacity-0 group-hover:opacity-0 transition-opacity duration-300 rounded-xl"
          ></div>
          <div
            class="absolute inset-0 bg-gradient-to-r from-[#3a7c94] to-transparent opacity-0 group-hover:opacity-50 transition-opacity duration-300 rounded-xl"
          ></div>
          <div
            class="absolute inset-0 flex gap-3 flex-col items-center justify-end text-white font-bold mb-20 hover:translate-y-[-20px] transition-all"
          >
            <p class="text-sm font-bold">{{ slide.text2 }}</p>
            <p class="text-sm w-3/4 text-center">{{ slide.text }}</p>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Pagination } from "swiper/modules";

interface Slide {
  image: string;
  text: string;
  text2: string;
}

export default defineComponent({
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const slideURLs: Slide[] = [
      {
        image:
          "https://asset.dubaiglobal-ce.com/images/woman-withdrawing-money-from-atm-finance-transfer-2023-11-27-05-22-18-utc.png",
        text: "Facilitate local money transfers with trusted currency exchange services, helping clients navigate global markets.",
        text2: "Local Money Transfer",
      },
      {
        image:
          "https://asset.dubaiglobal-ce.com/images/her-travel-documents-are-in-order-2023-11-27-05-28-58-utc.png",
        text2: "Currency Exchange",
        text: "Provide competitive exchange rates for a wide range of currencies to meet the needs of individuals, businesses, and travelers.",
      },
      {
        image:
          "https://asset.dubaiglobal-ce.com/images/woman-withdrawing-money-from-atm-finance-transfer-2023-11-27-05-22-18-utc.png",
        text: "Facilitate local money transfers with trusted currency exchange services, helping clients navigate global markets.",
        text2: "Local Money Transfer",
      },
      {
        image:
          "https://asset.dubaiglobal-ce.com/images/hands-showing-dollars-banknotes-2023-11-27-05-07-43-utc.png",
        text: "We strive to provide efficient solutions tailored to your financial needs.",
        text2: "International Money Transfer",
      },
    ];

    return {
      modules: [Pagination],
      slideURLs,
    };
  },
});
</script>
