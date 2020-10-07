<template>
  <section class="container mx-auto">
    <h1 class="text-3xl text-center font-bold mb-5 underline">
      Countries in the World Listing
    </h1>
    <div class="grid grid-cols-2">
      <section
        class="flex flex-col items-center mb-4"
        v-for="country in countries"
        :key="country.name"
      >
        <img :src="country.flag" :alt="country.name" class="w-1/2 h-1/2" />
        <div class="px-4">
          <span class="text-2xl font-bold">{{ country.name }}</span>
          <span class="text-xl">{{ country.capital }}</span>
          <p class="italic font-bold text-md">
            Population: {{ country.population }}
          </p>
        </div>
      </section>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData({ $http }) {
    const countries = await $http.$get(
      "https://restcountries.eu/rest/v2/all?fields=name;capital;flag;population"
    );
    return { countries };
  },
};
</script>

<style>
</style>