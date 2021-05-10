<template>
  <div>

    <HelloWorld
    msg="Welcome to Your Vue.js App"
    :mfp="true"
    :color="true"
    :toner_value="90"
    :paper_value="paper_value"
    />

  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';

export default {
  name: 'Home',
  components: {
    HelloWorld,
  },
  props: {
    mfp: Boolean,
    color: Boolean,
  },
  data() {
    return {
      paper_value: 100,
      toner_value: 80,
    };
  },
};
</script>
