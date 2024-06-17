<script setup>
  import SearchInput from './components/SearchInput.vue';
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
        <SearchInput />
     </div>
  </main>
</template>