<template>
    <main>
        <SectionLessons/>

        <div class="cta">
            <div class="d-flex-between boxed">
                <div class="left-side">
                    <h3>Start Learning to Drive Today</h3>
                    <p>Give us a call to schedule your first driving lesson</p>
                </div>

                <div class="right-side">
                    <h3>1-800-555-555</h3>
                </div>
            </div>
        </div>

        <SectionCourses/>
        <div class="bg-effect">
            <img src="../assets/img/latestnews-bottom-new-color.png" alt="">
        </div>
        
        <CoursesPercentages/>
    </main>
</template>

<script>
import SectionLessons from './SectionLessons.vue';
import SectionCourses from './SectionCourses.vue';
import CoursesPercentages from './CoursesPercentages.vue';

export default {
    name: 'AppMain',
    components: {
        SectionLessons,
        SectionCourses,
        CoursesPercentages
    }
}
</script>

<style scoped lang="scss">
    .cta {
        background-color: lightblue;
        background-image: url('../assets/img/horizontal-cta-background.jpg');
        background-position: center;
        background-size: cover;
        color: #fff;
        padding: 5rem 0;
        .left-side {
            h3 {
                margin-bottom: .5rem;
            }
        }
    }

    .bg-effect {
        img {
            max-width: 100%;
        }
    }

    
</style>