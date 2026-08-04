<script>
    import Tag from "$lib/Tag.svelte";

    let { title, description, tags } = $props();
</script>

<div class="card">
    <h3>{title}</h3>

    <p>{description}</p>

    <div class="tags">
        {#each tags as tag}
            <Tag text={tag} />
        {/each}
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
    .tags {
        display: flex;
        flex-wrap: wrap;
        gap: 0.5rem;
        margin: auto 0 0;
    }
</style>