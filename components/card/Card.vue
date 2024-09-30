<template>
  <div class="h-screen w-full mt-3 flex flex-col justify-center mb-20 lg:mb-5">
    <div
      class="bg-[#faf6e6] w-11/12 flex flex-col lg:flex-row items-center justify-between rounded-lg p-4 mx-auto"
    >
      <div
        class="relative w-full lg:w-1/2 lg:order-2 rounded-lg overflow-hidden"
      >
        <img
          class="w-full object-cover mt-0 lg:mt-0"
          src="https://asset.dubaiglobal-ce.com/images/luggage-travel-tourism-concept-closeup-of-yellow-2023-11-27-05-11-09-utc.png"
          alt="Travel Image"
        />
        <div class="absolute inset-0 bg-yellow-400 opacity-10"></div>
      </div>

      <div class="lg:w-1/2 w-full text-justify mt-4 lg:mt-0 lg:ml-4 lg:order-1">
        <h2 class="font-bold lg:text-3xl text-lg mb-2 uppercase">
          Money Exchange During Travel
        </h2>
        <p class="lg:w-3/4">
          We are a currency exchange company that is licensed to work by the
          Iraqi finance ministry and classified as an A-type currency exchange
          company. As a top currency exchange provider, we are committed to
          providing quick, safe, and practical currency exchange services. Our
          goal is to provide travelers, companies, and people with affordable
          exchange rates and top-notch customer service.
        </p>
        <div
          class="flex justify-start lg:justify-start mt-10 mb-4 lg:mb-0 lg:order-3"
        >
          <NuxtLink
            to="/"
            class="bg-yellow-400 w-48 p-2 rounded-full flex items-center justify-center group"
          >
            <span class="text-white ml-9">Read More</span>
            <span
              class="ml-5 bg-white border-0 scale-110 group-hover:scale-100 group-hover:opacity-80 transition-all rounded-full w-8 h-8 flex items-center justify-center"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
              >
                <path
                  fill="#FFEE58"
                  d="m14.475 12l-7.35-7.35q-.375-.375-.363-.888t.388-.887t.888-.375t.887.375l7.675 7.7q.3.3.45.675t.15.75t-.15.75t-.45.675l-7.7 7.7q-.375.375-.875.363T7.15 21.1t-.375-.888t.375-.887z"
                />
              </svg>
            </span>
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>
