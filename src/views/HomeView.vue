<script setup>
import Cta from '@/components/Cta.vue';
import Faq from '@/components/Faq.vue';
import FeatureSection from '@/components/FeatureSection.vue';
import Footer from '@/components/Footer.vue';
import Header from '@/components/Header.vue';
import Hero from '@/components/Hero.vue';
import Ratings from '@/components/Ratings.vue';
</script>

<template>
    <Header />
    <Hero />
    <FeatureSection />
    <Cta />
    <Ratings />
    <Faq />
    <Footer />
</template>

<style scoped lang="scss">
@use '../assets/style/main.scss' as *;
</style>