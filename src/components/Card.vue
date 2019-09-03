<template>
  <div>
    <div class="relative pb-5/6">
      <img
        class="absolute inset-0 h-full object-cover rounded-lg shadow-md"
        src="https://images.unsplash.com/photo-1512917774080-9991f1c4c750?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80"
        alt="Villa at Los Angeles"
      />
    </div>
    <div class="px-4">
      <div class="relative -mt-16 bg-white rounded-lg px-4 py-4 shadow-lg">
        <div class="flex">
          <span
            class="inline-block px-2 py-1 leading-none bg-teal-200 text-teal-800 font-semibold uppercase tracking-wide text-xs rounded-full"
          >Plus</span>
          <span
            class="ml-2 text-xs text-gray-600 font-semibold uppercase tracking-wide"
          >3 beds &bull; 2 baths</span>
        </div>
        <div>
          <h4 class="mt-1 text-gray-900 text-lg font-semibold">Modern home in city center</h4>
        </div>
        <div class="mt-1">
          <span class="text-gray-900">$1400</span>
          <span class="ml-1 text-sm text-gray-600">/wk</span>
        </div>
        <div class="mt-2 flex items-center">
          <svg
            v-for="i in 4"
            class="h-4 w-4 fill-current text-teal-500"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path d="M0 0h24v24H0z" fill="none" />
            <path
              d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"
            />
            <path d="M0 0h24v24H0z" fill="none" />
          </svg>
          <span class="ml-2 text-sm text-gray-600">34 reviews</span>
        </div>
      </div>
    </div>
  </div>
</template>