<template>
  <div id="app" class="min-h-screen bg-gray-200 antialiased xl:flex xl:flex-col xl:h-screen">
    <SiteHeader class="xl:flex-shrink-0"></SiteHeader>
    <div class="xl:flex xl:flex-1 xl:overflow-y-hidden">
      <SearchFilters></SearchFilters>
      <main class="py-6 xl:overflow-x-hidden">
        <div class="px-4">
          <h3 class="text-gray-900 text-xl">Los Angeles</h3>
          <p
            class="text-gray-600"
          >Live like the stars in these luxurious Southern California estates.</p>
        </div>
        <div class="mt-6 sm:overflow-x-auto">
          <div class="px-4 sm:inline-flex sm:-mx-1 sm:pb-8">
            <div
              v-for="(proparty, i) in properties"
              :key="i"
              :class="{'mt-10': i > 0}"
              class="sm:mt-0 sm:w-80 sm:flex-shrink-0 sm:px-2"
            >
              <PropartyCard :key="i" :property="proparty"></PropartyCard>
            </div>
          </div>
        </div>
      </main>
    </div>
  </div>
</template>

<script>
import SiteHeader from "@/components/SiteHeader";
import SearchFilters from "@/components/SearchFilters";
import PropartyCard from "@/components/PropartyCard.vue";

export default {
  name: "app",
  components: {
    SiteHeader,
    SearchFilters,
    PropartyCard
  },
  data() {
    return {
      properties: [
        {
          imgUrl:
            "https://images.unsplash.com/photo-1512917774080-9991f1c4c750?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80",
          beds: 3,
          baths: 2,
          title: "Modern home in city center",
          price: 160000,
          reviewCount: 34,
          rating: 5
        },
        {
          imgUrl:
            "https://images.unsplash.com/photo-1512917774080-9991f1c4c750?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80",
          beds: 1,
          baths: 2,
          title: "Modern home in city center",
          price: 125000,
          reviewCount: 20,
          rating: 2
        },
        {
          imgUrl:
            "https://images.unsplash.com/photo-1512917774080-9991f1c4c750?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80",
          beds: 3,
          baths: 1,
          title: "Modern home in city center",
          price: 116000,
          reviewCount: 685,
          rating: 3
        },
        {
          imgUrl:
            "https://images.unsplash.com/photo-1512917774080-9991f1c4c750?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80",
          beds: 3,
          baths: 4,
          title: "Modern home in city center",
          price: 540000,
          reviewCount: 53,
          rating: 4
        }
      ]
    };
  }
};
</script>

<style src="./assets/css/tailwind.css">
</style>
