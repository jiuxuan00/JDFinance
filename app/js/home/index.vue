<template lang="html">
    <div :class="$style.home">
        <heador></heador>
        <h-slider></h-slider>
        <novice></novice>
    </div>
</template>

<script>
import Heador from "../public/header";
import hSlider from "./hSlider";
import Novice from "./novice";
export default {
  components: {
    Heador,
    hSlider,
    Novice
  }
}
</script>

<style lang="scss" module>
  @import '../../css/reset.scss';
  .home{
    // color: red;
    font-size: 80px;
  }
</style>
