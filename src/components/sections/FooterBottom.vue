<template>
    <section id="footer-bottom">
        <div class="d-flex-around boxed">
            <div class="copyright">
                <p class="main-text">
                    <i class="fa-regular fa-copyright"></i>
                    Copyright 2012 - 2020 | Avada Theme by <span>Boolean</span> | 
                    all rights reserved | Powered by <span>Vue CLI</span>
                </p>
            </div>

            <div class="social">
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-youtube"></i>
                <i class="fa-brands fa-instagram"></i>
            </div>
        </div>
        <div class="icon d-flex-center">
            <a href="#start">
                <i class="fa-solid fa-chevron-up"></i>
            </a>
        </div>
    </section>
</template>

<script>
export default {
    name: 'FooterBottom'
}
</script>

<style scoped lang="scss">
@import '../../styles/vars.scss';
    #footer-bottom {
        background-color: #1C1D1E;
        padding: 2rem 0;
        position: relative;
        span {
            color: $brand_color;
        }

        .social * {
            color: #fff;
            margin: 0 .5rem;
            cursor: pointer;
        }

        .icon {
            width: 60px;
            background-color: darkslategray;
            position: absolute;
            bottom: 0;
            right: 10%;
            border-top-left-radius: .5rem;
            border-top-right-radius: .5rem;
            padding: .5rem;
            i {
                font-size: 1.5rem;
                text-align: center;
                color: gray;
            }
        }
    }
</style>