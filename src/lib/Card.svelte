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
        background-color: #141414;
        border-radius: .25em;
    }

    article:hover .main-img {
        transition: .25s;
        transform: translateY(-.5em);
    }

    .main-img {
        margin: 4em 3em 2em 3em;
    }

    img {
        max-width: 100%;
        object-fit: cover;
        border-radius: .25em;
    }

    .meta-info {
        display: flex;
        justify-content: space-between;
    }

    .meta-info p {
        color: #363636;
        font-family: Arial, Helvetica, sans-serif;
        font-weight: bold;
        font-size: 1em;
        margin: 1em;
    }

    @media(min-width: 1120px){
        .main-img{
            margin: 4em 5em 4em 5em;
        }
    }

</style>