<script>
    import Step from "./Step.svelte";

    let steps = [
        { name: "E-commerce Store", icon: "fa-solid fa-cart-shopping" },
        { name: "Ultimate Todos", icon: "fa-solid fa-list-check" },
        { name: "Pokedex", icon: "fa-solid fa-diagram-project" },
    ];

    let benefits = [
        {
            name: "A self-taught developer",
            description:
                "I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks, backend programming, design, cloud services and much much more.",
        },
        {
            name: "A product design & UX fanatic",
            description:
                "Carefully crafting and designing amazing user experiences allows me to express and experiment with every morsel of creativity I have. I love the challenge of learning new design concepts and enabling users with amazing online experiences.",
        },
        {
            name: "An excellent communicator",
            description:
                "Communication is key and it's a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team.",
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
                Hi! I'm <span class="poppins text-violet-400">Yash</span> Kemkar
                <br />
                Front End <span class="poppins text-violet-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400">favourite tech</span> includes JavaScript
                (Next.js, React.js or SvelteKit), TailwindCSS, Node.js and Firebase/Firestore!
            </p>
            <a
                href="#/"
                target="_blank"
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-30 group-hover:translate-x-full z-0 duration-200"
                ></div>
                <h4 class="relative z-[9]">Get in touch &rarr;</h4>
            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"images/profile.png"}
                alt="Profile image"
                class="object-cover z-2 max-h-[70vh]"
            />
        </div>
    </section>
    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my creative endeavours.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    The E-commerce store is a merchandising store created with <strong
                        class="text-violet-400"
                        >Next.js, Commerce.js, Stripe & Node.js + Express.js!
                    </strong> Commerce.js is a product CMS and Stripe is used for
                    all transaction handling.
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    Ultimate To-dos is a Full Stack <strong
                        class="text-violet-400"
                        >Next.js, Node.js + Express.js & Firebase!</strong
                    > CRUD application that allows a user to login, manage a tidy
                    and efficacious todo list, and persist this information across
                    devices.
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    The Pokedex is a <strong class="text-violet-400"
                        >React & TailwindCSS</strong
                    >
                    web application, hosted on
                    <strong class="text-violet-400">Netlify</strong>
                    that consumes and caches the
                    <strong class="text-violet-400">Pokemon API</strong> to display
                    all Pokemon information. Gotta catch em all!
                </p>
            </Step>
        </div>
    </section>
    <section
        id="about"
        class="pt-10 lg:pt-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-6"
        >
            <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am...
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-2 sm:gap-8">
                    <p
                        class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
                    </p>

                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3
                            class="text-2xl sm:text-3xl md:text-5xl text-violet-400"
                        >
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
        <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">The <span class="text-violet-400 poppins ">Complete</span> Package</h5>
        <div
            class="flex flex-col overflow x-scroll gap-10 max-w-[800px] mx-auto w-full"
        >
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class="border-b corder-solid border-slate-200">
                    <tr class="">
                        <th/>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                        <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8">Me</th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solidborder-white pl-4 pr-8 py-4 font-semibold whitespace-nowrap">Dedication</td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-violet-700"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solidborder-white pl-4 pr-8 py-4 font-semibold whitespace-nowrap">Critical Thinking</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-violet-700"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solidborder-white pl-4 pr-8 py-4 font-semibold whitespace-nowrap">Interpersonal Skills</td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-violet-700"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solidborder-white pl-4 pr-8 py-4 font-semibold whitespace-nowrap">Programming Ability</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-violet-700"></i></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
        <p class="mx-auto poppins">I'd be the perfect addition to your team. So why not invest?</p>
    </section>
    <section id="experience" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                I'm not entirely new to the workforce.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:5xl">
                Have a look at my <span class="poppins text-violet-400">professional & educational</span> background.
            </h3>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    The E-commerce store is a merchandising store created with <strong
                        class="text-violet-400"
                        >Next.js, Commerce.js, Stripe & Node.js + Express.js!
                    </strong> Commerce.js is a product CMS and Stripe is used for
                    all transaction handling.
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    Ultimate To-dos is a Full Stack <strong
                        class="text-violet-400"
                        >Next.js, Node.js + Express.js & Firebase!</strong
                    > CRUD application that allows a user to login, manage a tidy
                    and efficacious todo list, and persist this information across
                    devices.
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    The Pokedex is a <strong class="text-violet-400"
                        >React & TailwindCSS</strong
                    >
                    web application, hosted on
                    <strong class="text-violet-400">Netlify</strong>
                    that consumes and caches the
                    <strong class="text-violet-400">Pokemon API</strong> to display
                    all Pokemon information. Gotta catch em all!
                </p>
            </Step>
        </div>
    </section>
</main>
