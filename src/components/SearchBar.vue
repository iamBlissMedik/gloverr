<template>
  <div class="flex items-center relative ">
    <input
      class=" rounded-md px-6 py-2 border-0 outline-event_text"
      type="text"
      placeholder="Search"
      @input="searchT"
    />

    <div class="absolute left-1 text-event_text">
      <i class="fa fa-search" aria-hidden="true"></i>
    </div>
  </div>
</template>

<script setup>



const emit = defineEmits(["inputs"]);



const searchT = (e) => {
 emit("inputs",e.target.value)
};
</script>

<style scoped>
input{
  width: 40%;
}
</style>
