<script>
export default {
    name: 'TopNavigationBar',

    data() {
        return {
            navBarLinks: [
                {
                    text: 'CHARACTERS',
                    url: '#',
                    isSelected: false
                },
                {
                    text: 'COMICS',
                    url: '#',
                    isSelected: true
                },
                {
                    text: 'MOVIES',
                    url: '#',
                    isSelected: false
                },
                {
                    text: 'TV',
                    url: '#',
                    isSelected: false
                },
                {
                    text: 'GAMES',
                    url: '#',
                    isSelected: false
                },
                {
                    text: 'COLLECTIBLES',
                    url: '#',
                    isSelected: false
                },
                {
                    text: 'VIDEOS',
                    url: '#',
                    isSelected: false
                },
                {
                    text: 'FANS',
                    url: '#',
                    isSelected: false
                },
                {
                    text: 'NEWS',
                    url: '#',
                    isSelected: false
                },
                {
                    text: 'SHOP',
                    url: '#',
                    isSelected: false
                }
            ]
        }
    }
}
</script>

<template>
    <nav>
        <div class="content-box">
            <a href="#" class="logo">
                <img src="../assets/dc-logo.png" alt="DC Comics">
            </a>

            <menu>
                <li :class="{ selected: link.isSelected }" v-for="link in navBarLinks">
                    <a :href="link.url">
                        {{ link.text }}
                    </a>
                </li>
            </menu>
        </div>
    </nav>
</template>

<style lang="scss" scoped>
nav {
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 100;
    font-weight: 700;
    color: $clr-text-dk;
    background-color: $clr-secondary;

    .content-box {
        @include flex-space-between-center;
        height: $hgt-top-bar;

        .logo {
            display: block;
            height: 5rem;

            img {
                height: 100%
            }
        }

        menu {
            height: 100%;
            display: flex;
            justify-content: center;
            gap: 2rem;

            li {
                display: flex;
                flex-direction: column;
                justify-content: center;

                &:hover {
                    color: $clr-primary;
                }

                &.selected {
                    color: $clr-primary;
                    position: relative;

                    &::after {
                        content: '';
                        width: 100%;
                        height: 5px;
                        background-color: $clr-primary;
                        position: absolute;
                        bottom: 0;
                        right: 0;
                    }
                }
            }
        }
    }
}
</style>
