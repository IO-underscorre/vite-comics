<script>
export default {
    name: 'ComicSerie',

    props: {
        comicTitle: String,
        comicImgLink: String
    }
}
</script>

<template>
    <article>
        <figure>
            <img :src="comicImgLink" :alt="comicTitle">
        </figure>

        <strong>
            {{ comicTitle }}
        </strong>
    </article>
</template>

<style lang="scss" scoped>
article {
    width: 100%;

    figure {
        width: 100%;
        aspect-ratio: 1 / 1;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;
        }
    }

    strong {
        display: block;
        overflow-wrap: break-word;
        padding: 1.5rem 0;
        color: $clr-text-lt;
        font-size: .75rem;
        text-transform: uppercase;
    }
}
</style>