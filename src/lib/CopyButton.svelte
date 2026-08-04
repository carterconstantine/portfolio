<script>
    let { text, copytext, icon:Icon } = $props();

    let copied = $state(false);

    async function copyText() {
        await navigator.clipboard.writeText(copytext);
        copied = true;

        setTimeout(() => {
            copied = false;
        }, 2000);
    }
</script>

<button class:copied class="copy-button" onclick={copyText}>
    {#if Icon}
        <span class="icon"><Icon /></span>
    {/if}
    {copied ? "Copied!" : text}
</button>

<style>
    @import "../styles/theme.css";
    .copy-button {
        display: inline-flex;
        font: inherit;
        line-height: inherit;
        gap: 0.375rem;
        padding: 0.5rem;
        border-radius: 9999px;
        border: 1px solid var(--accent);
        background-color: var(--accent);
        color: var(--bg-tertiary);
        text-align: center;
        text-decoration: none;
        cursor: pointer;
    }
    .copy-button:active {
        background-color: var(--bg-tertiary);
        color: var(--accent)
    }
    .icon {
        width: 1rem;
        height: 1rem;
    }
</style>