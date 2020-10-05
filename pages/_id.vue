<template>
  <section class="container mx-auto">
    <div>
      <img
        :src="data.avatar_url"
        class="rounded-full w-1/4 mb-6"
        alt="profile image"
      />
      <h2 class="text-2xl font-bold">{{ data.name }}</h2>
      <span class="text-xl text-gray-700">{{ data.login }}</span>
      <h2 class="pt-3">{{ data.bio }}</h2>
      <span>Followers: {{ data.followers }}</span>
      <span>Following: {{ data.following }}</span>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData({ params, $http }) {
    const data = await $http.$get(`https://api.github.com/users/${params.id}`);
    return { data };
  },
};
</script>

<style>
</style>