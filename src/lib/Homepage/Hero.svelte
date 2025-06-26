<script lang="ts">
    let current = 0;
    const interval = 3000;

    const slides = [
        {
            image: "/images/slide2.jpg",
            title: "Structuring the Future",
            subtext: "We blend creativity with construction expertise.",
            button: { text: "Explore Work", href: "#portfolio" },
        },
        {
            image: "/images/slide1.jpg",
            title: "Designing Dreams",
            subtext: "From concept to creation — your vision is our blueprint.",
            button: { text: "Our Process", href: "#services" },
        },
        {
            image: "/images/slide3.jpg",
            title: "Elevating Skylines",
            subtext: "Turning ideas into iconic realities.",
            button: { text: "Let's Talk", href: "#contact" },
        },
        {
            image: "/images/slide4.jpg",
            title: "Minimal. Functional. Beautiful.",
            subtext: "Crafting architectural identities with clarity.",
            button: { text: "Know Us", href: "#about" },
        },
    ];

    const startCarousel = () => {
        setInterval(() => {
            current = (current + 1) % slides.length;
        }, interval);
    };

    startCarousel();
</script>

<section class="relative min-h-[90vh] w-full overflow-hidden">
    {#each slides as slide, i}
        <div
            class={`absolute inset-0 w-full h-full transition-opacity duration-1000 bg-cover bg-center ${
                i === current ? "opacity-100 z-10" : "opacity-0 z-0"
            }`}
            style="background-image: url({slide.image})"
        >
            <!-- Dark overlay -->
            <div class="absolute inset-0 bg-black/50"></div>

            <!-- Foreground content -->
            <div
                class="relative z-10 flex flex-col items-center justify-center text-center h-full px-6 sm:px-12"
            >
                <h1
                    class="text-4xl sm:text-5xl md:text-6xl font-bold text-white leading-tight mb-4"
                >
                    {slide.title}
                </h1>
                <p class="text-lg sm:text-xl text-white/90 mb-8 max-w-xl">
                    {slide.subtext}
                </p>
                <a
                    href={slide.button.href}
                    class="bg-emerald-600 text-white px-6 py-3 rounded-full font-medium hover:bg-emerald-700 transition"
                >
                    {slide.button.text}
                </a>
            </div>
        </div>
    {/each}
</section>
