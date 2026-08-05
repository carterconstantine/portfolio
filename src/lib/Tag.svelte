<script>
    let { text, icon: Icon } = $props();
</script>

<div class="tag">
    <div class="icon"><Icon /></div>
    {text}
</div>

<style>
    @import "../styles/theme.css";
    .tag {
        display: inline-flex;
        gap: 0.375rem;
        padding: 0.5rem;
        border-radius: 9999px;
        border: 1px solid var(--accent);
        background-color: var(--bg-tertiary);
        color: var(--accent);
    }

    .icon {
        width: 1em;
        height: 1em;
    }
</style>