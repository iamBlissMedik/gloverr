<script setup>
const emit = defineEmits(["buttonClick"]);
const props = defineProps(["index"]);
const buttonClick = (index) => {
  emit("buttonClick", index);
};
</script>
<template>
  <div>
    <button
      class="bg-white p-2 text-glover_purple border-2 border-glover_purple rounded font-bold"
      @click="buttonClick(index)"
    >
      Buy Ticket
    </button>
  </div>
</template>
