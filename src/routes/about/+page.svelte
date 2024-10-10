
<script>
    let about = [
        {
            metric: "10x",
            name: "a self taught ui/ux designer & developer",
            description:
                "I discovered my passion for designing through internet starting with Canva, HTML-CSS and Figma. My journey has since expanded to include JavaScript frameworks, design, allowing me to create online experiences.",
        },
        {
            name: "a graphic designer",
            description:
                "As a graphic designer, I blend creativity with strategy to communicate ideas visually.With an eye for aesthetics and a passion for innovation, I create compelling designs that resonate with audiences across various platforms.",
        },
        {
            name: "a student trader",
            description:
                " As a passionate student trader, I am actively learning the ins and outs of forex trading, stocks, and cryptocurrency. My enthusiasm for trading drives me to explore the markets, analyze trends, and develop strategies. I’m dedicated to honing my skills and embracing the challenges of this dynamic field.",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
            id="about"
            class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
        >
        
            <div
                class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-green-950 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-green-950 py-4"
            >
                <h6 class="text-large sm:text-xl md:text-2xl">
                    Want to know more?
                </h6>
                <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                    A bit <span class="poppins text-red-700">about</span> me.
                </h3>
            </div>
            <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
                I am . . .
            </p>
            <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
                {#each about as about, index}
                
                    <div class="flex gap-6 sm:gap-8">
                        <p
                            class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                        >
                            0{index + 1}
                        </p>
                        <div class="flex flex-col gap-6 sm:gap-8">
                            <h3 class="text-2xl sm:text-3xl md:text-5xl">
                                {about.name}
                            </h3>
                            <p>{about.description}</p>
                        </div>
                    </div>
                {/each}
            </div>
    </section>
</main>