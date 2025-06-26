<script lang="ts">
    const projects = [
        {
            title: "Skyline Apartments",
            category: "Residential",
            image: "/images/slide5.jpg",
        },
        {
            title: "Zenith Tower",
            category: "Commercial",
            image: "/images/slide5.jpg",
        },
        {
            title: "Natura Villas",
            category: "Luxury Villas",
            image: "/images/slide5.jpg",
        },
        {
            title: "Element Hub",
            category: "Mixed Use",
            image: "/images/slide5.jpg",
        },
        {
            title: "Vista Pavilion",
            category: "Public Infrastructure",
            image: "/images/slide5.jpg",
        },
        {
            title: "Coral Nest",
            category: "Eco Housing",
            image: "/images/slide5.jpg",
        },
    ];
</script>

<section id="portfolio" class="bg-white px-6 py-20 sm:px-10 md:px-20">
    <!-- Section Heading -->
    <div class="text-center mb-12">
        <p class="text-emerald-600 font-semibold text-sm tracking-wide">
            -- PORTFOLIO --
        </p>
        <h2
            class="text-3xl sm:text-4xl md:text-5xl font-bold text-gray-900 mt-2"
        >
            Selected Works
        </h2>
        <p class="mt-4 text-gray-600 max-w-2xl mx-auto text-sm sm:text-base">
            A glimpse into our world of forms, function, and finesse. Each
            project is a step toward transforming skylines and lives.
        </p>
    </div>

    <!-- Projects Grid -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
        {#each projects as project}
            <div
                class="group relative overflow-hidden rounded-xl shadow hover:shadow-xl transition duration-300 bg-gray-100"
            >
                <!-- Image -->
                <div
                    class="h-64 bg-cover bg-center transition-transform duration-300 group-hover:scale-105"
                    style="background-image: url({project.image})"
                ></div>

                <!-- Overlay content -->
                <div
                    class="absolute bottom-0 inset-x-0 bg-black/60 text-white px-5 py-4"
                >
                    <h3 class="text-lg font-semibold">{project.title}</h3>
                    <p class="text-sm text-emerald-300">{project.category}</p>
                </div>
            </div>
        {/each}
    </div>
</section>
