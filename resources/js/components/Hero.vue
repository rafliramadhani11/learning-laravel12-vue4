<template>
    <div class="relative min-h-[25rem] flex lg:flex-row flex-col">
        <div
            class="flex md:max-w-2xl lg:max-w-4xl xl:max-w-6xl md:mx-auto lg:flex lg:flex-row flex-col justify-center md:justify-normal h-full flex-1"
        >
            <div
                v-animateonscroll="{
                    enterClass:
                        'opacity-100 translate-y-0 transition-all duration-2500 ease-out',
                    leaveClass: 'opacity-0 translate-y-10',
                }"
                class="relative flex-1 z-20 flex items-center justify-center"
            >
                <div class="flex items-center justify-center w-full h-full">
                    <div class="w-full text-center lg:text-left">
                        <h1
                            class="text-3xl xl:text-4xl font-bold text-zinc-200 lg:text-zinc-950 lg:dark:!text-zinc-200 mb-6 leading-tight!"
                        >
                            <span class="block">Create the screens your</span>
                            <span class="block text-primary"
                                >visitors deserve to see</span
                            >
                        </h1>

                        <p
                            class="text-zinc-400 lg:text-zinc-500 text-xl leading-normal mb-8 lg:max-w-none"
                        >
                            Lorem ipsum dolor sit amet, consectetur adipiscing
                            elit,
                        </p>

                        <div
                            class="flex items-center gap-4 justify-center lg:justify-start"
                        >
                            <Button label="Learn More" type="button" />
                            <Button
                                label="Live Demo"
                                type="button"
                                outlined
                                class="!text-zinc-200 lg:!text-zinc-950 lg:dark:!text-zinc-200 hover:!text-zinc-950 hover:dark:!text-zinc-200"
                            />
                        </div>
                    </div>
                </div>
            </div>

            <div
                v-animateonscroll="{
                    enterClass:
                        'opacity-100 translate-y-0 transition-all duration-2500 ease-out',
                    leaveClass: 'opacity-0 translate-y-10',
                }"
                class="absolute lg:relative inset-0 lg:inset-auto flex-1"
            >
                <div
                    class="absolute lg:hidden inset-0 bg-zinc-900/50 backdrop-brightness-40 dark:backdrop-brightness-80 dark:bg-zinc-900/80 z-10"
                />
                <img
                    src="https://fqjltiegiezfetthbags.supabase.co/storage/v1/render/image/public/block.images/blocks/hero/hero-1.png"
                    alt="hero-1"
                    class="h-full w-full object-cover xl:[clip-path:polygon(12%_0,100%_0%,100%_100%,0_100%)]"
                />
            </div>
        </div>
    </div>
</template>

<script setup>
import Button from "primevue/button";
</script>
