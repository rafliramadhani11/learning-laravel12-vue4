<script setup>
import { Button, Menu } from "primevue";
import { ref } from "vue";

const menu = ref();

const items = ref([
    {
        label: "Home",
        icon: "pi pi-home",
    },
    {
        label: "Service",
        icon: "pi pi-briefcase",
    },
    {
        label: "About Us",
        icon: "pi pi-users",
    },
]);

const toggle = (event) => {
    menu.value.toggle(event);
};
</script>

<template>
    <Button
        @click="toggle"
        aria-haspopup="true"
        aria-controls="overlay_menu"
        icon="pi pi-bars"
        size="small"
        rounded
        class="md:!hidden"
    />

    <Menu
        ref="menu"
        :model="items"
        id="overlay_menu"
        popup
        class="w-full max-w-full left-0 right-0 !border-none !rounded-none !mt-2 dark:!bg-zinc-900 !shadow-none"
    >
        <template #item="{ item, props }">
            <a v-bind="props.action" class="flex items-center !px-6 !gap-x-3">
                <i :class="item.icon"></i>
                <span class="text-sm">{{ item.label }}</span>
            </a>
        </template>
    </Menu>
</template>
