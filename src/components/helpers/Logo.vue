<template>
  <div class="logo-div">
    <span
      class="logo-title-name"
      >
      <img class="logo" v-if="!nightMode" :src="image" :alt="name" />
      <img class="logo" v-else :src="image_dm" :alt="name" /></span
    >
    <span class="logo-title-dot dot-color">{{ dot }}</span>
  </div>
</template>

<script>
import info from "../../../info";

export default {
  name: "Logo",
  image: "Image",
  image_dm: "Imagedm",
  props: {
    nightMode: {
      type: Boolean,
    },
  },
  data() {
    return {
      name: info.logo_name,
      image: info.logo_image,
      image_dm: info.logo_image_dm,
      dot: ".",
    };
  },
};
</script>

<style scoped>
.logo-div:hover .logo-title-name {
  letter-spacing: 0px;
  transition: 0.5s all;
}
.logo-div {
  width: 100px;
  height: 75px;
}
.logo.nightmode {
  color: #fff;
}
.cls-1 {
  color: red;
}
.logo-title-name {
  font-size: 45px;
  font-weight: 500;
  letter-spacing: -2px;
  transition: 0.5s all;
  font-family: "Sedan", serif;
  font-weight: 400;
  font-style: italic;
}

.logo-title-dot {
  font-size: 60px;
  font-weight: 700;
  font-family: "Sedan", serif;
  font-style: normal;
  line-height: 45px;
  position: relative;
  top: 20px;
}
</style>
