<template>
    <section id="instructors" class="boxed">
        <h2 class="title">Your instructors</h2>
        <div class="d-flex">
            <div class="right-side">
                <p class="main-text">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quae, voluptatibus cum non, laudantium assumenda suscipit ab repellat illo amet explicabo voluptates! Voluptatum eius, voluptas rerum dolor itaque corporis ad deleniti!</p>
            </div>

            <div class="left-side">
                <a href="#" class="btn">MORE ABOUT US</a>
            </div>
        </div>

        <div class="instructors-cards d-flex">
            <div class="card"
            v-for="(instructor, index) in instructors" :key="index"
            >
                <div class="boxed">
                    <div class="img-wrapper">
                        <img :src="require('../../assets/img/' + instructor.url)" 
                        :alt="'instructor ' + instructor.name"
                        >
                    </div>

                    <h4 class="name">{{instructor.name}}</h4>

                    <div class="icons">
                        <i class="fa-brands fa-facebook-f"></i>
                        <i class="fa-brands fa-twitter"></i>
                        <i class="fa-brands fa-instagram"></i>
                    </div>

                    <div class="about-me">
                        <p class="main-text">
                            {{instructor.aboutMe}}
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionInstructors',
    data() {
        return {
            instructors:    [
                                {
                                    name: 'Mike Hart',
                                    url: 'instructor-mikehart-400x254.jpg',
                                    aboutMe: 'lorem ipsum doloret sit amet,consectetur adipiscing elit'
                                },
                                {
                                    name: 'John Smith',
                                    url: 'instructor-johnsmith-400x254.jpg',
                                    aboutMe: 'lorem ipsum doloret sit amet,consectetur adipiscing elit'
                                },
                                {
                                    name: 'Angela Hart',
                                    url: 'instructor-angelahart-400x254.jpg',
                                    aboutMe: 'lorem ipsum doloret sit amet,consectetur adipiscing elit'
                                }
                            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../../styles/vars.scss';

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
            padding: .7rem 6rem;
            color: #fff;
        }
    }

    .instructors-cards {
        gap: .5rem;
        .card {
            width: calc(100% / 3);
            padding: 2rem 0;
            transform: translateY(4rem);
            border-top: 5px solid $brand_color;
            .img-wrapper {
                img {
                    width: 100%;
                    transition: all linear .3s;
                    &:hover {
                        box-shadow: 1px 5px 5px 8px rgba(0,0,0,0.10);
                    }
                }
            }
            .name {
                font-size: 1.3rem;
                color: $title_color;
                margin: 1rem 0;
            }

            .icons * {
                color: $text_color;
                margin: 0 .5rem;
            }

            .about-me {
                margin-top: 1rem;
            }
        }
    }
</style>