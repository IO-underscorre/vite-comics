<script>
export default {
    name: 'FooterNavigationSection',

    data() {
        return {
            footerNavCategories: [
                {
                    title: 'DC COMICS',
                    links: [
                        {
                            text: 'Characters',
                            url: '#'
                        },
                        {
                            text: 'Comics',
                            url: '#'
                        },
                        {
                            text: 'Movie',
                            url: '#'
                        },
                        {
                            text: 'TV',
                            url: '#'
                        },
                        {
                            text: 'Games',
                            url: '#'
                        },
                        {
                            text: 'Videos',
                            url: '#'
                        },
                        {
                            text: 'News',
                            url: '#'
                        }
                    ]
                },
                {
                    title: 'SHOP',
                    links: [
                        {
                            text: 'Shop DC',
                            url: '#'
                        },
                        {
                            text: 'Shop DC Collectibles',
                            url: '#'
                        }
                    ]
                },
                {
                    title: 'DC',
                    links: [
                        {
                            text: 'Terms Of Use',
                            url: '#'
                        },
                        {
                            text: 'Privacy policy (New)',
                            url: '#'
                        },
                        {
                            text: 'Ad Choices',
                            url: '#'
                        },
                        {
                            text: 'Advertising',
                            url: '#'
                        },
                        {
                            text: 'Jobs',
                            url: '#'
                        },
                        {
                            text: 'Subscriptions',
                            url: '#'
                        },
                        {
                            text: 'Talent Workshops',
                            url: '#'
                        },
                        {
                            text: 'CPSC Certificates',
                            url: '#'
                        },
                        {
                            text: 'Ratings',
                            url: '#'
                        },
                        {
                            text: 'Shop Help',
                            url: '#'
                        },
                        {
                            text: 'Contact Us',
                            url: '#'
                        }
                    ]
                },
                {
                    title: 'SITES',
                    links: [
                        {
                            text: 'DC',
                            url: '#'
                        },
                        {
                            text: 'MAD Magazine',
                            url: '#'
                        },
                        {
                            text: 'DC Kids',
                            url: '#'
                        },
                        {
                            text: 'DC Universe',
                            url: '#'
                        },
                        {
                            text: 'DC Power Visa',
                            url: '#'
                        }
                    ]
                }
            ]
        }
    }
}
</script>

<template>
    <section class="footer-navigation-section">
        <div class="content-box">
            <nav>
                <div class="nav-category" v-for="(category , index) in footerNavCategories" :key="index">
                    <strong>
                        {{ category.title }}
                    </strong>
                    
                    <menu>
                        <li v-for="link in category.links">
                            <a :href="link.url">
                                {{ link.text }}
                            </a>
                        </li>
                    </menu>
                </div>
            </nav>

            <div class="background-logo">
                <img src="../assets/dc-logo-bg.png" alt="DC Comics">
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.footer-navigation-section {
    background-image: url("../assets/footer-bg.jpg");
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;

    .content-box {
        @include flex-space-between-center;
        gap: 20%;
        height: $hgt-footer-section-navigation;
        overflow: hidden;

        nav {
            height: 100%;
            flex: 0 0 fit-content;
            display: flex;
            flex-flow: column wrap;
            gap: 1.5rem;
            padding: 2.75rem 0;
        
            .nav-category {
                width: fit-content;

                strong {
                    display: block;
                    color: $clr-text-lt;
                    font-size: $fnt-size-lg;
                    margin-bottom: .75rem;
                }

                li {
            
                    a {
                        font-size: $fnt-size-sm;
                    
                        &:hover {
                            color: $clr-text-lt;
                        }
                    }
                }
            }
        }

        .background-logo {
            flex: 1 0;
            overflow: hidden;

            img {
                width: 100%;
            }
        }
    }
}
</style>