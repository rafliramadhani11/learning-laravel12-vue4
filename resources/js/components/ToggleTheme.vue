<script setup>
import { Button } from "primevue";
import { onMounted, ref } from "vue";

const isDark = ref(
    localStorage.getItem("theme")
        ? localStorage.getItem("theme") === "dark"
        : window.matchMedia("(prefers-color-scheme: dark)").matches
);

function setTheme() {
    document.documentElement.classList.toggle("dark-mode", isDark.value);
    localStorage.setItem("theme", isDark.value ? "dark" : "light");
}

function toggleTheme() {
    isDark.value = !isDark.value;
    setTheme();
}

onMounted(() => {
    setTheme();
});
</script>

<template>
    <Button
        @click="toggleTheme()"
        :icon="isDark ? 'pi pi-moon' : 'pi pi-sun'"
        variant="outlined"
        size="small"
        severity="secondary"
        rounded
    />
</template>
