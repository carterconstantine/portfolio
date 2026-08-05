<script>
    import Tag from "$lib/Tag.svelte";
    import Button from "$lib/Button.svelte";

    import GithubIcon from "~icons/mdi/github";

    let { title, description, tags, link } = $props();
</script>

<div class="card">
    <h3>{title}</h3>

    <p>{description}</p>

    <div class="bottom">
        <div class="tags">
            {#each tags as tag}
                <Tag {...tag} />
            {/each}
        </div>

        <div class="button">
            <Button text="Source Code" href = {link} icon={GithubIcon} />
        </div>
    </div>
</div>

<style>
    @import "../styles/theme.css";
    .card {
        background-color: var(--bg-secondary);
        border: 1px solid var(--accent);
        border-radius: 1rem;
        display: flex;
        flex-direction: column;
        padding: 0 1rem 0 1rem;
    }
    h3 {
        font-size: 1.5rem;
        text-align: center;
    }
    p {
        padding: 0;
    }
    .bottom {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-top: auto;
        margin-bottom: 1rem;
        white-space: nowrap;
    }
    .tags {
        display: flex;
        flex-wrap: wrap;
        gap: 0.5rem;
    }

</style>