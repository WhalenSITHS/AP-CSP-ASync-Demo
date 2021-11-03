<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  //options API
  name: "Home",
  components: {
    HelloWorld,
  },
  data() {
    return {
      name: "Daniel",
    };
  },
  beforeCreate: function () {
    console.log(this.name);
  },
  created: function () {
    console.log(this.name);
  },
};
</script>
