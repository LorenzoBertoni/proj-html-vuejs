<template>
    <section id="cta">
        <div class="d-flex-around boxed">
            <div class="left-side">
                <h3>Start Learning to Drive Today</h3>
                <h4>Give us a call to schedule your first driving lesson</h4>
            </div>

            <div class="right-side">
                <p> 
                    <i class="fa-solid fa-phone"></i> 1-800-555-555
                </p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionCta'
}
</script>

<style scoped lang="scss">
    #cta {
        background-color: lightblue;
        background-image: url('../../assets/img/horizontal-cta-background.jpg');
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
</style>