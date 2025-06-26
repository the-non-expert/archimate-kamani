<script lang="ts">
    const stats = [
        { value: "4.9", label: "#RATE AGENCY" },
        { value: "850+", label: "#TOTAL CONSTRUCTION" },
        { value: "$5.87B", label: "#TOTAL REVENUE" },
    ];
</script>

<section id="about"
    class="relative w-full bg-[#f0fdf4] px-6 py-20 sm:px-10 md:px-20 overflow-hidden"
>
    <!-- Sidebar Label (rotates for large screens, stacked on mobile) -->
    <div class="absolute top-8 left-[-3.5rem] hidden lg:block">
        <p
            class="text-emerald-600 font-bold text-xs tracking-widest transform -rotate-90 origin-left"
        >
            -- ABOUT US --
        </p>
    </div>

    <!-- Top visible label for mobile -->
    <div
        class="lg:hidden mb-4 text-emerald-600 font-semibold text-sm tracking-wide text-center"
    >
        -- ABOUT US --
    </div>

    <!-- Main Content -->
    <div class="max-w-6xl mx-auto text-center">
        <h2
            class="text-3xl sm:text-4xl md:text-5xl font-extrabold text-gray-900 leading-snug"
        >
            Crafting your vision. Turning innovative ideas into lasting &
            sustainable structures,<br class="hidden sm:inline" />
            with years of expertise and unwavering precision in the construction
        </h2>

        <p class="mt-6 text-gray-700 text-sm sm:text-base max-w-2xl mx-auto">
            We bring your vision to life with precision and quality. Our
            commitment to innovation and client satisfaction ensures every
            project exceeds expectations.
        </p>

        <!-- Stats Row -->
        <div
            class="mt-12 grid grid-cols-1 sm:grid-cols-3 gap-10 sm:gap-0 sm:divide-x divide-gray-300"
        >
            {#each stats as { value, label }}
                <div class="flex flex-col items-center px-4">
                    <p class="text-4xl font-bold text-emerald-600">{value}</p>
                    <p class="mt-2 text-sm text-gray-600">{label}</p>
                </div>
            {/each}
        </div>
    </div>
</section>
