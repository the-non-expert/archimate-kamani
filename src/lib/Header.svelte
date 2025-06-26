<script lang="ts">
    import { Menu, X } from "lucide-svelte";
    let isOpen = false;

    const navLinks = [
        { name: "Home", href: "/" },
        { name: "About", href: "/#about" },
        { name: "Portfolio", href: "#portfolio" },
        { name: "Services", href: "#services" },
        { name: "Contact", href: "#contact" },
    ];
</script>

<header class="w-full bg-white/90 backdrop-blur-md shadow-sm sticky top-0 z-50">
    <div
        class="max-w-7xl mx-auto px-4 sm:px-8 md:px-12 py-4 flex items-center justify-between"
    >
        <!-- Left: Logo + Brand Name -->
        <a href="/" class="flex items-center gap-4">
            <img
                src="/images/Logo.png"
                alt="Archimate Logo"
                class="h-10 w-auto sm:h-16"
            />
            <div class="border-l-2 pl-4 border-slate-300">
                <span
                    class="text-2xl sm:text-3xl font-bold tracking-tight text-slate-900"
                    >Archimate</span
                >
                <p class="text-sm text-slate-500  sm:block leading-none">
                    Architectural Detailing & Design
                </p>
            </div>
        </a>

        <!-- Desktop Navigation -->
        <nav
            class="hidden md:flex space-x-8 items-center text-xl font-bold"
        >
            {#each navLinks as link}
                <a
                    href={link.href}
                    class="relative text-slate-700 hover:text-emerald-600 transition"
                >
                    <span>{link.name}</span>
                    <span
                        class="absolute bottom-0 left-0 w-0 h-[2px] bg-emerald-600 transition-all duration-300 group-hover:w-full"
                    ></span>
                </a>
            {/each}
        </nav>

        <!-- Mobile Menu Button -->
        <button
            class="md:hidden text-slate-700"
            on:click={() => (isOpen = !isOpen)}
            aria-label="Toggle Menu"
        >
            {#if isOpen}
                <X class="w-6 h-6" />
            {:else}
                <Menu class="w-6 h-6" />
            {/if}
        </button>
    </div>

    <!-- Mobile Dropdown -->
    {#if isOpen}
        <div class="md:hidden px-6 py-4 border-t bg-white flex flex-col gap-4">
            {#each navLinks as link}
                <a
                    href={link.href}
                    class="text-slate-700 hover:text-emerald-600 transition"
                    >{link.name}</a
                >
            {/each}
        </div>
    {/if}
</header>
