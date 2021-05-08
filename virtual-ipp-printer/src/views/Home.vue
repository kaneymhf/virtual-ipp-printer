<template>
  <div>

    <HelloWorld msg="Welcome to Your Vue.js App" :mfp="true"/>

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
  },
};
</script>
