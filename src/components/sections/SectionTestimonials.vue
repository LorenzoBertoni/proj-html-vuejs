<template>
    <section id="testimonials">
        <div class="d-flex-column-center boxed">
            <h2 class="title">Testimonials</h2>
            <p class="main-text">
                Here's what our happy drivers had to say about our services:
            </p>
            <div class="img-wrapper">
                <img :src="require('../../assets/img/' + testimonials[active].url)" 
                :alt="'Photo for ' + testimonials[active].name"
                >
            </div>

            <div class="testimonial-experience">
                <p class="main-text boxed">
                    {{testimonials[active].isSaying}}
                </p>
            </div>

            <div class="testimonials-name">
                <h4 class="main-text">
                    {{testimonials[active].name}}
                </h4>
            </div>

            <div class="icons">
                <div 
                class="icon"
                v-for="(icon, index) in testimonials" 
                :key="index"
                :class="index == active? 'active' : '' "
                >
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionTestimonials',
    data() {
        return {
            active: 0,
            testimonials:   [
                                {
                                    name: 'Sophia Jones',
                                    url: 'testimonial-sophia.png',
                                    isSaying: 'Avada Driving School really helped me build my confidence behind the whell and with driving in general, and they got me a first time pass! Highly recommended'
                                },
                                {
                                    name: 'Grant Hart',
                                    url: 'testimonial-grant.png',
                                    isSaying: 'Avada Driving School really helped me build my confidence behind the whell and with driving in general, and they got me a first time pass!'
                                },
                                {
                                    name: 'Harold Smith',
                                    url: 'testimonial-harold.png',
                                    isSaying: 'Avada Driving School really helped me build my confidence behind the whell and with driving in general'
                                },
                                {
                                    name: 'Kate Jones',
                                    url: 'testimonial-kate.png',
                                    isSaying: 'Avada Driving School really helped me build my confidence behind the whell and with driving in general, and they got me a first time pass! Highly recommended'
                                },
                                {
                                    name: 'Kelly Doe',
                                    url: 'testimonial-kelly.png',
                                    isSaying: 'Avada Driving School really helped me build my confidence behind the whell and with driving in general. Highly recommended!'
                                }
                            ]
        }
    },
    methods: {
        getNext() {
            if(this.active < (this.testimonials.length - 1)) {
                this.active++;
            } else if (this.active == (this.testimonials.length - 1)) {
                this.active = 0;
            }
        }
    },
    mounted() {
        setInterval(this.getNext, 10000);
    }
}
</script>

<style scoped lang="scss">

    #testimonials {
        padding: 10rem 0;
        background-image: url('../../assets/img/testimonial-background.jpg');
        background-size: cover;
        background-position: center;
        .d-flex-column-center {
            height: inherit;
            .img-wrapper {
                width: 150px;
                height: 150px;
                border-radius: 50%;
                margin-top: 2.5rem;
                img {
                    width: 100%;
                    height: 100%;
                }
            }

            .testimonial-experience {
                p {
                    text-align: center;
                    margin-top: 1rem;
                    margin-bottom: 1rem;
                }
            }

            .icon {
                width: 10px;
                height: 10px;
                border: 1px solid gray;
                border-radius: 50%;
                display: inline-block;
                margin: 1rem .3rem;
                &.active {
                    background-color: gray;
                }
            }
        }
    }
</style>