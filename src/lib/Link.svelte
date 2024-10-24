<script>

export let label, href;
</script>

<a
    href={href}
    >
    {label}
</a>

<style>

    a {
        text-decoration: none;
        color: inherit;
    }

    a:hover {
        color: white;
        transition: .25s;
    }
</style>