<template>
    <header>
        <div class="top-header" id="start">
            <div class="d-flex-between boxed">
                <p>We have a 95% Succesfull Pass Rate!</p>
                <p>
                    <i class="fa-solid fa-phone"></i>
                    Give us a call to book your tuition! 1-800-555-555
                </p>
            </div>
        </div>

        <HeaderBottom/>

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
import HeaderBottom from './sections/HeaderBottom.vue';
export default {
    name: 'AppHeader',
    components: {
        HeaderBottom
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
                    font-size: 1.3rem;
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