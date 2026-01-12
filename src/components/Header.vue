<script setup>
import { ref } from 'vue';

const isOpen = ref(false);
</script>

<template>
    <header>
        <nav class="desktopNav">
            <a href="#">
                <img src="../assets/logos/odoo-white.svg" class="logoOdoo" alt="Logo de Odoo">
            </a>
            <button class="burgerBtn" type="button" aria-label="Open menu" @click="isOpen = !isOpen">
                <span></span>
                <span></span>
                <span></span>
            </button>
            <div class="links">
                <a href="#">Home</a>
                <a href="#">Products</a>
                <a href="#">Pages</a>
                <a href="#">App</a>
                <a href="#">Docs</a>
            </div>
            <div class="buttons">
                <button class="secondaryBtn">
                    <span>Sign in</span>
                </button>
                <button class="primaryBtn">
                    <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M5 7H19V19C19 20.1046 18.1046 21 17 21H7C5.89543 21 5 20.1046 5 19V7Z" stroke="#FFFFFF" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/><path d="M17.5 4H6.5L5 7H19L17.5 4Z" stroke="#FFFFFF" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/><path d="M15 11L14.2 13L9.8 13L9 11" stroke="#FFFFFF" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
                    <span>Buy now</span>
                </button>
            </div>
        </nav>
        <div class="mobileMenu" v-show="isOpen">
            <div class="mobileLinks">
                <a href="#">Home</a>
                <a href="#">Products</a>
                <a href="#">Pages</a>
                <a href="#">App</a>
                <a href="#">Docs</a>
            </div>
            <div class="mobileButtons">
                <button class="secondaryBtn">
                    <span>Sign in</span>
                </button>
                <button class="primaryBtn">
                    <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M5 7H19V19C19 20.1046 18.1046 21 17 21H7C5.89543 21 5 20.1046 5 19V7Z" stroke="#FFFFFF" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/><path d="M17.5 4H6.5L5 7H19L17.5 4Z" stroke="#FFFFFF" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/><path d="M15 11L14.2 13L9.8 13L9 11" stroke="#FFFFFF" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
                    <span>Buy now</span>
                </button>
            </div>
        </div>
    </header>
</template>
