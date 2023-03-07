<template>
  <!-- all events -->
  <div>
    <!-- event title -->
    <div class="text-event_head font-semibold mb-3">
      <h1>All Events</h1>
    </div>
    <!-- event cards -->
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
      <div v-for="(event, index) in filteredEvents" :key="index">
        <Card :event="event" :index="index"/>
      </div>
    </div>
  </div>
</template>

<script setup>
import Card from "./Card.vue";



const props = defineProps({
  filteredEvents: {
    type: Array,
  },
});

</script>
