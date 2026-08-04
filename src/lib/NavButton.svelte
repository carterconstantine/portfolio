<script>
    let { text, link } = $props();
</script>

<a href={link}>{text}</a>

<style>
    @import "../styles/theme.css";
    a {
        padding: 0.5rem;
        border-radius: 9999px;
        border: 1px solid var(--accent);
        background-color: var(--accent);
        color: var(--bg-tertiary);
        text-align: center;
        text-decoration: none;
    }
    a:active {
        background-color: var(--bg-tertiary);
        color: var(--accent)
    }
</style>