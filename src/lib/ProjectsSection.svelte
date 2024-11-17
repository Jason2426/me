<script>
    import Card from "$lib/Card.svelte";

    const projects = [
        { name: "DDA Vacature", type: "FDND Project", imgSrc: "./test.png", href: "" },
        { name: "TouchTribe", type: "FDND Project", imgSrc: "./test.png", href: "" }
    ];
</script>

<section class="my-work">
    <section class="intro-text">
        <p>At this moment i’m still working on great projects which will be shown on this website eventually. Note : this website can change overtime as I try to keep improving it with my current skills and the creative mindset I have at this moment. </p>
    </section>
    <section class="projects">
        {#each projects as project}
            <Card
                href={project.href}
                imgSrc={project.imgSrc}
                name={project.name} 
                type={project.type}
            />
        {/each}
    </section>
</section>

<style>
    .my-work{
        display: flex;
        flex-direction: column;
        margin: 5em 1.5em 0 1.5em;
    }

    .intro-text {
        color: #4D4D4D;
    }

    .projects {
        display: flex;
        flex-wrap: wrap;
        gap: 1.5em;
        margin-top: 3em;
    }
</style>