<template>
  <img :src="result && result.message" width="100" height="100" />
</template>

<script>
import axios from "axios";
import { defineComponent } from "vue";
export default defineComponent({
  async setup() {
    const rawData = await axios.get("https://dog.ceo/api/breeds/image/random");
    return {
      result: rawData.data,
    };
  },
});
</script>

<style lang="scss" scoped></style>
