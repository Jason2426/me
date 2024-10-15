<script>

</script>


<main>
    <section class="intro-section">
        <header>
            <span class="bengals">
                I LOVE
            </span>
            <span class="bengals2">
                WEB?
            </span>
        </header>
        <!-- <div class="meta-info">
            <h2>
                @Jason <strong> Wong </strong>
            </h2>

            <h2 hidden>
                <data value="time">hey</data>
            </h2>
        </div>
        <div class="images-of-me">
            <div class="pic-1">
                <img src="" alt="">
            </div>
            <div class="pic-2">
                <img src="" alt="">
            </div>
        </div>
        <hr>
        <div class="description">
            <p>
                Currently diving into front-end development to broaden my skills. I’m passionate about design, inspired by creative developers, aspiring to become one myself one day.
            </p>
        </div> -->
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

    span {
        display: flex;
        text-wrap: nowrap;
        font-size: 15vw;
    }

    span.bengals {
        color: transparent;
        text-shadow:
        0 0 0 #FFFFFF,
        0 1.5em 0 #FFFFFF,
        0 3em 0 #FFFFFF,
        0 4.5em 0 #FFFFFF,
        0 6em 0 #FFFFFF;
        overflow: hidden;
        animation: animateTextShadow 1.5s ease forwards;
    }

    span.bengals2 {
        transform: rotate(0.5turn);
        color: transparent;
        text-shadow:
        0 6em 0 #FFFFFF,
        0 4.5em 0 #FFFFFF,
        0 3em 0 #FFFFFF,
        0 1.5em #FFFFFF,
        0 0 0 #FFFFFF;
        overflow: hidden;
        animation: animateTextShadow 1.5s ease forwards;
    }
        @keyframes animateTextShadow {
        0% {
            text-shadow:
            0 6em 0 #FFFFFF,
            0 4.5em 0 #FFFFFF,
            0 3em 0 #FFFFFF,
            0 1.5em 0 #FFFFFF,
            0 0 0 #FFFFFF;
        }
        100% {
            text-shadow:
            0 0 0 #FFFFFF,
            0 -1.5em 0 #FFFFFF,
            0 -3em 0 #FFFFFF,
            0 -4.5em 0 #FFFFFF,
            0 -6em 0 #FFFFFF;
        }
    }

</style>