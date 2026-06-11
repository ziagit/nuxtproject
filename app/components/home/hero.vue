<!-- pages/index.vue -->
<template>
    <main>
        <section class="grid grid-cols-2 gap-12 items-center min-h-screen
             px-16 py-24">

            <div>
                <div class="inline-flex items-center gap-1.5 text-xs
                 border border-neutral-200 rounded-full px-3 py-1
                 text-neutral-500 mb-7">
                    <span class="w-1.5 h-1.5 rounded-full bg-green-600" />
                    Available for work
                </div>

                <h1 class="text-5xl font-medium tracking-tight
               leading-[1.15] mb-5">
                    Designer &
                    developer,
                    based in Seoul.
                </h1>

                <p class="text-neutral-500 leading-relaxed
             max-w-sm mb-8">
                    I craft thoughtful interfaces and build the
                    systems behind them.
                </p>

                <div class="flex items-center gap-4">
                    <NuxtLink to="/work" class="inline-flex items-center gap-2 text-sm
                   font-medium border border-neutral-300
                   px-5 py-2 rounded-lg hover:bg-neutral-50
                   transition-colors">
                        View work
                        <ArrowRightIcon class="w-4 h-4" />
                    </NuxtLink>
                    <NuxtLink to="/contact" class="text-sm text-neutral-500
                   hover:text-neutral-900 transition-colors">
                        Get in touch
                    </NuxtLink>
                </div>
            </div>

            <div class="flex flex-col gap-3">
                <div class="overflow-hidden rounded-3xl border border-neutral-100 shadow-lg">
                    <img
                        src="/images/hero.jpeg"
                        alt="Hero image"
                        class="w-full h-96 object-cover"
                    />
                </div>

                <div class="bg-neutral-50 rounded-xl p-5
                 border border-neutral-100">
                    <p class="text-[11px] uppercase tracking-widest
               text-neutral-400 mb-2">Currently</p>
                    <p class="text-sm font-medium mb-1">
                        Freelance designer & developer
                    </p>
                    <p class="text-xs text-neutral-500">
                        Open to full-time & contract roles
                    </p>
                </div>

                <div class="bg-neutral-50 rounded-xl p-5
                 border border-neutral-100">
                    <p class="text-[11px] uppercase tracking-widest
               text-neutral-400 mb-3">Stack</p>
                    <div class="flex flex-wrap gap-1.5">
                        <span v-for="tech in stack" :key="tech" class="text-xs text-neutral-500 border
                     border-neutral-200 rounded-full px-2.5 py-0.5">
                            {{ tech }}
                        </span>
                    </div>
                </div>

                <div class="grid grid-cols-2 gap-3">
                    <div v-for="stat in stats" :key="stat.label" class="bg-neutral-50 rounded-xl p-4
                   border border-neutral-100 text-center">
                        <p class="text-2xl font-medium tracking-tight mb-0.5">
                            {{ stat.value }}
                        </p>
                        <p class="text-xs text-neutral-400">{{ stat.label }}</p>
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<script setup>
const stack = [
    'Nuxt', 'Vue', 'Tailwind',
    'TypeScript', 'Figma', 'Node.js',
]
const stats = [
    { value: '24+', label: 'projects shipped' },
    { value: '5 yrs', label: 'experience' },
]
</script>