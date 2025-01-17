<script>
    import Step from "../components/Step.svelte";

    // Steps for projects
    let steps = [
        {
            name: "Controlling Mouse Pointer Using Face and Eye Gestures for Quadriplegic Patients",
            icon: "fa-solid fa-mouse-pointer",
            description:
                "Designed a system to control a mouse pointer through facial and eye gestures using computer vision techniques like Haar Cascade and AdaBoost. This system aimed to provide accessibility for quadriplegic patients.",
        },
        {
            name: "AI-Powered Intrusion Detection System",
            icon: "fa-solid fa-shield-alt",
            description:
                "Implemented a real-time network intrusion detection system using machine learning algorithms to classify malicious traffic. Deployed the solution on AWS for scalability and reliability.",
        },
        {
            name: "Threat Intelligence Using Natural Language Processing",
            icon: "fa-solid fa-brain",
            description:
                "Built a threat intelligence platform using NLP to extract actionable insights from cybersecurity blogs and reports. Integrated SpaCy and NLTK for text processing and visualized results using Power BI.",
        }
    ];

    // Benefits for the about section
    let benefits = [
        {
            name: "Technical Expertise",
            description:
                "Proficient in Python, C, JavaScript, R, and secure coding practices. Skilled in using tools like Metasploit, Wireshark, Splunk, and machine learning frameworks (Scikit-learn, TensorFlow, PyTorch).",
        },
        {
            name: "Cybersecurity enthusiast",
            description:
                "Certified in CEH and AWS Machine Learning. Experienced in penetration testing, cryptography, and compliance with frameworks like NIST, ISO/IEC 27001, and GDPR.",
        },
        {
            name: "Innovative Problem-Solver",
            description:
                "Passionate about leveraging AI and machine learning to drive proactive threat detection and improve cybersecurity solutions. Adept at integrating cutting-edge technologies into practical applications.",
        },
        {
            name: "Strong Communicator and Team Player",
            description:
                "Effective communicator with a focus on transparency and collaboration. Excels in fostering productive relationships and achieving team goals in diverse environments.",
        },
    ];

    // Function to handle email redirects
    function openEmail() {
        window.location.href = 'mailto:meghana.msismpl2024@learner.manipal.edu';
    }
</script>

<main class="flex flex-col flex-1 p-4">
    <!-- Intro Section -->
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Meghana D Duttargi</span>
                <br />Cybersecurity and <span class="poppins text-violet-400">Data AI Enthusiast</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                Leveraging expertise in cybersecurity and AI to drive proactive threat detection and innovative problem-solving. Skilled in network security, penetration testing, and machine learning frameworks.
            </p>
            <button
                on:click={openEmail}
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950">
                <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"></div>
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </button>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"../assest/images/WhatsApp Image 2025-01-16 at 16.28.20_cd8a09c2.jpg"}
                alt="Meghana D Duttargi"
                class="object-cover z-[2] max-h-[70vh]"
            />
        </div>
    </section>

    <!-- Projects Section -->
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">A few of my creative endeavors.</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            {#each steps as step}
                <Step step={step}>
                    <p>{step.description}</p>
                </Step>
            {/each}
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center py-4">
            <h6 class="text-large sm:text-xl md:text-2xl">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">{benefit.name}</h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
        <h5 class={" text-2xl sm:text-3xl font-semibold text-center poppins "}>
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
        </div>
        <p class="mx-auto">So why not invest?</p>
    
    </section>
    
</main>
