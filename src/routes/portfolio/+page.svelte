<script>
    import Step from "../../lib/Step.svelte";
    
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
</script>

<section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
    <div class="flex flex-col gap-2 text-center">
        <h6 class="text-large sm:text-xl md:text-2xl">
            Explore My Creative Journey:
        </h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            A Showcase of <span class="poppins text-red-700">Innovative</span> projects
        </h3>
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
        <Step step={steps[0]}>
            <p>
                Weather Bloom is a weather application that uses the OpenWeatherMap API to <strong
                    class="text-red-700"
                    >display the current weather and forecast for any location in the world</strong
                >  making it an essential tool for anyone wanting to stay informed about the weather.
            </p>
        </Step>

        <Step step={steps[1]}>
            <p>
                HCI Simple Calculator is a <strong
                    class="text-red-700">JavaScript</strong
                >
                <strong class="text-red-700">Simple Calculator</strong
                >
                with <strong class="text-red-700">Animated background</strong> that allows users to perform basic arithmetic operations.
            </p>
        </Step>

        <Step step={steps[2]}>
            <p>
                My other works can be seen in a Google Drive folder, showcasing some of <strong class="text-red-700"
                    >my Compiled works</strong
                >
                throughout my journey as a student leader | designer | computer science student.
                Each piece reflects   
                <strong class="text-red-700">my growth and experiences</strong>, in various projects, and collaborations. 
                Feel free to explore the collection, which includes a range of designs, coding projects, 
                and leadership initiatives that highlight my creativity and commitment to excellence.
            </p>
        </Step>
    </div>
</section>