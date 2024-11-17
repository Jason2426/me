<script>
    export let href, imgSrc, name, type;
</script>

<a href={href}>
    <article>
        <section class="main-img">
            <img src={imgSrc} alt="">
        </section>
        <section class="meta-info">
            <p>{name}</p>
            <p>{type}</p>
        </section>
    </article>
</a>

<style>
    a {
        text-decoration: none;
        color: #303030;
    }
    article {
        display: flex;
        flex-direction: column;
        background-color: #181818;
        border-radius: .25em;
    }
    .main-img{
        margin: 4em 2.5em 2em 2.5em;
    }
    img {
        max-width: 100%;
        object-fit: cover;
        border-radius: .25em;
    }
    .meta-info {
        display: flex;
        justify-content: space-between;
        font-size: 12px;
        font-weight: bold;
        font-family: Arial, Helvetica, sans-serif;
        margin: 1.5em;
    }
</style>