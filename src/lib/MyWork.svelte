<script>
    
    import Link from "$lib/Link.svelte";

    const projects = [
        { label : "DDA Vacature", href : "/", className : "?" },
        { label : "TouchTribe", href : "/", className : "?" },
        { label : "RedPers", href : "/", className : "?" },
        { label : "Lifely", href : "/", className : "?" },
        { label : "Kompas Publishing", href : "/", className : "?" },
        { label : "CrossMarX", href : "/", className : "?" },
    ];

</script>

<section class="my-work">
    <h4>My work</h4>
    <ul>
        {#each projects as project}
            <li>
                <Link
                    href={project.href}
                    class={project.className}
                    label={project.label}
                />
            </li>
        {/each}
    </ul>
</section>

<style>
    
    .my-work {
        display: flex;
        flex-direction: column;
        justify-content: center;
        margin: 3em 1.75em 0 1.75em;
        color: var(--secondary-text-color);
    }

    .my-work h4 {
        margin-bottom: 1.5em;
    }

    ul {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: .75em;
        font-size: calc(var(--heading-sm) - 1.5em);
    }
</style>