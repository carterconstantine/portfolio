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
        align-items: center;
        justify-content: center;
        gap: 0.375rem;
        padding: 0.5rem;
        border-radius: 9999px;
        border: 1px solid var(--accent);
        background-color: var(--bg-tertiary);
        color: var(--accent);
        text-align: center;
    }

    .icon {
        width: 1rem;
        height: 1rem;
    }
</style>