<template>
    <div class="containerd">
        <div class="leftdesign">
            Design your personalized credit card.
            <span class="titledesign">You have the freedom to personalize the design of your credit card, ensuring a
                truly unique experience that makes you feel extraordinary</span>
                <button class="createcard">Create New Card <img src="../assets/go.svg" alt="" class="go"></button>
        </div>
        <div class="rightdesign">
            <img src="../assets/star.svg" alt="" class="star">
            <img src="../assets/card.svg" alt="" class="card">
            <img src="../assets/card2.svg" alt="" class="cardt">
            <img src="../assets/card3.svg" alt="" class="cardth">
        </div>
    </div>
</template>
<script setup>
import { onMounted } from 'vue';

onMounted(() => {
const elements = document.querySelectorAll('.containerd');


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
const cards = document.querySelectorAll('.rightdesign');


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
.containerd {
    width: 100%;
    display: flex;
    justify-content: center;
    margin-top: 126px;
    min-height: 519.39px;
    opacity: 0;
    scale: 0.8;
    transition: all 1s ease;
}
.containerd.visible {
    opacity: 1;
    scale: 1;
}
.rightdesign.visible > .card {
    translate: 0px 0px;
    opacity: 1;
}
.rightdesign.visible > .cardt {
    translate: 0px 0px;
    opacity: 1;
}
.rightdesign.visible > .cardth {
    translate: 0px 0px;
    opacity: 1;
}
.leftdesign {
    font-weight: bold;
    font-size: 40px;
    color: white;
    display: flex;
    flex-direction: column;
    text-align: left;
    max-width: 604px;
    justify-content: center;
    padding-left: 70px;
    width: 100%;
    gap: 20px;

}
.titledesign {
    color: #ADB2B1;
    font-weight: 400;
    font-size: 16px;
    max-width: 424px;
    width: 100%;
}
.createcard {
    padding: 16px 32px;
    max-width: 233.5px;
    background-color: #2BB32A;
    border: 0;
    border-radius: 64px;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    color: white;
    cursor: pointer;
    transition: all 0.3s ease;
}
.createcard:active {
    scale: 0.9;
}
.go {
    margin-left: 10px;
    position: relative;
    top: 4px;
}
.rightdesign {
    max-width: 695px;
    width: 90%;
    display: flex;
    position: relative;
    height: 519.39px;
    flex-direction: column;
}
.star {
    width: 279.49px;
    left: 0;
    bottom: 60px;
    position: absolute;
}
.card {
    width: 505.05px;
    position: absolute;
    top: 0;
    right: 60px;
    z-index: 3;
    translate: 0px 300px;
    transition: all 1.2s ease;
}
.cardt {
    width: 505.05px;
    position: absolute;
    top: 100px;
    right: 60px;
    z-index: 2;
    translate: 0px 300px;
    transition: all 1.5s ease;
}
.cardth {
    width: 505.05px;
    position: absolute;
    top: 220px;
    right: 60px;
    z-index: 1;
    translate: 0px 300px;
    transition: all 2s ease;
}
@media(max-width:1100px) {
    .containerd {
        flex-wrap: wrap;
        flex-direction: column-reverse;
        align-items: center;
    }
}
@media(max-width:900px) {
    .rightdesign {
        scale: 0.7;
    }
    .leftdesign {
        width: 80%;
        padding-left: 0;
    }
    .card {
        right: -80px;
    }
    .cardt {
        right: -80px;
    }
    .cardth {
        right: -80px;
    }
    .containerd {
        margin-top: 0;
    }
}
</style>