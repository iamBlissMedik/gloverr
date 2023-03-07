<script setup>
import ButtonVue from "./Button.vue";
import { ref } from "vue";
const props = defineProps({
  event: {
    type: Object,
  },
  index: {
    type: Number,
  },
});
// extract date
const dateFormat = (dateData) =>
  new Date(dateData).toDateString().split(" ").slice(1, 3).reverse().join(" ");

//   to get the link
const link = ref("");

// navigate to event
const goToTicket = (e) => {
  link.value = props.event.url;
};
</script>
<template>
  <!-- event card 1 -->
  <div class="grid items-center bg-card p-5 rounded card">
    <!-- event image -->

    <div>
      <img :src="event.artist.image_url" alt="" class="w-full h-60" />
    </div>
    <!-- event details + date tag -->
    <div class="flex justify-between items-center">
      <!-- event details -->
      <div class="text-event_text">
        <!-- card title -->
        <div class="text-event_head font-semibold mt-2 mb-2">
          <h1>{{ event.venue.name }}</h1>
        </div>
        <!-- CARD LOCATION -->
        <div class="flex items-center mb-2">
          <i class="fa fa-map-marker mr-2" aria-hidden="true"></i>
          <p>{{ event.venue.city }}</p>
        </div>
        <!-- price tag -->
        <div class="mb-4 flex items-center">
          <i class="fa fa-tag mr-2" aria-hidden="true"></i>
          <p>
            Starting from
            <span class="text-glover_purple font-bold">₦90,000</span>
          </p>
        </div>
        <!-- BUTTON -->
        <div>
          <a :href="link">
            <ButtonVue @buttonClick="goToTicket" :index="index" />
          </a>
        </div>
      </div>
      <!-- date tag -->
      <div class="date-tag">
        <div class="circle-1"></div>
        <p>{{ dateFormat(event.datetime) }}</p>
        <div class="circle-2"></div>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>