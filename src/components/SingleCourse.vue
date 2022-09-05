<template>
    <div class="course d-flex-column-center boxed">
        <img :src="require('../assets/img/' + path)" :alt="title">
        <h4>{{title}}</h4>
        <button class="btn">LEARN MORE</button>
    </div>
</template>

<script>
export default {
    name: 'SingleCourse',
    props: {
        path: String,
        title: String,
    }
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';

    .course {
            gap: 1rem;
        }

        img {
            cursor: pointer;
        }

        h4 {
            color: #7F9EA8;
        }

        .btn {
            border: 3px solid $btn-secondary;
            color: $btn-secondary;
            transition: all .3s linear;
            &:hover {
                border: 3px solid $brand_color;
                color: $brand_color;
            }
        }
</style>