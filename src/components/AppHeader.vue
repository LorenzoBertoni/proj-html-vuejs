<template>
    <header>
        <div class="top-header">
            <div class="d-flex-between boxed">
                <p>We have a 95% Succesfull Pass Rate!</p>
                <p>Give us a call to book your tuition! 1-800-555-555</p>
            </div>
        </div>

        <div class="bottom-header">
            <div class="d-flex-between boxed">
                <div class="logo-wrapper">
                    <a href="#">
                        <img 
                        src="../assets/img/avada-drivers-logo-1x.png"
                        alt="logo for Avada driving school"
                        >
                    </a>
                </div>
                
                <nav class="nav-bar">
                    <ul class="d-flex-end">
                        <li v-for="(link, index) in navLinks" :key="index"
                        :class="link.isActive? 'active' : '' "
                        >
                            <a href="#">
                                {{link.name.toUpperCase()}}
                            </a>
                        </li>

                        <li>
                            <a href="#" class="btn">BOOK NOW</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>

        <section id="jumbotron">
            <div class="jumbo-wrapper boxed d-flex-start">
                <div class="jumbo-text">
                    <h1>Drive with Avada</h1>
                    <p>We offer the finest driving tuition money can buy</p>
                </div>
            </div>
        </section>
    </header>
</template>

<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            navLinks:   [
                            {
                                name: 'home',
                                isActive: true,
                                isNew: false
                            },
                            {
                                name: 'about',
                                isActive: false,
                                isNew: false
                            },
                            {
                                name: 'prices',
                                isActive: false,
                                isNew: false
                            },
                            {
                                name: 'courses',
                                isActive: false,
                                isNew: true
                            },
                            {
                                name: 'location',
                                isActive: false,
                                isNew: false
                            },
                            {
                                name: 'blog',
                                isActive: false,
                                isNew: false
                            },
                        ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';

    .top-header {
        background-color: $header_color;
        padding: 1rem 0;

        p {
            color: #7F9EA8;
        }
    }

    .bottom-header {
        background-color: gray;
        padding: 2rem 0;
        .logo-wrapper {
            a {
                img {
                    width: 100%;
                }
            }
        }
        .nav-bar {
            .active {
                border-bottom: 3px solid $brand_color;
            }

            ul {
                list-style: none;
                gap: 4rem;
                li {
                    a {
                        color: #fff;
                        font-weight: bold;
                        cursor: pointer;
                        transition: color .3s linear;
                        text-decoration: none;
                        &:hover:not(.btn) {
                            color: $brand_color;
                        }
                    }
                }

                .btn {
                    background-color: $brand_color;
                    color: $btn_text_color;
                    transition: background-color .3s linear;
                    &:hover {
                        background-color: #48644B;
                    }
                }
            }
        }
    }

    #jumbotron {
        background-color: lightblue;
        background-image: url('../assets/img/homepage-hero-background.jpg');
        background-size: cover;
        background-position: center;
        padding: 20rem 0;
        .jumbo-wrapper {
            .jumbo-text {
                color: #fff;
                h1 {
                    font-size: 3rem;
                    margin-bottom: .5rem;
                }

                p {
                    font-size: 1.1rem;
                }
            }
        }
    }
</style>