<script>
export default {
    name: 'ComicsUtilitiesSection',

    data() {
        return {
            comicsUtilitiesLinks: [
                {
                    text: 'DIGITAL COMICS',
                    url: '#',
                    iconFileName: 'buy-comics-digital-comics.png'
                },
                {
                    text: 'DC MERCHANDISE',
                    url: '#',
                    iconFileName: 'buy-comics-merchandise.png'
                },
                {
                    text: 'SUBSCRIPTION',
                    url: '#',
                    iconFileName: 'buy-comics-subscriptions.png'
                },
                {
                    text: 'COMIC SHOP LOCATOR',
                    url: '#',
                    iconFileName: 'buy-comics-shop-locator.png'
                },
                {
                    text: 'DC POWER VISA',
                    url: '#',
                    iconFileName: 'buy-dc-power-visa.svg'
                }
            ]
        }
    },

    methods: {
        getFilePath(pathToFile) {
            return new URL(pathToFile, import.meta.url).href;
        }
    }
}
</script>

<template>
    <section class="comics-utilities-section">
        <menu class="content-box">
            <li v-for="(link , index) in comicsUtilitiesLinks" :key="index">
                <a :href="link.url">
                    <div class="linkIcon">
                        <img :src="getFilePath(`../assets/buy-icons/${link.iconFileName}`)" :alt="link.text">
                    </div>

                    <span>
                        {{ link.text }}
                    </span>
                </a>
            </li>
        </menu>
    </section>
</template>

<style lang="scss" scoped>
.comics-utilities-section {
    background-color: $clr-primary;
    color: $clr-secondary;

    .content-box {
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        padding: 3rem 0;

        a {
            @include flex-space-between-center;
            gap: .75rem;

            &:hover {
                text-decoration: underline;
            }

            .linkIcon {
                width: 3.5rem;
                height: 3.5rem;

                img {
                    width: 100%;
                    height: 100%;
                    object-fit: contain;
                }
            }
        }
    }
}
</style>