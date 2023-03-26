<template>
  <!-- profile container -->
  <div class="flex items-center justify-center gap-2">
    <!-- profile image -->
    <div class="">
      <img src="../assets/images/profile.jpg" alt="" class="w-8" />
    </div>
    <!-- first name -->
    <div>
      <p class="text-user_name">Bliss</p>
    </div>
    <!-- drop down icon -->
    <div class="bg-dropDown rounded-sm text-user_name font-normal p-1">
      <i class="fa fa-caret-down" aria-hidden="true"></i>
    </div>
  </div>
</template>
<style scoped>
div {
  cursor: pointer;
}
</style>
