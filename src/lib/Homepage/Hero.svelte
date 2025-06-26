<script lang="ts"></script>

<section
    class="relative min-h-[85vh] flex flex-col justify-center items-center bg-slate-50 overflow-hidden px-6 sm:px-10"
>
    <!-- Subtle grid blueprint pattern -->
    <div
        class="absolute inset-0 bg-[url('/images/blueprint-pattern.svg')] bg-repeat opacity-[0.05] z-0"
    ></div>

    <!-- Architectural GIF as a soft, moving centerpiece -->
    <img
        src="/images/buildingGlitch.gif"
        alt="Glitchy 3D Architecture"
        class="absolute top-1/2 left-1/2 w-[700px] sm:w-[600px] md:w-[800px] max-w-[1000vw] -translate-x-1/2 -translate-y-1/2 opacity-20 pointer-events-none select-none z-0"
    />

    <!-- Foreground Content -->
    <div
        class="relative z-10 text-center max-w-4xl flex flex-col items-center gap-6"
    >
        <!-- Subtle label -->
        <span
            class="uppercase tracking-wider text-sm text-slate-500 font-semibold"
        >
            Archimate Studio
        </span>

        <!-- Headline -->
        <h1
            class="text-4xl sm:text-5xl md:text-6xl font-extrabold text-slate-900 leading-tight"
        >
            We Draft <span class="text-emerald-600">Dreams</span><br />
            Into Concrete Reality
        </h1>

        <!-- Subtext -->
        <p class="text-slate-600 text-base sm:text-lg md:text-xl max-w-2xl">
            Every line tells a story. From structural detail to 3D
            elevation—this is design, precision, and soul in steel.
        </p>

        <!-- Buttons -->
        <div class="flex flex-col sm:flex-row gap-4 mt-4">
            <a
                href="#portfolio"
                class="bg-emerald-600 text-white px-6 py-3 rounded-lg text-base font-medium shadow hover:bg-emerald-700 transition"
            >
                View Portfolio
            </a>
            <a
                href="#contact"
                class="border border-slate-800 text-slate-800 px-6 py-3 rounded-lg text-base font-medium hover:bg-slate-800 hover:text-white transition"
            >
                Let’s Build Together
            </a>
        </div>
    </div>
</section>
