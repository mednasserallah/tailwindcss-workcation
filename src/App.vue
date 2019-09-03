<template>
  <div id="app" class="bg-gray-200 antialiased">
    <SiteHeader></SiteHeader>
    <SearchFilters></SearchFilters>
    <main class="py-6">
      <div class="px-4">
        <h3 class="text-gray-900 text-xl">Los Angeles</h3>
        <p class="text-gray-600">Live like the stars in these luxurious Southern California estates.</p>
      </div>
      <div class="mt-6 sm:overflow-x-auto">
        <div class="px-4 sm:inline-flex sm:-mx-1 sm:pb-8">
          <div
            v-for="i in 6"
            :key="i"
            :class="{'mt-10': i > 1}"
            class="sm:mt-0 sm:w-80 sm:flex-shrink-0 sm:px-2"
          >
            <Card></Card>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import SiteHeader from "@/components/SiteHeader";
import SearchFilters from "@/components/SearchFilters";
import Card from "@/components/Card.vue";

export default {
  name: "app",
  components: {
    SiteHeader,
    SearchFilters,
    Card
  }
};
</script>

<style src="./assets/css/tailwind.css">
</style>
