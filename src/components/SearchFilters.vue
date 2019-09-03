<template>
  <section class="bg-gray-800">
    <div class="flex justify-between px-4 py-3">
      <div class="relative sm:w-full sm:max-w-sm">
        <div class="absolute inset-y-0 left-0 flex items-center pl-3">
          <svg class="w-6 h-6 fill-current text-gray-500" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0 0 16 9.5 6.5 6.5 0 1 0 9.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"
            />
            <path d="M0 0h24v24H0z" fill="none" />
          </svg>
        </div>
        <input
          class="sm:block w-full pl-10 pr-4 py-2 focus:outline-none focus:bg-white focus:text-gray-900 bg-gray-900 text-white rounded-lg"
          placeholder="Search by keywords"
        />
      </div>
      <button
        @click="toggle"
        type="button"
        class="pl-3 pr-4 ml-2 inline-flex items-center bg-gray-700 rounded-lg shadow focus:outline-none focus:shadow-outline hover:bg-gray-600"
      >
        <svg class="w-6 h-6 fill-current text-gray-500" xmlns="http://www.w3.org/2000/svg">
          <path
            v-if="isOpen"
            d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12z"
          />
          <path v-else d="M10 18h4v-2h-4v2zM3 6v2h18V6H3zm3 7h12v-2H6v2z" />
          <path d="M0 0h24v24H0z" fill="none" />
        </svg>
        <span class="ml-1 text-white font-medium">Filter</span>
      </button>
    </div>

    <form v-show="isOpen">
      <div class="lg:flex">
        <!-- Property capacity & price -->
        <div
          class="px-4 py-4 border-t border-gray-900 sm:flex sm:justify-between lg:w-2/5 lg:flex-wrap"
        >
          <div class="flex -mx-2 sm:w-1/2 lg:w-full">
            <label class="block w-1/2 px-2">
              <span class="text-sm text-gray-500 font-semibold">Bedrooms</span>
              <select class="mt-1 form-select block w-full">
                <option value="4">4</option>
              </select>
            </label>

            <label class="block w-1/2 px-2">
              <span class="text-sm text-gray-500 font-semibold">Bathrooms</span>
              <select class="mt-1 form-select block w-full lg:ml-4">
                <option v-for="(i, index) in 5" :value="i" :key="index">{{ i }}</option>
              </select>
            </label>
          </div>

          <!-- Price Range -->
          <div class="mt-4 sm:w-1/2 sm:mt-0 lg:w-full">
            <label class="block">
              <span class="text-sm text-gray-500 font-semibold">Price Range</span>
              <select class="mt-1 form-select block w-full">
                <option value="2000">Up to $2000/ wk</option>
              </select>
            </label>
          </div>
        </div>

        <!-- Property Type -->
        <div class="px-4 py-4 border-t border-gray-900 lg:w-1/5 lg:border-l">
          <div>
            <span class="text-sm text-gray-500 font-semibold">Property Type</span>
            <div class="sm:flex lg:block">
              <label class="mt-3 flex items-center sm:w-1/4 lg:w-full">
                <input class="form-radio" type="radio" name="propertyType" value="house" />
                <span class="ml-2 text-white">House</span>
              </label>

              <label class="mt-3 flex items-center sm:w-1/4 lg:w-full">
                <input class="form-radio" type="radio" name="propertyType" value="apartment" />
                <span class="ml-2 text-white">Apartment</span>
              </label>

              <label class="mt-3 flex items-center sm:w-1/4 lg:w-full">
                <input class="form-radio" type="radio" name="propertyType" value="loft" />
                <span class="ml-2 text-white">Loft</span>
              </label>

              <label class="mt-3 flex items-center sm:w-1/4 lg:w-full">
                <input class="form-radio" type="radio" name="propertyType" value="townhouse" />
                <span class="ml-2 text-white">Townhouse</span>
              </label>
            </div>
          </div>
        </div>

        <!-- Amenities -->
        <div class="px-4 py-4 border-t border-gray-900 lg:w-2/5 lg:border-l">
          <div>
            <span class="text-sm text-gray-500 font-semibold">Amenities</span>
            <div class="sm:flex sm:flex-wrap">
              <label class="mt-3 flex items-center sm:w-1/4 lg:w-1/2">
                <input class="form-checkbox" type="checkbox" name="balcony" />
                <span class="ml-2 text-white">Balcony</span>
              </label>

              <label class="mt-3 flex items-center sm:w-1/4 lg:w-1/2">
                <input class="form-checkbox" type="checkbox" name="pool" />
                <span class="ml-2 text-white">Pool</span>
              </label>

              <label class="mt-3 flex items-center sm:w-1/4 lg:w-1/2">
                <input class="form-checkbox" type="checkbox" name="beach" />
                <span class="ml-2 text-white">Beach</span>
              </label>

              <label class="mt-3 flex items-center sm:w-1/4 lg:w-1/2">
                <input class="form-checkbox" type="checkbox" name="beach" />
                <span class="ml-2 text-white">Pet friendly</span>
              </label>

              <label class="mt-3 flex items-center sm:w-1/4 lg:w-1/2">
                <input class="form-checkbox" type="checkbox" name="beach" />
                <span class="ml-2 text-white">Kid friendly</span>
              </label>

              <label class="mt-3 flex items-center sm:w-1/4 lg:w-1/2">
                <input class="form-checkbox" type="checkbox" name="beach" />
                <span class="ml-2 text-white">Parking</span>
              </label>

              <label class="mt-3 flex items-center sm:w-1/4 lg:w-1/2">
                <input class="form-checkbox" type="checkbox" name="airConditioning" />
                <span class="ml-2 text-white">Air conditioning</span>
              </label>
            </div>
          </div>
        </div>
      </div>

      <!-- Update results -->
      <div class="px-4 py-4 bg-gray-900 text-right">
        <button
          class="px-4 py-2 block w-full sm:inline-block sm:w-auto font-semibold text-white rounded-lg bg-indigo-500 hover:bg-indigo-400"
        >Update results</button>
      </div>
    </form>
  </section>
</template>

<script>
export default {
  data() {
    return {
      isOpen: true
    };
  },

  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    }
  }
};
</script>