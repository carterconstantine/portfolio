<script>
    import ProjectCard from './ProjectCard.svelte';

    import SvelteIcon from '$lib/assets/SvelteIcon.svelte';
    import CSSIcon from '$lib/assets/CSSIcon.svelte';
    import PythonIcon from '$lib/assets/PythonIcon.svelte';

    const projects = [
        {
            title: 'My Website',
            description: 'This website is a website I created to act as a way to showcase my projects and unique skills. I\'m very new to web dev, so while this website is unpolished and lacking in features right now, it will be improved as I learn more.',
            tags: [{'text':'Svelte', 'icon':SvelteIcon}, {'text':'CSS', 'icon':CSSIcon}],
            link: "https://github.com/carterconstantine/website"
        },
        {
            title: 'Beat Saber Score Feed',
            description: 'Beat Saber Score Feed is an open source discord bot that posts Beat Saber scores from any of the 3 major leaderboards (ScoreSaber, BeatLeader, and AccSaber) in a channel for people to view. It\'s highly configurable and can be set up in any server.',
            tags: [{'text':'Python', 'icon':PythonIcon}],
            link: "https://github.com/Beat-Saber-Score-Feed/Score-Feed-Bot"
        },
        {
            title: 'Latte',
            description: 'Latte is an open-source discord bot I developed for my friend\'s server, inspired by his cat. The bot can send pictures of his cat, "chomp" users, and handle a few other tasks that the community uses frequently.',
            tags: [{'text':'Python', 'icon':PythonIcon}],
            link: "https://github.com/carterconstantine/latte"
        }
    ];
</script>

<h2>My Projects:</h2>

<div class="grid">
    {#each projects as project}
        <ProjectCard {...project} />
    {/each}
</div>

<style>
    .grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 1.5rem;
        width: 90%;
        margin: 0 auto;
    }

    h2 {
        font-size: 2rem;
        text-align: center;
    }
</style>