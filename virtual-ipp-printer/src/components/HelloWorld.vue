<template>
  <div class="home">
    <div class="device">
      <div style="float: left; width: 30%">
      <h2>Device</h2>

      <img v-if="this.mfp == true" alt="Vue logo" src="../assets/logo.png">
      <img v-if="this.mfp == false" alt="Vue logo" src="../assets/logo.png">

      </div>
      <div>
        <h2>INFO</h2>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    mfp: Boolean,
  },
};
</script>
