<!-- components/AppFooter.vue -->
<template>
    <footer class="border-t border-neutral-200 px-8 pt-8 pb-6">

        <div class="flex items-start justify-between mb-8">

            <div>
                <NuxtLink to="/" class="flex items-center gap-2 mb-2">
                    <div class="w-6 h-6 bg-neutral-900 rounded flex
                   items-center justify-center">
                        <span class="text-white text-[11px] font-medium">A</span>
                    </div>
                    <span class="text-sm font-medium">Alex Kim</span>
                </NuxtLink>
                <p class="text-xs text-neutral-400 max-w-[200px] leading-relaxed">
                    Designer & developer building thoughtful digital experiences.
                </p>
            </div>

            <div class="flex gap-12">
                <div>
                    <p class="text-[11px] uppercase tracking-widest
               text-neutral-400 font-medium mb-3">Pages</p>
                    <ul class="flex flex-col gap-2">
                        <li v-for="link in navLinks" :key="link.to">
                            <NuxtLink :to="link.to" class="text-xs text-neutral-500
                       hover:text-neutral-900 transition-colors">
                                {{ link.label }}
                            </NuxtLink>
                        </li>
                    </ul>
                </div>

                <div>
                    <p class="text-[11px] uppercase tracking-widest
               text-neutral-400 font-medium mb-3">Find me</p>
                    <ul class="flex flex-col gap-2">
                        <li v-for="s in social" :key="s.href">
                            <a :href="s.href" target="_blank" class="text-xs text-neutral-500 flex items-center
                       gap-1.5 hover:text-neutral-900 transition-colors">
                                <component :is="s.icon" class="w-3.5 h-3.5" />
                                {{ s.label }}
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="border-t border-neutral-100 pt-5
             flex items-center justify-between">
            <p class="text-[11px] text-neutral-400">
                © {{ year }} Alex Kim. All rights reserved.
            </p>
            <p class="text-[11px] text-neutral-400">
                Designed & built by me
            </p>
        </div>

    </footer>
</template>

<script setup>
const year = new Date().getFullYear()

const navLinks = [
    { label: 'Work', to: '/work' },
    { label: 'About', to: '/about' },
    { label: 'Writing', to: '/writing' },
    { label: 'Contact', to: '/contact' },
]

const social = [
    { label: 'GitHub', href: 'https://github.com/alexkim' },
    { label: 'LinkedIn', href: 'https://linkedin.com/in/alexkim' },
    { label: 'Twitter', href: 'https://x.com/alexkim' },
    { label: 'Email', href: 'mailto:hello@alexkim.dev' },
]
</script>