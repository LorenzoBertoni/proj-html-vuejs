<template>
    <section id="instructors" class="boxed">
        <h4>Your instructors</h4>
        <div class="d-flex">
            <div class="right-side">
                <p class="main-text">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quae, voluptatibus cum non, laudantium assumenda suscipit ab repellat illo amet explicabo voluptates! Voluptatum eius, voluptas rerum dolor itaque corporis ad deleniti!</p>
            </div>

            <div class="left-side">
                <a href="#" class="btn">MORE ABOUT US</a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionInstructors'
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';
    h4 {
        font-size: 2rem;
        color: $title_color;
    }

    .right-side {
        width: 60%;

        p {
            margin-top: 1.5rem;
            color: $text_color;
            line-height: 1.5rem;
        }
    }

    .left-side {
        width: 40%;
        display: flex;
        justify-content: center;
        a {
            background-color: $brand_color;
            padding: .7rem 4rem;
            color: #fff;
        }
    }
</style>