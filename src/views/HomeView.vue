<template>
  <button v-on:click="ItemDetail">queryについて</button>
</template>
<script>
export default {
  data() {
    return {
      id: 'a84ddc62-e70d-c5bc-3be2-bde775cbd6b6',
    };
  },
  methods: {
    ItemDetail() {
      this.$route.push({ name: 'ItemDetail', params: { itemId: this.id } });
    },
  },
};
</script>
