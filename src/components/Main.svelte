<script>
    import Step from "./Step.svelte";

    let steps = [
        {
            name: "Weather Bloom",
            href: "https://github.com/Chajse/WeatherBloom.git",
            icon: "fa-solid fa-umbrella",
            description:
                "A weather application that uses the OpenWeatherMap API to display the current weather and forecast for any location in the world.",
        },
        {
            name: "Simple Calculator",
            icon: "fa-solid fa-calculator",
            href: "https://github.com/Chajse/HCI_CALCULATOR.git",
            description:
                "A simple calculator application that allows users to perform basic arithmetic operations.",
        },
        {
            name: "Other Works",
            icon: "fa-brands fa-windows",
            href: "https://drive.google.com/drive/folders/1Hr_J-ZUIMinyHE0pD0UhWgUUATDd4he1?usp=sharing",
            description:
                "Augment your datasets with our filters and dataset manipulations to ensure your models are trained on the highest quality datasets (coming soon).",
        },
    ];

    let benefits = [
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
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Alloizeus John</span>
                <br />UI/UX
                <span class="poppins text-violet-400">Designer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400 font-bold">favorite tech</span> includes Adobe Softwares, Figma, and Canva.
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

    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    Weather Bloom is a weather application that uses the OpenWeatherMap API to <strong
                        class="text-violet-400"
                        >display the current weather and forecast for any location in the world</strong
                    >  making it an essential tool for anyone wanting to stay informed about the weather.
                </p>
            </Step>

            <Step step={steps[1]}>
                <p>
                    HCI Simple Calculator is a <strong
                        class="text-violet-400">JavaScript</strong
                    >
                    <strong class="text-violet-400">Simple Calculator</strong
                    >
                    with <strong class="text-violet-400">Animated background</strong> that allows users to perform basic arithmetic operations.
                </p>
            </Step>

            <Step step={steps[2]}>
                <p>
                    My other works can be seen in a Google Drive folder, showcasing some of <strong class="text-violet-400"
                        >my Compiled works</strong
                    >
                    throughout my journey as a student leader | designer | computer science student.
                    Each piece reflects   
                    <strong class="text-violet-400">my growth and experiences</strong>, in various projects, and collaborations. 
                    Feel free to explore the collection, which includes a range of designs, coding projects, 
                    and leadership initiatives that highlight my creativity and commitment to excellence.
                </p>
            </Step>
        </div>
    </section>
    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
       
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
            <h6 class="text-large sm:text-xl md:text-2xl">
                Want to know more?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
               
                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
        <!--<h5 class={" text-2xl sm:text-3xl font-semibold text-center poppins "}>
            The <span class="text-violet-400">Complete</span> Package
        </h5>
        <div
            class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
        >
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class={"border-b border-solid border-slate-200  "}>
                    <tr class="">
                        <th />
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                        <th
                            class="bg-violet-700 text-white whitespace-nowrap p-4 px-8"
                            >Me</th
                        >
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Dedication</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Critical Thought</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr>
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Interpersonal Skills</td
                        >
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr class="border-t border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Progamming Ability</td
                        >
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>-->
    </section>
</main>