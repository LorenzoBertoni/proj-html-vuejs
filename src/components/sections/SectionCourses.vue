<template>
    <section id="courses">
        <div class="d-flex boxed">
            <div class="card">
                <div class="card-text boxed">
                    <img src="../../assets/img/new-corner.jpg">
                    <h3>Courses</h3>
                    <p 
                    class="main-text"
                    >
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime nam libero deserunt ipsa adipisci. Aspernatur dolores fugit vitae error
                    </p>
                    <button class="btn">COURSE INFORMATION</button>
                </div>
            </div>

            <div class="courses-types d-flex-between">
                <SingleCourse 
                :path="'courses-passplus-200x200.jpg'"
                :title="'Pass Plus'"
                />

                <SingleCourse 
                :path="'course-intensive-200x200.jpg'"
                :title="'Intensive Course'"
                />

                <SingleCourse
                :path="'courses-instructor-200x200.jpg'"
                :title="'Instructors'"
                />
            </div>
        </div>
    </section>
</template>

<script>
import SingleCourse from '../SingleComponents/SingleCourse.vue';
export default {
    name: 'SectionCourses',
    components: {
        SingleCourse
    }
}
</script>

<style scoped lang="scss">
@import '../../styles/vars.scss';

    #courses {
        background-image: url('../../assets/img/promise-background.jpg');
        background-position: center;
        background-size: cover;
        background-color: lightgray;
        .card {
            width: 30%;
            margin-right: 2.5rem;
            position: relative;
            img {
                width: 25%;
                position: absolute;
                top: 0;
                left: 0;
            }

            .card-text {
                h3 {
                    font-size: 1.5rem;
                    color: $title_color;
                    margin: 2.5rem 0;
                }
    
                p {
                    margin-bottom: 1.5rem;
                }
    
                .btn {
                    background-color: $brand_color;
                    color: $btn_text_color;
                    margin-bottom: 2rem;
                }
            }
        }

        .courses-types {
            width: 70%;
        }
    }
</style>