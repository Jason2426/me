<script>

    import { time } from "$lib/stores.js";

    const formatter = new Intl.DateTimeFormat(
        "en",
        {
            hour12 : true,
            hour: "numeric",
            minute: "2-digit",
            second: "2-digit"
        }
    );

</script>

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
    <section class="sub-section">
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

    .sub-section {
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
        margin: 1.5em;
        animation: reveal 2s cubic-bezier(0.77, 0, 0.175, 1) 0.85s forwards;
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
        .sub-section {
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
