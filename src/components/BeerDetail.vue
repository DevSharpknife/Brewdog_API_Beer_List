<template>
  <article v-if='beer'>
      <h3>{{ beer.name }}</h3>
      <p>{{ beer.tagline }}</p>
      <p>abv:{{ beer.abv }}</p>
      <img class="large-beer":src="beer.image_url" alt="beer pic">
  </article>
</template>

<script>
import { eventBus } from '@/main.js';

export default {
    name: 'beer-detail',
    props: ['beer']
}
</script>

<style>

.large-beer {
    height: 30vh;
}

</style>