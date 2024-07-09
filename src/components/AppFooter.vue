<script>
import FooterNavigationSection from './FooterNavigationSection.vue';

export default {
    name: 'AppFooter',

    components: {
        FooterNavigationSection
    },

    data() {
        return {
            socialLinks: [
                {
                    social: 'Facebook',
                    url: '#',
                    iconFileName: 'facebook.png'
                },
                {
                    social: 'Periscope',
                    url: '#',
                    iconFileName: 'periscope.png'
                },
                {
                    social: 'Pinterest',
                    url: '#',
                    iconFileName: 'pinterest.png'
                },
                {
                    social: 'Twitter',
                    url: '#',
                    iconFileName: 'twitter.png'
                },
                {
                    social: 'Youtube',
                    url: '#',
                    iconFileName: 'youtube.png'
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
    <footer>
        <FooterNavigationSection />

        <section class="bottom-socials-bar content-box">
            <a href="#" class="visual-btn">
                SIGN-UP NOW!
            </a>

            <div class="socials">
                <span>
                    FOLLOW US
                </span>

                <ul>
                    <li v-for="link in socialLinks">
                        <a :href="link.url">
                            <img :src="this.getFilePath(`../assets/social-icons/${link.iconFileName}`)" :alt="link.social">
                        </a>
                    </li>
                </ul>
            </div>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
footer {
    background-color: #303030;
    color: $clr-text;

    .bottom-socials-bar {
        @include flex-space-between-center;
        height: $hgt-footer-section-socials;

        .socials{
            @include flex-space-between-center;
            gap: 1.5rem;

            span {
                color: $clr-primary;
                font-size: $fnt-size-lg;
                font-weight: 700;
            }
            
            ul {
                @include flex-space-between-center;
                gap: 1rem;

                li {
                    width: 2.25rem;
                    height: 2.25rem;
                    border-radius: 50%;

                    &:hover {
                        filter: brightness(150%);
                    }
                
                    img {
                        width: 100%;
                        object-fit: cover;
                    }
                }
            }
        }
    }
}
</style>