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
        span {
            color: $brand_color;
        }

        .social * {
            color: #fff;
            margin: 0 .5rem;
            cursor: pointer;
        }
    }
</style>