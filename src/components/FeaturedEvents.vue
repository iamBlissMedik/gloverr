<script setup>
import ButtonVue from "./Button.vue";
</script>
<template>
  <div class="mt-3 mb-5">
    <!-- featured event title -->
    <div class="mb-3">
      <h1 class="text-event_head font-semibold">Featured Events</h1>
    </div>
    <!-- featured events -->
    <div class="relative z-10">
      <div class="grid sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-2 gap-4">
        <!-- left -->
        <div class="bg-card rounded grid p-5 items-center">
          <!-- image -->
          <div class="mb-2">
            <img src="../assets/images/wizkid.jpg" alt="" class="w-full" />
          </div>
          <!-- event content -->
          <div>
            <!-- event headeer -->
            <h1 class="text-event_head font-semibold mb-2">Wizkid in Warri</h1>
            <!-- event details -->
            <div class="flex items-center justify-between">
              <!-- event location,date,and price -->
              <div class="text-event_text">
                <!-- location n date -->
                <div class="flex mb-2">
                  <!-- location -->
                  <div class="mr-7 flex items-center">
                    <i class="fa fa-map-marker mr-2" aria-hidden="true"></i>
                    <p>Lagos</p>
                  </div>
                  <!-- date -->
                  <div class="flex items-center sm:text-sm">
                    <i class="fa fa-calendar mr-2" aria-hidden="true"></i>
                    <p>8th December,2021</p>
                  </div>
                </div>
                <!-- price -->
                <div class="flex items-center">
                  <i class="fa fa-tag mr-2" aria-hidden="true"></i>
                  <p>
                    Starting from
                    <span class="text-glover_purple font-bold">₦90,000</span>
                  </p>
                </div>
              </div>
              <!-- button -->
              <ButtonVue />
            </div>
          </div>
        </div>
        <!-- right -->
        <div class="bg-card rounded grid p-5 items-center">
          <!-- image -->
          <div class="mb-2">
            <img src="../assets/images/wizkid.jpg" alt="" class="w-full" />
          </div>
          <!-- event content -->
          <div>
            <!-- event headeer -->
            <h1 class="text-event_head font-semibold mb-2">Wizkid in Warri</h1>
            <!-- event details -->
            <div class="flex items-center justify-between">
              <!-- event location,date,and price -->
              <div class="text-event_text">
                <!-- location n date -->
                <div class="flex mb-2">
                  <!-- location -->
                  <div class="mr-7 flex items-center">
                    <i class="fa fa-map-marker mr-2" aria-hidden="true"></i>
                    <p>Lagos</p>
                  </div>
                  <!-- date -->
                  <div class="flex items-center">
                    <i class="fa fa-calendar mr-2" aria-hidden="true"></i>
                    <p>8th December,2021</p>
                  </div>
                </div>
                <!-- price -->
                <div class="flex items-center">
                  <i class="fa fa-tag mr-2" aria-hidden="true"></i>
                  <p>
                    Starting from
                    <span class="text-glover_purple font-bold">₦90,000</span>
                  </p>
                </div>
              </div>
              <!-- button -->
              <ButtonVue />
            </div>
          </div>
        </div>
      </div>
      <!-- next icon BUTTON-->
      <div class="position: absolute top-16 right-0 z-30">
        <div
          class="relative top-10 left-2 bg-next_event drop-shadow rounded-lg w-4 flex justify-center items-center z"
        >
          <i class="fa fa-angle-right" aria-hidden="true"></i>
        </div>
      </div>
    </div>
  </div>
</template>
