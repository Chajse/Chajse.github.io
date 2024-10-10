<!--<script>

    import Main from "../components/Main.svelte";
</script>


<Main />-->

<script>

</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-red-700">Alloizeus John</span>
                <br />UI/UX
                <span class="poppins text-red-700">Designer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-red-700 font-bold">favorite tech</span> includes Adobe Softwares, Figma, and Canva.
                I also like the JavaScript (Svelte, React, and Node) and Python programming language.
            </p>
        </div>

        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"images/profile.png"}
                alt="Zetane Engine"
                class="object-cover z-[2] max-h-[70vh]"/>
        </div>

    </section>
</main>