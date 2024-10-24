<script>
    
    import Link from "$lib/Link.svelte";

    const projects = [
        { label : "DDA Vacature", href : "/"},
        { label : "TouchTribe", href : "/"},
        { label : "RedPers", href : "/"},
        { label : "Lifely", href : "/"},
        { label : "Kompas Publishing", href : "/"},
        { label : "CrossMarX", href : "/"},
    ];

</script>

<section class="my-work">
    <h4>My work</h4>
    <ul>
        {#each projects as project}
            <li>
                <Link
                    href={project.href}
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
        margin: 5em 1.75em 0 1.75em;
        color: var(--secondary-text-color);
    }

    .my-work h4 {
        font-family: var(--arvo-italic-bold);
        margin-bottom: 1.5em;
    }

    ul {
        display: flex;
        flex-direction: column;
        gap: .75em;
        font-size: calc(var(--heading-sm) - .4em);
    }

    @media (min-width: 820px){
        .my-work {
            margin: 12em 3em 0 3em;
            flex-direction: row;
            justify-content: space-between;
        }

        .my-work h4 {
            font-size: 34px;
        }

        ul {
            align-items: self-end;
            font-size: calc(var(--heading-md) + .5em);
        }
    }
</style>