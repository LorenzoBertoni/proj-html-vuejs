<template>
    <section id="lessons">
            <div class="d-flex boxed">
                <div class="lessons-info d-flex-column">
                    <h2>Get Behind The Wheel</h2>

                    <p class="main-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti ex officia labore quis. Incidunt eius recusandae impedit aperiam voluptate eligendi.</p>

                    <p class="main-text">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Fugit officiis ipsam dignissimos dolor modi sapiente impedit laborum in! Numquam porro, obcaecati velit odit sint vitae voluptate iusto veritatis labore odio quos mollitia est, dignissimos architecto facilis, cupiditate saepe sit! Ratione?</p>
                </div>
                
                <div class="form-wrapper">
                    <div class="card">
                        <div class="form-info boxed">
                            <h3>First Lesson Free!</h3>
                            <p class="main-text">When you make a block booking with us your first lesson is included free.</p>
                        </div>

                        <form action="" class="boxed" method="get">
                            <input type="text" placeholder="Your Name*" minlength="2" required
                            class="input-style"
                            >
                            <input type="email" placeholder="Email*" required
                            class="input-style"
                            >
                            <input type="text" placeholder="Telephone" 
                            class="input-style"
                            >
                            <input type="text" placeholder="Location" 
                            class="input-style"
                            >
                            <button class="btn">REQUEST A CALLBACK</button>
                        </form>
                    </div>
                </div>
            </div>
        </section>
</template>

<script>
export default {
    name: 'SectionLessons'
}
</script>

<style scoped lang="scss">
    @import '../styles/vars.scss';
    #lessons {
        .lessons-info, .form-wrapper {
            width: 50%;
        }

        .lessons-info {
            h2 {
                color: $title_color;
                font-size: 2rem;
                margin-bottom: 2rem;
            }

            p {
                margin: 1rem 0;
                font-size: 1.2rem;
                line-height: 2.5rem;
            }
        }

        .form-wrapper {
            .card {
                padding: 2rem 0;
                .form-info {
                    h3 {
                        margin-bottom: 2rem;
                        color: $brand_color;
                    }
                    p {
                        line-height: 1.5rem;
                        margin-bottom: 1rem;
                    }
                }
                form * {
                    margin: .8rem 0;
                }

                .btn {
                    background-color: $brand_color;
                    color: $btn_text_color;
                }
            }
        }
    }
</style>