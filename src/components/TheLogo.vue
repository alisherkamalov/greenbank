<template>
    <div class="containerl">
        <div class="hidden">
            <div class="slider" ref="slider">
                <img src="../assets/upwork.svg" alt="" class="logo">
                <img src="../assets/petal.svg" alt="" class="logo">
                <img src="../assets/rakuten.svg" alt="" class="logo">
                <img src="../assets/nyt.svg" alt="" class="logo">
                <img src="../assets/vice.svg" alt="" class="logo">
                <img src="../assets/dell.svg" alt="" class="logo">

                <img src="../assets/upwork.svg" alt="" class="logo">
                <img src="../assets/petal.svg" alt="" class="logo">
                <img src="../assets/rakuten.svg" alt="" class="logo">
                <img src="../assets/nyt.svg" alt="" class="logo">
                <img src="../assets/vice.svg" alt="" class="logo">
                <img src="../assets/dell.svg" alt="" class="logo">
            </div>
        </div>

    </div>
</template>

<script setup>
import { onMounted, ref } from 'vue';

const slider = ref(null);

onMounted(() => {
    const sliderEl = slider.value;
    const slideSpeed = 1; 
    let scrollAmount = 0;
    const totalScrollWidth = sliderEl.scrollWidth / 2; 

    const animateSlider = () => {
        scrollAmount -= slideSpeed;
        sliderEl.style.transform = `translateX(${scrollAmount}px)`;

        
        if (Math.abs(scrollAmount) >= totalScrollWidth) {
            scrollAmount = 0;
        }

        requestAnimationFrame(animateSlider);
    };

    animateSlider();
    
    const elements = document.querySelectorAll('.slider');
    const observer = new IntersectionObserver((entries, observer) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add('visible');
                
                observer.unobserve(entry.target);
                }
            });
    }, {
        root: null,        
        rootMargin: '0px',  
        threshold: 0.1      
    });

    
    elements.forEach(element => observer.observe(element));

});
</script>

<style scoped>
.containerl {
    width: 100%;
    overflow: hidden;
    display: flex;
    justify-content: center;
    margin-top: 100px;
}

.slider {
    display: flex;
    align-items: center;
    gap: 105px;
    /* Начальная позиция */
    transform: translateX(0);
    opacity: 0;
    scale: 0.8;
    transition: all 1s ease;
}
.slider.visible {
    opacity: 1;
    scale: 1;
}
.hidden {
    overflow: hidden;
    max-width: 1240px;
}
.logo {
    height: 32px;
}
</style>
