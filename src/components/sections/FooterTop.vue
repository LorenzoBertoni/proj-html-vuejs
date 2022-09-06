<template>
    <section id="footer-top">
        <div class="d-flex-center boxed">
            <div class="school-info">
                <div class="logo-wrapper">
                    <img 
                    src="../../assets/img/avada-drivers-logo-1x.png" 
                    alt="Avada Driving School Logo"
                    >
                </div>

                <p class="main-text">
                    Avada Driving School is the right choice for experienced drivers looking for a refresher course, or the brand new drivers wanting to pass first time.
                </p>
            </div>

            <div class="contacts">
                <h4>CONTACT DETAILS</h4>
                <div class="contact-details">
                    <div class="address">
                        <i class="fa-solid fa-house-chimney"></i>
                        <p class="main-text">12345 North Main Street, <br> New York, NY 555555</p>
                    </div>

                    <div class="phone-number">
                        <i class="fa-solid fa-phone"></i>
                        <p class="main-text">1.800.555.6789</p>
                    </div>

                    <div class="email">
                        <i class="fa-regular fa-envelope"></i>
                        <p class="main-text">info@your-domain.com</p>
                    </div>

                    <div class="site">
                        <i class="fa-solid fa-link"></i>
                        <p class="main-text">Theme-fusion.com</p>
                    </div>
                </div>
            </div>

            <div class="courses">
                <h4>COURSES</h4>
                <div 
                class="course"
                v-for="(course, index) in courses"
                :key="index"
                >
                    <i class="fa-solid fa-circle-arrow-right"></i>
                    <p class="main-text">{{course.name}}</p> 
                </div>
            </div>

            <div class="brand-info d-flex-column-center">
                <img src="../../assets/img/footer-ad-grid-200x178.png" alt="Brand Info">
                <a href="#" class="btn">BOOK NOW</a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'FooterTop',
    data() {
        return {
            courses:    [
                            {
                                name: 'Pass Plus'
                            },
                            {
                                name: 'Intensive Course'
                            },
                            {
                                name: 'Automatic'
                            },
                            {
                                name: 'Instructor Training'
                            }
                        ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../../styles/vars.scss';

    #footer-top {
        padding: 5rem 0 8rem 0;
        background-image: url('../../assets/img/footer-background-color.jpg');
        background-position: center;
        background-size: cover;
        .d-flex-center {
            gap: 2rem;
            .school-info,
            .contacts,
            .courses,
            .brand-info {
                width: calc(25% - 2rem);
                padding: .5rem .2rem;
            }

            .main-text {
                font-weight: 600;
            }

            h4 {
                color: #fff;
                margin-bottom: 1rem;
            }

            .address,
            .phone-number,
            .email,
            .site,
            .course {
                display: flex;
                i {
                    margin-top: .5rem;
                    color: lightgray;
                }
            }

            .address *,
            .phone-number *,
            .email *,
            .site *,
            .course * {
                margin-left: .5rem;
            }

            .course * {
                color: $brand_color !important;
            }
            .brand-info {
                .btn {
                    background-color: $brand_color;
                    color: $btn_text_color;
                    margin-top: 1rem;
                }
            }
        }
    }
</style>