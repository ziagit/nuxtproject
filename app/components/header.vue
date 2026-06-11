<!-- components/AppHeader.vue -->
<template>
    <header class="flex items-center justify-between
           px-8 h-16 bg-neutral-950 border-b border-neutral-800 text-white">

        <NuxtLink to="/" class="flex items-center gap-2">
            <div class="w-7 h-7 bg-neutral-900 rounded-md
               flex items-center justify-center">
                <span class="text-white text-sm font-medium">A</span>
            </div>
            <span class="text-[15px] font-medium tracking-tight text-white">
                Alex Kim
            </span>
        </NuxtLink>

        <nav class="flex items-center gap-8">
            <NuxtLink v-for="link in links" :key="link.to" :to="link.to" class="text-sm text-neutral-400
               hover:text-white transition-colors" active-class="text-white font-medium">
                {{ link.label }}
            </NuxtLink>
        </nav>
    </header>
</template>

<script setup>
const links = [
    { label: 'Work', to: '/work' },
    { label: 'About', to: '/about' },
    { label: 'Writing', to: '/writing' },
    { label: 'Contact', to: '/contact' },
]
</script>