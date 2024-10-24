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

<section class="my-projects-section">
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
    
    .my-projects-section {
        display: flex;
        flex-direction: column;
        margin: 5em 1.75em 0 1.75em;
        color: var(--secondary-text-color);
    }

    .my-projects-section h4 {
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
        .my-projects-section {
            margin: 16.5em 3em 0 3em;
            flex-direction: row;
            justify-content: space-between;
            align-content: center;
        }

        .my-projects-section h4 {
            font-size: 42px;
        }

        ul {
            align-items: self-end;
            font-size: calc(var(--heading-md) + .1em);
            gap: .6em;
        }
    }
</style>