<template>
    <div class="bottom-header">
        <div class="d-flex-between boxed">
            <div class="logo-wrapper">
                <a href="#">
                    <img 
                    src="../../assets/img/avada-drivers-logo-1x.png"
                    alt="logo for Avada driving school"
                    >
                </a>
            </div>
                
            <nav class="nav-bar">
                <ul class="d-flex-end">
                    <li v-for="(link, index) in navLinks" :key="index"
                    :class="link.isActive? 'active' : '' "
                    >
                        <a :href="'#' + link.goTo"
                        :class="link.isNew? 'new' : '' ">
                            {{link.name.toUpperCase()}}
                        </a>
                    </li>

                    <li>
                        <a href="#" class="btn">BOOK NOW</a>
                    </li>
                </ul>
            </nav>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderBottom',
    data() {
        return {
            navLinks:   [
                            {
                                name: 'home',
                                isActive: true,
                                isNew: false,
                                goTo: 'jumbotron' 
                            },
                            {
                                name: 'about',
                                isActive: false,
                                isNew: false,
                                goTo: 'instructors'
                            },
                            {
                                name: 'prices',
                                isActive: false,
                                isNew: false,
                                goTo: 'news-letter'
                            },
                            {
                                name: 'courses',
                                isActive: false,
                                isNew: true,
                                goTo: 'courses'
                            },
                            {
                                name: 'location',
                                isActive: false,
                                isNew: false,
                                goTo: 'footer-top'
                            },
                            {
                                name: 'blog',
                                isActive: false,
                                isNew: false,
                                goTo: ''
                            },
                        ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../../styles/vars.scss';
    .bottom-header {
        background-color: rgba(0, 0, 0, 0.5);
        padding: 2rem 0;
        .logo-wrapper {
            a {
                img {
                    width: 100%;
                }
            }
        }

        .nav-bar {
            ul {
                list-style: none;
                gap: 4rem;
                li {
                    a {
                        color: #fff;
                        font-weight: bold;
                        cursor: pointer;
                        transition: color .3s linear;
                        text-decoration: none;
                        &:hover:not(.btn) {
                            color: #7F9EA8;
                        }
                        &.new::after {
                            content: 'New';
                            width: 60px;
                            padding: .3rem .5rem;
                            border-radius: .5rem;
                            background-color: $brand_color;
                        }
                    }
                }

                .btn {
                    background-color: $brand_color;
                    color: $btn_text_color;
                    transition: background-color .3s linear;
                    &:hover {
                        background-color: #48644B;
                    }
                }

                .active {
                    border-bottom: 3px solid $brand_color;
                    margin-top: 3px;
                }
            }
        }
    }
</style>