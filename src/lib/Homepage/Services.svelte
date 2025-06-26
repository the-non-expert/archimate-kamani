<script lang="ts">
    import { PenTool, Ruler, Layout, Building2, ToyBrick
 } from "lucide-svelte";

    const services = [
        {
            name: "Drafting",
            icon: PenTool,
            description:
                "Precision CAD drawings tailored to your architectural vision.",
        },
        {
            name: "Detailing",
            icon: Ruler,
            description:
                "Intricate component detailing that brings designs to life.",
        },
        {
            name: "Layout",
            icon: Layout,
            description:
                "Functional and aesthetic spatial planning for every project.",
        },
        {
            name: "3D Elevation",
            icon: Building2,
            description:
                "Photorealistic renders that visualize the final outcome.",
        },
        {
            name: "Structural Detailing",
            icon: ToyBrick,
            description:
                "Engineering-grade drawings for robust construction integrity.",
        },
    ];
</script>

<section id="services" class="bg-emerald-50 px-6 py-20 sm:px-10 md:px-20">
    <!-- Header -->
    <div class="text-center mb-12">
        <p class="text-emerald-600 font-semibold text-sm tracking-wide">
            -- SERVICES --
        </p>
        <h2
            class="text-3xl sm:text-4xl md:text-5xl font-bold text-gray-900 mt-2"
        >
            Our Core Expertise
        </h2>
        <p class="mt-4 text-gray-700 max-w-2xl mx-auto text-sm sm:text-base">
            We provide complete architectural solutions—from pen to pixel, draft
            to detail.
        </p>
    </div>

    <!-- Services Grid -->
    <div
        class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 max-w-6xl mx-auto"
    >
        {#each services as service}
            <div
                class="bg-white p-6 rounded-xl shadow hover:shadow-lg transition group border border-gray-200"
            >
                <!-- Icon -->
                <svelte:component
                    this={service.icon}
                    class="w-8 h-8 text-emerald-600 mb-4 group-hover:scale-110 transition-transform"
                />
                <h3 class="text-xl font-semibold text-gray-800 mb-2">
                    {service.name}
                </h3>
                <p class="text-gray-600 text-sm">{service.description}</p>
            </div>
        {/each}
    </div>
</section>
