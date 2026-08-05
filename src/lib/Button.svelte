<script>
    let { href, onclick, copytext, text, icon: Icon } = $props();

    let copied = $state(false);

    async function copyText() {
        await navigator.clipboard.writeText(copytext);
        copied = true;

        setTimeout(() => {
            copied = false;
        }, 2000);
    }
</script>

{#if href}
    <a href={href} class="button">
        <span class="icon">
            <Icon />
        </span>
        {text}
    </a>
{:else if copytext}
    <button class="button" onclick={copyText}>
        <span class="icon">
            <Icon />
        </span>
        {copied ? "Copied!" : text}
    </button>
{:else}
    <button class="button" onclick={onclick}>
        <span class="icon">
            <Icon />
        </span>
        {text}
    </button>
{/if}

<style>
    @import "../styles/theme.css";

    .button {
        display: inline-flex;
        font: inherit;
        line-height: inherit;
        gap: 0.375rem;
        padding: 0.5rem;
        border-radius: 9999px;
        border: 1px solid var(--accent);
        background-color: var(--accent);
        color: var(--bg-tertiary);
        text-decoration: none;
        cursor: pointer;
        transition: transform 0.15s, background-color 0.15s;
    }
    .button:active {
        background-color: var(--bg-tertiary);
        color: var(--accent)
    }
    .button:hover {
        transform: scale(110%);
        background-color: color-mix(in srgb, var(--accent), white 20%);
    }
    .icon {
        width: 1em;
        height: 1em;
    }
</style>