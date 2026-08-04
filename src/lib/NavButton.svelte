<script>
    let { text, link, icon:Icon } = $props();
</script>

<a href={link} class="nav-button">
    <span class="icon"><Icon /></span>
    {text}
</a>

<style>
    @import "../styles/theme.css";
    .nav-button {
        display: inline-flex;
        gap: 0.375rem;
        padding: 0.5rem;
        border-radius: 9999px;
        border: 1px solid var(--accent);
        background-color: var(--accent);
        color: var(--bg-tertiary);
        text-align: center;
        text-decoration: none;
    }
    .nav-button:active {
        background-color: var(--bg-tertiary);
        color: var(--accent)
    }
    .icon {
        width: 1rem;
        height: 1rem;
    }
</style>