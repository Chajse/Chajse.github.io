<script>
    export let y;
    export let innerHeight;

    export let tabs = [
        { name: "Projects ", link: "#projects" },
        { name: "About me", link: "#about" },
        { name: "Blog", class: "hover:text-red-800",  link: "https://www.youtube.com/watch?v=dQw4w9WgXcQ" },
        // { name: "Contact", link: "" },
        // {name: '', link: ''},
    ];
    let isDropdownOpen = false;
</script>

<header
    class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid " +
        (y > 0
            ? " py-4 bg-stone-950 border-red-950"
            : " py-6 bg-transparent border-transparent")}
>
    <h1 class="font-medium">
        <b class="font-bold poppins">ALLOIZEUS JOHN</b> <span class="">DE BELEN</span>
    </h1>
    <div class="sm:flex items-center gap-4 hidden">

        {#each tabs as tab, index}
            <a
                href={tab.link}
                class={"duration-200 " + (tab.name === "Blog" ? "hover:text-red-800 !important" : "hover:text-green-950")}
                target={index === 2 ? "_blank" : ""}
            >
                <p class="duration-200">{tab.name}</p>
            </a>
        {/each}
        <a href="/contact" class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-black text-white">
            <div
                class="absolute top-0 right-full w-full h-full bg-blue-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
            />
            <h4 class="relative z-9 font-afacad">Connect with Me</h4>
        </a>
    </div>
    <div class="sm:hidden relative">
        <button on:click={() => isDropdownOpen = !isDropdownOpen} class="px-4 py-2 bg-black text-white rounded flex items-center gap-2 hover:text-blue-400 duration-200">
            <i class="fas fa-bars"></i>
        </button>
        {#if isDropdownOpen}
            <div class="absolute right-0 mt-2 w-48 bg-black border border-gray-200 rounded shadow-lg transition-transform transform origin-top-right duration-200 ease-out scale-100">
                {#each tabs as tab, index}
                    <a
                        href={tab.link}
                        class="block px-4 py-2 text-white hover:text-blue-400 duration-200"
                    >
                        <p class="font-afacad">{tab.name}</p>
                    </a>
                {/each}
                <a href="/contact" class="block px-4 py-2 text-white hover:text-blue-400 duration-200 font-afacad">
                    Tap me
                </a>
            </div>
        {/if}
    </div>
</header>