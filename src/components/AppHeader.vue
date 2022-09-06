<template>
    <header>
        <div class="top-header">
            <div class="d-flex-between boxed">
                <p>We have a 95% Succesfull Pass Rate!</p>
                <p>
                    <i class="fa-solid fa-phone"></i>
                    Give us a call to book your tuition! 1-800-555-555
                </p>
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
                            <a :href="'#' + link.goTo"
                            :class="link.isNew? 'new' : '' ">
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

                <div class="jumbo-cards">
                    <div class="card">
                        <i class="fa-solid fa-file"></i>
                        <p>Demos</p>
                    </div>

                    <div class="card two">
                        <p class="icon">$39</p>
                        <p>On Sale</p>
                    </div>
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
                                isNew: false,
                                goTo: 'jumbotron' 
                            },
                            {
                                name: 'about',
                                isActive: false,
                                isNew: false,
                                goTo: 'instructors'
                            },
                            {
                                name: 'prices',
                                isActive: false,
                                isNew: false,
                                goTo: 'news-letter'
                            },
                            {
                                name: 'courses',
                                isActive: false,
                                isNew: true,
                                goTo: 'courses'
                            },
                            {
                                name: 'location',
                                isActive: false,
                                isNew: false,
                                goTo: 'footer-top'
                            },
                            {
                                name: 'blog',
                                isActive: false,
                                isNew: false,
                                goTo: ''
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
                margin-top: 3px;
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
                            color: #7F9EA8;
                        }
                        &.new::after {
                            content: 'New';
                            width: 60px;
                            padding: .3rem .5rem;
                            border-radius: .5rem;
                            background-color: $brand_color;
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
        padding: 15rem 0;
        position: relative;
        .jumbo-wrapper {
            .jumbo-text {
                color: #fff;
                h1 {
                    font-size: 4rem;
                    margin-bottom: .5rem;
                }

                p {
                    font-size: 1.1rem;
                }
            }
            .jumbo-cards {
                .card, .two {
                    width: 70px;
                    padding: .5rem;
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    position: absolute;
                    i {
                        font-size: 1.5rem;
                        color: #7F9EA8;
                        margin-bottom: .5rem;
                    }

                    p {
                        color: #7F9EA8;
                        font-size: .8rem;
                    }
                }

                .card {
                    top: 1rem;
                    right: 1rem;
                }

                .two {
                    top: 6rem;
                    right: 1rem;
                    .icon {
                        font-size: 1.5rem;
                        color: $brand_color;
                        font-weight: 700;
                    }
                }
            }
        }
    }
</style>