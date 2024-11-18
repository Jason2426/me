<script>
    import Card from "$lib/Card.svelte";

    const projects = [
        { name: "DDA Vacature", type: "FDND Project", imgSrc: "./test.png", href: "" },
        { name: "TouchTribe", type: "FDND Project", imgSrc: "./test.png", href: "" },
        { name: "RedPers", type: "FDND Project", imgSrc: "./test.png", href: "" },
        { name: "Kompas", type: "Personal Project", imgSrc: "./test.png", href: "" },
        { name: "Kompas", type: "Personal Project", imgSrc: "./test.png", href: "" },
        { name: "Kompas", type: "Personal Project", imgSrc: "./test.png", href: "" },
        { name: "Kompas", type: "Personal Project", imgSrc: "./test.png", href: "" },
        { name: "Kompas", type: "Personal Project", imgSrc: "./test.png", href: "" },
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
        margin: 7.5em 1.5em 0 1.5em;
    }

    .intro-text {
        display: flex;
        justify-content: center;
        text-align: center;
        color: #3b3b3b;
        width: 100%;
    }

    .intro-text p{
        max-width: 100%;
    }

    .projects {
        display: grid;
        justify-content: center;
        align-items: center;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        gap: 1.5em;
        margin-top: 3em;
    }

    @media(min-width: 720px){

    .intro-text p{
        font-size: 1em;
        max-width: 75%;
    }
        .projects{
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        }
    }

    @media(min-width: 1120px){
        .intro-text p{
             max-width: 37.5%;
    }
    }

    @media(min-width: 1320px){
        .projects{
            grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
        }
    }

</style>