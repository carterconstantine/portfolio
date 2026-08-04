<script>
    import NavButton from "$lib/NavButton.svelte";
    import CopyButton from "$lib/CopyButton.svelte";

    let { title, description, navButtons, copyButtons } = $props();
</script>

<div class="card">
    <h3>{title}</h3>

    <p>{description}</p>

    <div class="bottom">
        <div class="nav-buttons">
            {#each navButtons as button}
                <NavButton {...button} />
            {/each}
        </div>

        <div class="copy-buttons">
            {#each copyButtons as button}
                <CopyButton {...button} />
            {/each}
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
        justify-content: space-between;
        align-items: center;
        margin-top: auto;
        margin-bottom: 1rem;
        white-space: nowrap;
        gap: 0.5rem
    }

</style>