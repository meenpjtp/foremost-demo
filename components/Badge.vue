<template>
  <a :href="`${link}`" target="_blank">
    <div
      class="badge"
      :style="`backgroundImage: url(${require(`~/assets/image/${img}`)}); backgroundPosition: ${position}; backgroundSize: ${size};`"
    ></div>
  </a>
</template>

<script>
export default {
  props: ["link", "img", "position", "size"],
};
</script>