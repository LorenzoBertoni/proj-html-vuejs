<template>
    <section id="latest-news">
        <div class="card boxed">
            <h2 class="title">Latest News</h2>
            <div class="d-flex-center">
                <div 
                class="news"
                v-for="(news, index) in newsList"
                :key="index"
                >
                    <div class="img-wrapper">
                        <img :src="require('../assets/img/' + news.url)" :alt="news.title">
                    </div>
                    <h4>{{news.title}}</h4>
                    <p class="main-text">
                        <small>{{news.date}} <span>{{news.comments}} comments</span></small> 
                    </p>
                    <p class="main-text">
                        {{news.description}}
                    </p>
                </div>
            </div>
            <div class="d-flex-center">
                <a href="#" class="btn">MORE FROM THE BLOG</a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionLatestNews',
    data() {
        return {
            newsList:   [
                        {
                            url: 'blog-choosecar-320x202.jpg',
                            title: 'What Car to Start With?',
                            date: 'February 7th 2019',
                            comments: 0,
                            description: 'lorem ipsum sit dolor amet, consectetur adipiscing'
                        },
                        {
                            url: 'blogpost-10and2-320x202.jpg',
                            title: 'Avada Driving School Expanding',
                            date: 'February 7th 2019',
                            comments: 0,
                            description: 'lorem ipsum sit dolor amet, consectetur adipiscing'
                        },
                    ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';
    #latest-news {
        height: 600px;
        background-image: url('../assets/img/latestnews-background.jpg');
        background-position: center;
        background-size: cover;
        .card {
            border-top: 5px solid #7F9EA8;
            .title {
                margin-top: 3rem;
            }
        }
        .d-flex-center {
            gap: 6rem;
            margin-top: 2rem;

            h4 {
                margin: .5rem 0 .1rem 0;
                color: $brand_color;
            }

            span {
                color: $brand_color;
            }
        }
        .btn {
            background-color: $brand_color;
            color: $btn_text_color;
            margin-bottom: 1rem;
        }
    }
</style>