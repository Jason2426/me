<script>
    import { onMount } from 'svelte';

    let time = '';
    const updateTime = () => {
        const now = new Date();
        time = now.toLocaleTimeString(undefined, {
            hour: '2-digit',
            minute: '2-digit',
            second: '2-digit',
            hour12: false
        });
    };

    onMount(() => {
        updateTime();
        const interval = setInterval(updateTime, 1000);
        return () => clearInterval(interval);
    });
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
                <span><data id="clock" value="time">Local Time : {time}</data></span>
            </h4>
        </div>
        <div class="images-of-me">
            <div class="pic-1">
                <img src="" alt="">
            </div>
            <div class="pic-2">
                <img src="" alt="">
            </div>
        </div>
        <hr hidden>
        <div class="description">
            <p>
                Currently diving into front-end development to broaden my skills. I’m passionate about design, inspired by creative developers, aspiring to become one myself one day.
            </p>
        </div>
    </section>

    <section class="my-work">
        <h2>Have a look at my work</h2>
        <article>
            <h4>
                TouchTribe
            </h4>
            <span>
                Design & Front-End
            </span>
            <svg><!--Arrow Btn--></svg>
            <img src="" alt="">
        </article>
    </section>

</main>

<style>

    .intro-section {
        display: flex;
        flex-direction: column;
    }

    header {
        display: flex;
        gap: 1em;
    }

    header span {
        display: flex;
        text-wrap: nowrap;
        font-size: 14.75vw;
    }

    h4 data {
        display: none;
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

    

    .description {
        display: none;
    }

    .my-work {
        display: none;
    }

</style>