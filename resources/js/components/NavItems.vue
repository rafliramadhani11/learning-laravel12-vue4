<script setup>
import { ref } from "vue";

const items = ref([
    {
        label: "Home",
    },
    {
        label: "Service",
    },
    {
        label: "About Us",
    },
]);
</script>

<template>
    <div class="md:flex hidden gap-x-5 items-center justify-between">
        <a v-for="(item, index) in items" :key="index" href="#">
            {{ item.label }}
        </a>
    </div>
</template>
