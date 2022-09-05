<template>
    <div class="courses-percentages d-flex boxed">
            <div class="card d-flex-column-center">
                <div class="circle-wrap">
                    <div class="circle">
                        <div class="mask half">
                            <div class="fill"></div>
                        </div>
                        <div class="mask full">
                            <div class="fill"></div>
                        </div>
                        <div class="inside-circle"> 95% </div>
                    </div>
                </div>
                <p>Pass Rate</p>
            </div>

            <div class="card d-flex-column-center">
                <div class="circle-wrap">
                    <div class="circle">
                        <div class="mask half">
                            <div class="fill"></div>
                        </div>
                        <div class="mask full">
                            <div class="fill"></div>
                        </div>
                        <div class="inside-circle"> 95% </div>
                    </div>
                </div>
                <p>Pass Rate</p>
            </div>

            <div class="card d-flex-column-center">
                <div class="circle-wrap">
                    <div class="circle">
                        <div class="mask half">
                            <div class="fill"></div>
                        </div>
                        <div class="mask full">
                            <div class="fill"></div>
                        </div>
                        <div class="inside-circle"> 95% </div>
                    </div>
                </div>
                <p>Pass Rate</p>
            </div>
        </div>
</template>

<script>
export default {
    name: 'CoursesPercentages',
    props: {
        percentage: Number
    }
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';

    .courses-percentages {
        gap: .5rem;
        .card {
            border-top: 4px solid $brand_color;

            .circle-wrap {
                margin: 3rem auto;
                width: 150px;
                height: 150px;
                background: #fefcff;
                border-radius: 50%;
                border: 1px solid #cdcbd0;

                .circle {
                    .mask {
                        clip: rect(0px, 150px, 150px, 75px);
                    }
                    .mask, .fill {
                        width: 150px;
                        height: 150px;
                        position: absolute;
                        border-radius: 50%;
                    }
                }

                .inside-circle {
                    width: 122px;
                    height: 122px;
                    border-radius: 50%;
                    background-color: #fff;
                    line-height: 120px;
                    text-align: center;
                    margin-top: 14px;
                    margin-left: 14px;
                    color: $text_color;
                    position: absolute;
                    z-index: 100;
                    font-weight: 500;
                    font-size: 2rem;
                }
            }

            .mask .fill {
                clip: rect(0px, 75px, 150px, 0px);
                background-color: $brand_color;
            }

            .mask.full,
            .circle .fill {
                animation: fill ease-in-out 3s;
                transform: rotate(171deg);
            }

            @keyframes fill{
                0% {
                    transform: rotate(0deg);
                }
                100% {
                    transform: rotate(171deg);
                }
            }
        }
    }
</style>