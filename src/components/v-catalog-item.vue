<template>
  <div class="v-catalog-item">
    <img
      class="v-catalog-item__img"
      :src="require('../assets/images/' + product_data.image)"
      alt="img"
    />
    <p class="v-catalog-item__name">{{ product_data.name }}</p>
    <p class="v-catalog-item__price">Price: {{ product_data.price }} RUB</p>
    <button
      class="v-catalog-item__add_to_card_btn btn"
      @click="sendDataToParent"
    >
      Add to cart
    </button>
  </div>
</template>

<script>
export default {
  name: "v-catalog-item",
  components: {},
  props: {
    product_data: {
      type: Object,
      default() {
        return {};
      },
    },
  },
  data() {
    return {
      title: "Catalog-item",
    };
  },
  computed: {},
  methods: {
    sendDataToParent() {
      this.$emit("sendArticle", this.product_data.article);
    },
  },
  watch: {},
  mounted() {},
};
</script>

<style lang="scss">
.v-catalog-item {
  flex-basis: 25%;
  box-shadow: 0 0 8px 0 #e0e0e0;
  padding: $padding * 2;
  margin-bottom: $margin * 2;
  &__img {
    width: 100px;
  }
}
</style>
