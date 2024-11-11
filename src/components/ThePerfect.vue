<template>
    <div class="containerp">

        <div class="leftperfect">
            <img src="../assets/card5.svg" alt="" class="cardone">
            <img src="../assets/card4.svg" alt="" class="cardtwo">
            <img src="../assets/star2.svg" alt="" class="star">
        </div>
        <div class="rightperfect">
            Find the Perfect Credit Card for You
            <span class="title">Discover your ideal credit card with ease. Our comprehensive selection caters to every
                financial need and lifestyle. Whether you seek cashback rewards, travel perks, or building credit, we
                have the perfect credit card waiting for you. Unleash the possibilities and find the credit card that
                fits your unique goals and aspirations.
            </span>
            <button class="learnmore">Learn More</button>
        </div>

    </div>
</template>
<script setup>
import { onMounted } from 'vue';

onMounted(() => {
const elements = document.querySelectorAll('.rightperfect');


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
const cards = document.querySelectorAll('.leftperfect');


const observertwo = new IntersectionObserver((entries, observertwo) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');
      
      observertwo.unobserve(entry.target);
    }
  });
}, {
  root: null,         
  rootMargin: '0px',  
  threshold: 0.1      
});


cards.forEach(element => observertwo.observe(element));
})
</script>
<style scoped>
.containerp {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 100px;
}

.leftperfect {
    width: 90%;
    max-width: 604px;
    min-height: 490.86px;
    position: relative;
    perspective: 1000px;
}

.cardone {
    position: absolute;
    top: 0;
    left: 20px;
    z-index: 2;
    scale: 0.8;
    transform-style: preserve-3d;
    transform: rotateY(25deg);
    transition: all 1.2s ease;
}
.leftperfect.visible > .cardone {
    transform: rotateY(0deg);
    scale: 1;
}
.leftperfect.visible > .cardtwo {
    transform: rotateY(0deg);
    scale: 1;
}
.cardtwo {
    position: absolute;
    top: 155px;
    left: 0;
    z-index: 1;
    transform-style: preserve-3d;
    transform: rotateY(25deg);
    scale: 0.8;
    transition: all 1.5s ease;
}

.star {
    position: absolute;
    right: 25px;
    bottom: 15px;
    z-index: 0;
}

.rightperfect {
    width: 90%;
    max-width: 604px;
    min-height: 340px;
    font-weight: bold;
    font-size: 40px;
    text-align: left;
    color: white;
    flex-direction: column;
    display: flex;
    gap: 15px;
    transition: all 1s ease;
    opacity: 0;
    scale: 0.8;
}
.rightperfect.visible {
    opacity: 1;
    scale: 1;
}
.title {
    font-weight: 400;
    font-size: 16px;
    color: #ADB2B1;
    
    line-height: 24px;
    max-width: 532px;
    width: 90%;
}
.learnmore {
    font-weight: 400;
    font-size: 16px;
    color: white;
    line-height: 24px;
    border: 0;
    border-radius: 64px;
    background-color: #2BB32A;
    padding: 16px 32px;
    max-width: 152px;
    cursor: pointer;
    transition: all 0.3s ease;
}
.learnmore:active {
    scale: 0.9;
}
@media (max-width:1100px) {
    .containerp {
        flex-wrap: wrap;
    }
}
@media(max-width:500px) {
    .leftperfect {
        scale: 0.7;
        position: relative;
        left: -30px;
    }
    .containerp {
        margin-top: 0;
    }
}
</style>