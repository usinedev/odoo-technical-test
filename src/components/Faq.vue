<script setup>
import { ref } from 'vue';

const faqs = [
    {
        question: 'Which license do I need?',
        answer: 'Use the standard commercial license for production. The free license is fine for personal tests and demos.',
        icon: `<svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" clip-rule="evenodd" d="M6 1C4.34314 1 3 2.34315 3 4V20C3 21.6569 4.34315 23 6 23H19C20.6569 23 22 21.6569 22 20V10C22 9.73478 21.8946 9.48043 21.7071 9.29289L13.7071 1.29292C13.6114 1.19722 13.4983 1.1229 13.3753 1.07308C13.2572 1.02527 13.1299 1 13 1H6ZM12 3H6C5.44771 3 5 3.44771 5 4V20C5 20.5523 5.44772 21 6 21H19C19.5523 21 20 20.5523 20 20V11H13C12.4477 11 12 10.5523 12 10V3ZM18.5858 9.00003L14 4.41424V9.00003H18.5858Z"/></svg>`
    },
    {
        question: 'How do I get access to my database?',
        answer: 'Open Settings > Database, then click “Connect.” Your credentials are listed in the project dashboard.',
        icon: `<svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M17 10.25H8.75V8C8.75 7.13805 9.09241 6.3114 9.7019 5.7019C10.3114 5.09241 11.138 4.75 12 4.75C12.862 4.75 13.6886 5.09241 14.2981 5.7019C14.9076 6.3114 15.25 7.13805 15.25 8C15.25 8.19891 15.329 8.38968 15.4697 8.53033C15.6103 8.67098 15.8011 8.75 16 8.75C16.1989 8.75 16.3897 8.67098 16.5303 8.53033C16.671 8.38968 16.75 8.19891 16.75 8C16.75 6.74022 16.2496 5.53204 15.3588 4.64124C14.468 3.75045 13.2598 3.25 12 3.25C10.7402 3.25 9.53204 3.75045 8.64124 4.64124C7.75045 5.53204 7.25 6.74022 7.25 8V10.25H7C6.27065 10.25 5.57118 10.5397 5.05546 11.0555C4.53973 11.5712 4.25 12.2707 4.25 13V18C4.25 18.7293 4.53973 19.4288 5.05546 19.9445C5.57118 20.4603 6.27065 20.75 7 20.75H17C17.7293 20.75 18.4288 20.4603 18.9445 19.9445C19.4603 19.4288 19.75 18.7293 19.75 18V13C19.75 12.2707 19.4603 11.5712 18.9445 11.0555C18.4288 10.5397 17.7293 10.25 17 10.25ZM18.25 18C18.25 18.3315 18.1183 18.6495 17.8839 18.8839C17.6495 19.1183 17.3315 19.25 17 19.25H7C6.66848 19.25 6.35054 19.1183 6.11612 18.8839C5.8817 18.6495 5.75 18.3315 5.75 18V13C5.75 12.6685 5.8817 12.3505 6.11612 12.1161C6.35054 11.8817 6.66848 11.75 7 11.75H17C17.3315 11.75 17.6495 11.8817 17.8839 12.1161C18.1183 12.3505 18.25 12.6685 18.25 13V18Z"/></svg>`
    },
    {
        question: 'How do I see previous orders?',
        answer: 'Go to Orders > History. You can filter by date, status, or customer in one click.',
        icon: `<svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" clip-rule="evenodd" d="M1 4C1 2.34315 2.34315 1 4 1H7.76393C8.90025 1 9.93904 1.64201 10.4472 2.65836L11.3416 4.44721C11.511 4.786 11.8573 5 12.2361 5H20C21.6569 5 23 6.34315 23 8V20C23 21.6569 21.6569 23 20 23H4C2.34315 23 1 21.6569 1 20V4ZM4 3C3.44772 3 3 3.44772 3 4V20C3 20.5523 3.44772 21 4 21H20C20.5523 21 21 20.5523 21 20V8C21 7.44772 20.5523 7 20 7H12.2361C11.0998 7 10.061 6.35799 9.55279 5.34164L8.65836 3.55279C8.48897 3.214 8.1427 3 7.76393 3H4Z"/></svg>`
    }
];

const openIndex = ref(null);

const toggle = (index) => {
    openIndex.value = openIndex.value === index ? null : index;
};
</script>

<template>
    <section class="faqSection">
        <div class="faqTop">
            <p class="title">Helpful answers</p>
            <p>Start building fast, beautiful and modern looking websites in no time.</p>
        </div>
        <div class="questions">
            <div class="questionsContainer questionsLeft">
                <div v-for="(item, index) in faqs" :key="`left-${index}`" class="qaItem">
                    <button class="question" type="button" @click="toggle(index)" :aria-expanded="openIndex === index">
                        <div class="questionAndIcon">
                            <span v-html="item.icon"></span>
                            <span>{{ item.question }}</span>
                        </div>
                        <span class="seeMore">{{ openIndex === index ? '-' : '+' }}</span>
                        <p v-show="openIndex === index" class="answer">{{ item.answer }}</p>
                    </button>
                </div>
            </div>
            <div class="questionsContainer questionsRight">
                <div v-for="(item, index) in faqs" :key="`right-${index}`" class="qaItem">
                    <button class="question" type="button" @click="toggle(index + faqs.length)" :aria-expanded="openIndex === index + faqs.length">
                        <div class="questionAndIcon">
                            <span v-html="item.icon"></span>
                            <span>{{ item.question }}</span>
                        </div>
                        <span class="seeMore">{{ openIndex === index + faqs.length ? '-' : '+' }}</span>
                        <p v-show="openIndex === index + faqs.length" class="answer">{{ item.answer }}</p>
                    </button>
                </div>
            </div>
        </div>
    </section>
</template>
