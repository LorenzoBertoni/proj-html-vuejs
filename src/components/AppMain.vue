<template>
    <main>
        <SectionLessons/>

        <SectionCta/>

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
import SectionLessons from './sections/SectionLessons.vue';
import SectionCourses from './sections/SectionCourses.vue';
import CoursesPercentages from './sections/CoursesPercentages.vue';
import SectionInstructors from './sections/SectionInstructors.vue';
import SectionTestimonials from './sections/SectionTestimonials.vue';
import SectionLatestNews from './sections/SectionLatestNews.vue';
import SectionNewsLetter from './sections/SectionNewsLetter.vue';
import SectionCta from './sections/SectionCta.vue';

export default {
    name: 'AppMain',
    components: {
        SectionLessons,
        SectionCourses,
        CoursesPercentages,
        SectionInstructors,
        SectionTestimonials,
        SectionLatestNews,
        SectionNewsLetter,
        SectionCta
    }
}
</script>

<style scoped lang="scss">
    .bg-effect {
        img {
            max-width: 100%;
        }
    }
</style>