<script lang="ts">
    let name = "";
    let email = "";
    let message = "";

    function handleSubmit() {
        // Placeholder: Hook this up with your backend or email API
        alert(`Message sent from ${name} (${email})`);
        name = "";
        email = "";
        message = "";
    }
</script>

<section
    id="contact"
    class="bg-emerald-600 text-white px-6 py-20 sm:px-10 md:px-24"
>
    <div
        class="max-w-6xl mx-auto grid grid-cols-1 lg:grid-cols-2 gap-12 items-center"
    >
        <!-- Left: Textual Call-to-Action -->
        <div>
            <p
                class="text-sm font-semibold tracking-wide uppercase text-white/70 mb-2"
            >
                -- Get in Touch --
            </p>
            <h2
                class="text-3xl sm:text-4xl md:text-5xl font-bold leading-tight mb-6"
            >
                Let’s build something <span class="text-emerald-100"
                    >remarkable</span
                > together.
            </h2>
            <p class="text-white/90 text-base sm:text-lg">
                Whether it's a dream home, commercial space, or innovative
                structure, we're ready to bring your vision to life. Send us a
                message and we'll get back within 24 hours.
            </p>
        </div>

        <!-- Right: Contact Form -->
        <form
            on:submit|preventDefault={handleSubmit}
            class="bg-white rounded-xl p-6 shadow-lg text-gray-800 space-y-4"
        >
            <input
                type="text"
                placeholder="Your Name"
                bind:value={name}
                required
                class="w-full px-4 py-3 rounded-md border border-gray-300 focus:outline-none focus:ring-2 focus:ring-emerald-500"
            />
            <input
                type="email"
                placeholder="Your Email"
                bind:value={email}
                required
                class="w-full px-4 py-3 rounded-md border border-gray-300 focus:outline-none focus:ring-2 focus:ring-emerald-500"
            />
            <textarea
                placeholder="Your Message"
                bind:value={message}
                required
                class="w-full px-4 py-3 rounded-md border border-gray-300 h-32 resize-none focus:outline-none focus:ring-2 focus:ring-emerald-500"
            ></textarea>
            <button
                type="submit"
                class="bg-emerald-600 text-white px-6 py-3 rounded-md font-medium hover:bg-emerald-700 transition"
            >
                Send Message
            </button>
        </form>
    </div>
</section>
