<script setup lang="ts">
import { ref } from "vue";
import BaseIcon from "@/components/common/atoms/base-icon/BaseIcon.vue";
import BaseDropdown from "@/components/common/atoms/base-dropdown/BaseDropdown.vue";

const dropdownServicesValue = ref<string | null>(null);

const dropdownServices = ref([
  {
    value: "Polygon",
    key: "Polygon ",
    icon: "icon-logo-polygon.svg",
  },
  {
    value: "Polygon1",
    key: "Polygon1",
    icon: "icon-logo-polygon.svg",
  },
  {
    value: "Polygon2",
    key: "Polygon2",
    icon: "icon-logo-polygon.svg",
  },
]);
</script>

<template>
  <header class="header">
    <div class="header__logo"></div>
    <div class="header__service">
      <base-icon src="icon-search.svg" />

      <base-dropdown
        v-model="dropdownServicesValue"
        :options="dropdownServices"
        :placeholder="'Polygon  '"
      />
    </div>
  </header>
</template>

<style lang="scss" scoped>
@import "./AppHeader";
</style>
