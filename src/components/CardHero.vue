<script setup>
</script>

<template>
    <div class="cardHero">
        <div class="top">
            <span class="subtitle">Manage cards</span>
            <button class="thirdBtn">Add new</button>
        </div>
        <img src="../assets/img/bank_card.png" alt="Bank card of John Snow">
        <!-- For the bank card I took a screenshot because I think it should be an asset (and also to save time to be honest) -->
        <div class="bill">
            <div class="topBill">
                <span class="subtitle">Starbucks</span>
                <span class="price">$5,50 USD</span>
            </div>
            <p>Pending - San Fransisco, United States</p>
        </div>
        <div class="bill">
            <div class="topBill">
                <span class="subtitle">Nike Sports</span>
                <span class="price">$129,00 USD</span>
            </div>
            <p>Pending - Lisbon, Portugal</p>
        </div>
        <a href="#">
            <span>View all</span>
            <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M10 7L15 12L10 17" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </a>
    </div>
</template>