<script>

export let label, className, href;
</script>

<a
    href={href}
    class={className}>
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