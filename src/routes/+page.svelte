<script>
    import { time } from "$lib/stores.js";
    import Link from "$lib/Link.svelte";

    const formatter = new Intl.DateTimeFormat(
        "en",
        {
            hour12 : true,
            hour: "numeric",
            minute: "2-digit",
            second: "2-digit"
        }
    );

    const projects = [
        { label : "DDA Vacature", href : "/", className : "?" },
        { label : "TouchTribe", href : "/", className : "?" },
        { label : "RedPers", href : "/", className : "?" },
        { label : "Lifely", href : "/", className : "?" },
        { label : "Kompas Publishing", href : "/", className : "?" },
        { label : "CrossMarX", href : "/", className : "?" },
    ];
</script>

<main>
    <section class="intro-section">
        <header>
            <span class="bengals">
                I LOVE
            </span>
            <span class="bengals bengals2">
                WEB?
            </span>
        </header>
        <div class="meta-info">
            <h4>
                <span>@Jason <strong> Wong </strong></span>
            </h4>

            <h4>
                <span>
                    <data id="clock" value="time">Local Time : {formatter.format($time)}</data>
                </span>
            </h4>
        </div>
        <section class="container-section">
            <div class="images-of-me">
                <div class="picture-1">
                    <img src="./young_me.jpeg" alt="Small liliputter">
                </div>
                <div class="picture-2">
                    <img src="./jsn.jpeg" alt="">
                </div>
            </div>
            <hr />
            <div class="description">
                <p>
                    Currently diving into front-end development to broaden my skills. I’m passionate about design, inspired by creative developers, aspiring to become one myself one day.
                </p>
            </div>
       </section>
    </section>

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

    <!-- <iframe style="border-radius:12px" src="https://open.spotify.com/embed/track/6m9qPYXmhge2QhBLfFKnVF?utm_source=generator&theme=0" width="50%" height="102" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe> -->

</main>

<style>

    .intro-section {
        display: flex;
        flex-direction: column;
    }

    header {
        display: flex;
        gap: 1em;
        margin-bottom: .5em;
    }

    header span {
        display: flex;
        white-space: nowrap;
        font-size: 14.75vw;
    }

    h4 span {
        opacity: 0;
        display: block;
        transform: translateY(100%);
        animation: reveal 1.8s cubic-bezier(0.77, 0, 0.175, 1) 0.3s forwards;
    }

    span.bengals {
        /* de tekst zelf is doorzichtig */
        color: transparent;
        /* 5 shadows - steeds 1.5em lager */
        text-shadow:
        0 0 0 #FFFFFF,
        0 1.5em 0 #FFFFFF,
        0 3em 0 #FFFFFF,
        0 4.5em 0 #FFFFFF,
        0 6em 0 #FFFFFF;
        /* de shadows die uitsteken zijn niet te zien */
        overflow: hidden;
        /* de transitie voor de terugweg */
	    /* de text-shadows doen er .75s over */
        animation: animateTextShadow 1.5s ease forwards;
    }
    span.bengals2 {
        transform: rotate(0.5turn);
    }

    .meta-info {
        margin-bottom: 5em;
    }

    h4 data {
        display: none;
    }

    .container-section {
        display: flex;
        flex-direction: column;
    }

    .images-of-me {
        display: grid;
        justify-content: center;
        align-content: center;
        grid-template-columns: repeat(9, 1fr);
        grid-template-rows: repeat(13, 1fr);

    }

    .images-of-me img {
        max-width: 12em;
        height: 100%;
        width: 100%;
        object-fit: cover;
        border-radius: .5em;
        opacity: 0;
        animation: reveal 2.2s cubic-bezier(0.77, 0, 0.175, 1) 0.3s forwards;
    }

    .picture-1 {
        grid-area: 1 / 2 / 9 / 6;
    }

    .picture-2 {
        grid-area: 5 / 5 / 13 / 9;
    }

    hr {
        width: 100%;
        margin: 1em 0;
        border: none; /* Remove default border */
        border-top: 2px solid #2E2C2C; /* Add a blue top border */
        animation: line-reveal 2s ease 2.25s forwards;
        opacity: 0;
    }

    .description {
        opacity: 0;
        margin: 2em;
        animation: reveal 2s cubic-bezier(0.77, 0, 0.175, 1) 0.85s forwards;
    }

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

    @media (min-width: 545px){
        .meta-info {
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            margin: 1em .5em 7.5em .5em;
        }
        h4 data {
            display: block;
        }
    }

    @media (min-width: 992px) {
        .meta-info {
            margin: 0em 3em 5em 3em;
        }
        header {
            margin: 0 .5em;
        }
        h4 data {
            display: block;
        }

        hr {
            display: none;
        }
        .container-section {
            flex-direction: row;
            justify-content: space-between;
        }

        .description {
            width: 55%;
            margin: 0 2.5em 0 0;
            align-self: flex-end;
        }
    }

</style>