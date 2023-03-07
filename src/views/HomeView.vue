<script setup>
import Heading from "../components/Heading.vue";
import SearchBar from "../components/SearchBar.vue";
import FeaturedEvents from "../components/FeaturedEvents.vue";
import AllEvents from "../components/AllEvents.vue";
import axios from "axios";
import { onMounted, ref, computed } from "vue";

const data = ref([]);
const isLoading = ref(null);

const search = ref("");

onMounted(() => {
  axios
    .get(
      "https://rest.bandsintown.com/artists/john%20legend/events?app_id=0ab49580-c84f-44d4-875f-d83760ea2cfe"
    )
    .then((response) => {
      isLoading.value = true;

      data.value = response.data.map((e) => {
        if (!e?.artist) {
          e.artist = {
            image_url: "https://photos.bandsintown.com/thumb/14225788.jpeg",
          };
          return e;
        } else {
          return e;
        }
      });
    })
    .catch((error) => {
      console.log(error.message);
    });
});

const onInput = (e) => {
  search.value = e.toLowerCase().trim();
};

// filtered events
const filteredEvents = computed(() => {
  return data.value.filter((e) =>
    e.venue.name.toLowerCase().includes(search.value)
  );
});
</script>

<template>
  <div class="mx-auto px-8 py-8 lg:px-20 lg:py-10 z-10" v-if="isLoading">
    <header>
      <Heading />
    </header>
    <main>
      <SearchBar @inputs="onInput" />
      <FeaturedEvents  />
      <AllEvents :filteredEvents="filteredEvents" />
    </main>
  </div>
</template>
