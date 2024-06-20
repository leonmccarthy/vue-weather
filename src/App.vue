<script setup>
  import { ref } from 'vue';
  import SearchInput from './components/SearchInput.vue';

  const places = ref([])

  const addPlace = (data) => {
    places.value.push(data)
  }
</script>
<template>
  <main>

    <!-- Date -->
    <div class="text-center mb-6">
      {{ new Date().toLocaleDateString('en-US', {
        weekday: 'long',
        year: 'numeric',
        month: 'long',
        day: 'numeric'
      }) }}
    </div>

    <!-- Search -->
     <div>
        <SearchInput @place-data="addPlace"/>
     </div>

     <!-- Weather cards -->
      <div>
        <p v-for="place in places">{{ place.location.name }}</p>
      </div>
  </main>
</template>