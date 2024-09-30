<template>
  <div class="mt-10 h-full w-full mb-20 lg:mb-0">
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
      <div class="flex justify-center items-center">
        <div
          class="h-20 ml-2 mr-2 w-20 rounded-full border-2 flex justify-center items-center"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="32"
            height="32"
            viewBox="0 0 512 512"
          >
            <path
              fill="none"
              stroke="#3a7c94"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="32"
              d="M48.9 112.37C138.32 96.33 175.29 84.45 256 48c80.71 36.45 117.68 48.33 207.1 64.37C479.3 369.13 271.42 457.79 256 464c-15.42-6.21-223.3-94.87-207.1-351.63"
            />
            <path
              fill="#3a7c94"
              d="M256 48c80.71 36.45 117.68 48.33 207.1 64.37C479.3 369.13 271.42 457.79 256 464Z"
            />
          </svg>
        </div>
        <div class="ml-2 w-1/2 text-justify">
          <h2 class="font-bold text-lg mb-2">Know Your Customer</h2>
          <p>
            To confirm our clients' identities, comprehend their financial
            activity, and evaluate the possibility of money laundering or
            terrorist funding.
          </p>
        </div>
      </div>

      <div class="flex justify-center items-center">
        <div
          class="h-20 ml-2 mr-2 w-20 rounded-full border-2 flex justify-center items-center"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="40"
            height="32"
            viewBox="0 0 640 512"
          >
            <path
              fill="#3a7c94"
              d="M320 96a32 32 0 1 1-64 0a32 32 0 1 1 64 0m21.1 80C367 158.8 384 129.4 384 96c0-53-43-96-96-96s-96 43-96 96c0 33.4 17 62.8 42.9 80H224c-17.7 0-32 14.3-32 32s14.3 32 32 32h32v208h-48c-53 0-96-43-96-96v-6.1l7 7c9.4 9.4 24.6 9.4 33.9 0s9.4-24.6 0-33.9L97 263c-9.4-9.4-24.6-9.4-33.9 0L7 319c-9.4 9.4-9.4 24.6 0 33.9s24.6 9.4 33.9 0l7-7v6.1c0 88.4 71.6 160 160 160h160c8 0 15.9-.6 23.6-1.7c-4.8-9-7.6-19.3-7.6-30.3v-33.3c-5.2.9-10.5 1.3-16 1.3h-48V240h32c17.7 0 32-14.3 32-32s-14.3-32-32-32H341zM528 240c17.7 0 32 14.3 32 32v48h-64v-48c0-17.7 14.3-32 32-32m-80 32v48c-17.7 0-32 14.3-32 32v128c0 17.7 14.3 32 32 32h160c17.7 0 32-14.3 32-32V352c0-17.7-14.3-32-32-32v-48c0-44.2-35.8-80-80-80s-80 35.8-80 80"
            />
          </svg>
        </div>
        <div class="ml-2 w-1/2 text-justify">
          <h2 class="font-bold text-lg mb-2">Record Keeping</h2>
          <p>
            In order to support our AML and CTF activities, we keep thorough
            records of all transactions and customer information, as required by
            law.
          </p>
        </div>
      </div>

      <div class="flex justify-center items-center">
        <div
          class="h-20 ml-2 mr-2 w-20 rounded-full border-2 flex justify-center items-center"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="32"
            height="32"
            viewBox="0 0 512 512"
          >
            <path
              fill="#3a7c94"
              d="M256 96c38.4 0 73.7 13.5 101.3 36.1l-32.6 32.6c-4.6 4.6-5.9 11.5-3.5 17.4s8.3 9.9 14.8 9.9h112c8.8 0 16-7.2 16-16V64c0-6.5-3.9-12.3-9.9-14.8s-12.9-1.1-17.4 3.5l-34 34C363.4 52.6 312.1 32 256 32c-10.9 0-21.5.8-32 2.3v64.9c10.3-2.1 21-3.2 32-3.2m-123.9 58.7l32.6 32.6c4.6 4.6 11.5 5.9 17.4 3.5s9.9-8.3 9.9-14.8V64c0-8.8-7.2-16-16-16H64c-6.5 0-12.3 3.9-14.8 9.9s-1.1 12.9 3.5 17.4l34 34C52.6 148.6 32 199.9 32 256c0 10.9.8 21.5 2.3 32h64.9c-2.1-10.3-3.2-21-3.2-32c0-38.4 13.5-73.7 36.1-101.3M477.7 224h-64.9c2.1 10.3 3.2 21 3.2 32c0 38.4-13.5 73.7-36.1 101.3l-32.6-32.6c-4.6-4.6-11.5-5.9-17.4-3.5s-9.9 8.3-9.9 14.8v112c0 8.8 7.2 16 16 16h112c6.5 0 12.3-3.9 14.8-9.9s1.1-12.9-3.5-17.4l-34-34C459.4 363.4 480 312.1 480 256c0-10.9-.8-21.5-2.3-32M256 416c-38.4 0-73.7-13.5-101.3-36.1l32.6-32.6c4.6-4.6 5.9-11.5 3.5-17.4s-8.3-9.9-14.8-9.9H64c-8.8 0-16 7.2-16 16v112c0 6.5 3.9 12.3 9.9 14.8s12.9 1.1 17.4-3.5l34-34C148.6 459.4 199.9 480 256 480c10.9 0 21.5-.8 32-2.3v-64.9c-10.3 2.1-21 3.2-32 3.2"
            />
          </svg>
        </div>
        <div class="ml-2 w-1/2 text-justify">
          <h2 class="font-bold text-lg mb-2">Internal Controls and Audits</h2>
          <p>
            To guarantee the efficacy of our AML and CTF procedures, we have set
            up thorough internal controls and carry out frequent audits.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>
