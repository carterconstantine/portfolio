<script>
    import ContactCard from "$lib/ContactCard.svelte";
    import MailIcon from "$lib/assets/MailIcon.svelte"
    import CopyIcon from "$lib/assets/CopyIcon.svelte"
    import GithubIcon from "$lib/assets/GithubIcon.svelte"
    import LinkedInIcon from "$lib/assets/LinkedInIcon.svelte"

    const contacts = [
        {
            title: "Dev Email",
            description: "My main contact email is contact@carterconst.dev, please use this email for contacting me about my projects or business opportunities.",
            navButtons: [
                {
                    "text": "Open Email",
                    "link": "mailto:contact@carterconst.dev",
                    "icon": MailIcon,
                }
            ],
            copyButtons: [
                {
                    "text": "Copy Email",
                    "copytext": "contact@carterconst.dev",
                    "icon": CopyIcon,
                }
            ]
        },
        {
            title: "Personal Email",
            description: "My personal email is constantine.carter09@gmail.com, feel free to use this for everything else!",
            navButtons: [
                {
                    "text": "Open Email",
                    "link": "mailto:constantine.carter09@gmail.com",
                    "icon": MailIcon,
                }
            ],
            copyButtons: [
                {
                    "text": "Copy Email",
                    "copytext": "constantine.carter09@gmail.com",
                    "icon": CopyIcon,
                }
            ]
        },
        {
            title: "Discord",
            description: "My Discord username is carterconst, reach out on here for more chill conversations if you don't want to use email.",
            copyButtons: [
                {
                    "text": "Copy Username",
                    "copytext": "carterconst",
                    "icon": CopyIcon,
                }
            ]
        },
        {
            title: "Github",
            description: "My Github username is carterconstantine, you can check out my projects here or submit bug reports on the Issues tab of my projects.",
            navButtons: [
                {
                    "text": "Open Github",
                    "link": "https://github.com/carterconstantine",
                    "icon": GithubIcon,
                }
            ],
            copyButtons: [
                {
                    "text": "Copy Username",
                    "copytext": "carterconstantine",
                    "icon": CopyIcon,
                }
            ]
        },
        {
            title: "LinkedIn",
            description: "I don't use LinkedIn much since I'm not actively looking for a job or internships, but feel free to connect with me here!",
            navButtons: [
                {
                    "text": "Open LinkedIn",
                    "link": "https://linkedin.com/in/carterconst",
                    "icon": LinkedInIcon,
                }
            ]
        }
    ]
</script>

<h2>Contact:</h2>

<p>Have a question about my work? Please contact me on one of the platforms below.</p>

<div class="grid">
    {#each contacts as contact}
        <ContactCard {...contact} />
    {/each}
</div>

<style>
    h2 {
        font-size: 2rem;
        text-align: center;
    }
    p {
        text-align: center;
    }
    .grid {
        display: grid;
        grid-template-columns: repeat(3, minmax(300px, 1fr));
        gap: 1.5rem;
        width: 90%;
        margin: 0 auto;
    }
    @media (max-width: 1000px) {
        .grid {
            grid-template-columns: repeat(2, minmax(300px, 1fr));
        }
    }
    @media (max-width: 650px) {
        .grid {
            grid-template-columns: 1fr;
        }
    }
</style>