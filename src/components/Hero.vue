<script setup>
import CardHero from './CardHero.vue';
import Header from './Header.vue';


</script>

<template>
    <section class="hero">
        <Header />
        <div class="heroContainer">
            <div class="left">
                <h1>Development done right</h1>
                <p>Build a beautiful, modern website with flexible components built from scratch.</p>
                <button class="bigCta">
                    <span>Get started</span>
                    <span class="icon">+</span>
                </button>
                <div class="trustedBy">
                    <span>Trusted by:</span>
                    <img src="../assets/logos/google-white.svg" alt="">
                    <img src="../assets/logos/spotify-white.svg" alt="">
                    <img src="../assets/logos/airbnb-white.svg" alt="">
                    <img src="../assets/logos/paypal-white.svg" alt="">
                </div>
            </div>
            <div class="right">
                <CardHero />
            </div>
        </div>
    </section>
</template>