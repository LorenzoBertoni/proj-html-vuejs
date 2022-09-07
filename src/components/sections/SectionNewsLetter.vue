<template>
    <section id="news-letter">
        <div class="d-flex-column-center">
            <h2 class="title">
                Sign Up to our Newsletter
            </h2>

            <form 
            action="" 
            method="get" 
            class="d-flex-column-center">
                <input class="input-style" type="email" required>
                <button class="btn">SUBSCRIBE</button>
            </form>

            <p class="main-text">
                <small>(We do not share your data with anybody, and only use it for its intended purpose)</small>
            </p>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionNewsLetter'
}
</script>

<style scoped lang="scss">
@import '../../styles/vars.scss';
    #news-letter {
        background-image: url('../../assets/img/newsletter_background.jpg');
        background-position: center;
        background-size: cover;
        .d-flex-column-center {
            width: 60%;
            margin: 0 auto;
            width: inherit;
            .title {
                margin: 2.5rem 0 3rem 0;
            }
            .input-style {
                background-color: #fff;
                width: 100%;
            }
            .btn {
                background-color: $brand_color;
                padding: 1rem 20rem;
                margin-top: 2rem;
                color: $btn_text_color;
            }
            p {
                margin: 1.5rem 0 3rem 0;
            }
        }
    }
</style>