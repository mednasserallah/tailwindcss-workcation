<template>
  <div>
    <div class="relative pb-5/6">
      <img
        class="absolute inset-0 h-full object-cover rounded-lg shadow-md"
        :src="property.imgUrl"
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
          >{{ property.beds }} {{ property.beds === 1 ? 'bed' : 'beds' }} &bull; {{ property.baths }} {{ property.baths === 1 ? 'bath' : 'baths' }}</span>
        </div>
        <div>
          <h4 class="mt-1 text-gray-900 text-lg font-semibold">{{ property.title }}</h4>
        </div>
        <div class="mt-1">
          <span class="text-gray-900">{{ formattedPrice }}</span>
          <span class="ml-1 text-sm text-gray-600">/wk</span>
        </div>
        <div class="mt-2 flex items-center">
          <svg
            v-for="i in 5"
            :key="i"
            :class="{'text-teal-500': i <= property.rating}"
            class="h-4 w-4 fill-current text-gray-500"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path d="M0 0h24v24H0z" fill="none" />
            <path
              d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"
            />
            <path d="M0 0h24v24H0z" fill="none" />
          </svg>
          <span class="ml-2 text-sm text-gray-600">{{ property.reviewCount }} reviews</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    property: {
      type: Object,
      required: true
    }
  },
  computed: {
    formattedPrice() {
      const formatter = new Intl.NumberFormat("en-US", {
        style: "currency",
        currency: "USD"
      });

      return formatter.format(this.property.price / 100);
    }
  }
};
</script>
