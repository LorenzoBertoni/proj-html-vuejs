<template>
    <header>
        <div class="top-header">
            <div class="d-flex-between boxed">
                <p>lorem ipsum</p>
                <p>lorem ipsum sit dolor amet</p>
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
                        <li>lorem</li>
                        <li>lorem</li>
                        <li>lorem</li>
                        <li>lorem</li>
                        <li>lorem</li>
                        <li>lorem</li>
                        <li>
                            <a href="#" class="btn">btn</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>

        <section id="jumbotron">
            <div class="jumbo-wrapper boxed d-flex-start">
                <div class="jumbo-text">
                    <h1>lorem Ipsum sit dolor</h1>
                    <p>lorem ipsum</p>
                </div>
            </div>
        </section>
    </header>
</template>

<script>
export default {
    name: 'AppHeader'
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
            ul {
                list-style: none;
                gap: 4rem;
                li {
                    color: #fff;
                }

                .btn {
                    background-color: $brand_color;
                    color: $btn_text_color;
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