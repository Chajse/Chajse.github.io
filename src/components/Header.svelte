<script>
    export let y;

    export let tabs = [
        { name: "Projects ", link: "#projects" },
        { name: "About me", link: "#about" },
        { name: "Blog", class: "hover:text-red-800",  link: "https://www.youtube.com/watch?v=dQw4w9WgXcQ" },
        // { name: "Contact", link: "" },
        // {name: '', link: ''},
    ];
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
    </div>
</header>