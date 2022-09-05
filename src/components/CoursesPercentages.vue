<template>
    <div class="courses-percentages d-flex boxed">
            <div class="card d-flex-column-center">
                <div class="circle-wrap">
                    <div class="circle">
                        <div class="mask half">
                            <div class="fill"></div>
                        </div>
                        <div class="mask close-to-full">
                            <div class="fill"></div>
                        </div>
                        <div class="inside-circle"> 95% </div>
                    </div>
                </div>
                <p>PASS RATE</p>
            </div>

            <div class="card d-flex-column-center">
                <div class="circle-wrap">
                    <div class="circle">
                        <div class="mask half">
                            <div class="fill-two"></div>
                        </div>
                        <div class="mask full">
                            <div class="fill-two"></div>
                        </div>
                        <div class="inside-circle"> 100% </div>
                    </div>
                </div>
                <p>REFERRAL RATE</p>
            </div>

            <div class="card d-flex-column-center">
                <div class="circle-wrap">
                    <div class="circle">
                        <div class="mask half">
                            <div class="no-fill"></div>
                        </div>
                        <div class="mask empty">
                            <div class="no-fill"></div>
                        </div>
                        <div class="inside-circle"> 0% </div>
                    </div>
                </div>
                <p>ACCIDENT RATE</p>
            </div>
        </div>
</template>

<script>
export default {
    name: 'CoursesPercentages'
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';

    .courses-percentages {
        gap: .8rem;
        p {
            margin-bottom: 4rem;
            color: $text_color;
            font-weight: 700;
        }
        .card {
            border-top: 5px solid $brand_color;
            transform: translateY(-8rem);
            //***regole generali per gli spin
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
                    .mask, .fill,
                    .fill-two,
                    .no-fill {
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

            .mask .fill,
            .mask .fill-two,
            .mask .no-fill {
                clip: rect(0px, 75px, 150px, 0px);
                background-color: $brand_color;
            }

            //***animazioni uniche per spin
            //*95%
            .mask.close-to-full,
            .circle .fill{
                animation: spin ease-in-out 3s;
                transform: rotate(171deg);
            }

            @keyframes spin {
                0% {
                    transform: rotate(0deg);
                }
                100% {
                    transform: rotate(171deg);
                }
            }
            //*100%
            .mask.full,
            .circle .fill-two {
                animation: fullSpin ease-in-out 3s;
                transform: rotate(180deg);
            }

            @keyframes fullSpin {
                0% {
                    transform: rotate(0deg);
                }
                100% {
                    transform: rotate(180deg);
                }
            }

            //*0%
            .mask.empty,
            .circle .no-fill {
                animation: noSpin ease-in-out 3s;
                transform: rotate(2deg);
            }
        }
    }
</style>