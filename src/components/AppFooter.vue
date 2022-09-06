<template>
    <footer>
        <FooterTop/>
        <FooterBottom/>
    </footer>
</template>

<script>
import FooterTop from './sections/FooterTop.vue';
import FooterBottom from './sections/FooterBottom.vue';

export default {
    name: 'AppFooter',
    components: {
        FooterTop,
        FooterBottom
    }
}
</script>

<style>
    
</style>