<template>
    <main>
        <SectionLessons/>

        <section class="cta">
            <div class="d-flex-around boxed">
                <div class="left-side">
                    <h3>Start Learning to Drive Today</h3>
                    <h4>Give us a call to schedule your first driving lesson</h4>
                </div>

                <div class="right-side">
                    <p>1-800-555-555</p>
                </div>
            </div>
        </section>

        <SectionCourses/>
        <div class="bg-effect">
            <img src="../assets/img/latestnews-bottom-new-color.png">
        </div>
        <CoursesPercentages/>

        <SectionInstructors/>

        <SectionTestimonials/>

        <SectionLatestNews/>

        <SectionNewsLetter/>
    </main>
</template>

<script>
import SectionLessons from './SectionLessons.vue';
import SectionCourses from './SectionCourses.vue';
import CoursesPercentages from './CoursesPercentages.vue';
import SectionInstructors from './SectionInstructors.vue';
import SectionTestimonials from './SectionTestimonials.vue';
import SectionLatestNews from './SectionLatestNews.vue';
import SectionNewsLetter from './SectionNewsLetter.vue';

export default {
    name: 'AppMain',
    components: {
        SectionLessons,
        SectionCourses,
        CoursesPercentages,
        SectionInstructors,
        SectionTestimonials,
        SectionLatestNews,
        SectionNewsLetter
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
                font-size: 2rem;
            }
        }

        .right-side {
            p {
                font-size: 2rem;
            }
        }
    }

    .bg-effect {
        img {
            max-width: 100%;
        }
    }

    
</style>