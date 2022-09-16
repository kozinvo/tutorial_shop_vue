<template>
  <div class="v-main-wrapper">
    <p>{{ title }}</p>
    <v-catalog />
    <v-cart />
  </div>
</template>

<script>
import vCatalog from "./v-catalog.vue";
import vCart from "./v-cart.vue";

export default {
  name: "v-main-wrapper",
  components: { vCatalog, vCart },
  props: {},
  data() {
    return {
      title: "Main wrapper",
    };
  },
  computed: {},
  methods: {},
  watch: {},
  mounted() {
    console.log("Hello I am alive");
  },
};
</script>

<style>
.v-main-wrapper {
  margin: 0 auto;
  max-width: 900px;
}
</style>
