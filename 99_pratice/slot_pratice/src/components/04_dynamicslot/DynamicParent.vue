<script setup>
import { reactive } from "vue";
import DynamicChild from "./DynamicChild.vue";
const dynamicImg = reactive({
  name: "name",
  img:
    "https://i.namu.wiki/i/QVzdyUdTlweOa37HqhVDauXIS1zv1lCeoGL96N-AEvM54Vacn3-K9PlRV6xJ-MLBbZXThp61g2PPCtlA7cROXA.webp",
});
</script>

<template>
  <div>
    <h1>DynamicSlot :</h1>
    <input v-model="dynamicImg.name" />
    <DynamicChild>
      <template #[dynamicImg.name]>
        {{ dynamicImg.name }}
        <img :src="dynamicImg.img" />
      </template>
    </DynamicChild>
  </div>
</template>

<style scoped>
.parentsContainer {
  display: flex;
  align-items: center;
  flex-direction: column;
  border: 1px solid;
}
</style>
