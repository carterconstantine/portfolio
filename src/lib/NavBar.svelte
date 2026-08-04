<script>
    import { page } from '$app/state';
</script>

<ul>
    <li><a href="/" class:active={page.url.pathname === "/"}>Home</a></li>
    <li><a href="/projects" class:active={page.url.pathname === "/projects"}>Projects</a></li>
    <li><a href="/contact" class:active={page.url.pathname === "/contact"}>Contact</a></li>
    <li><a href="/about" class:active={page.url.pathname === "/about"}>About</a></li>
</ul>

<style>
    ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
        background-color: var(--bg-secondary);
        display: flex;
        border: 1px solid var(--accent);
        border-radius: 0.5rem;
        overflow: hidden
    }

    ul li a {
        display: block;
        color: var(--text);
        padding: 14px 16px;
        text-decoration: none;
    }

    ul li a:hover {
        background-color: var(--bg-tertiary);
    }

    ul li a.active {
        background-color: var(--accent);
        color: var(--bg-secondary);
    }
</style>