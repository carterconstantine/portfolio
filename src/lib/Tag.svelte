<script>
    let { text } = $props();
</script>

<p>{text}</p>

<style>
    @import "../styles/theme.css";
    p {
        padding: 0.5rem;
        border-radius: 9999px;
        border: 1px solid var(--accent);
        background-color: var(--bg-tertiary);
        color: var(--text);
        text-align: center;
    }
</style>