<template>
    <div class="containerf">
        <div class="feedbackcont">
            <ul class="ulfeed">
                <li class="lifeed">
                    <img src="../assets/feednum.svg" alt="" class="feednum">
                    "Great session! Dani was super helpful. She shared some practical advice on how can lorem ip we go
                    about refining our service offerings."
                    <div class="user">
                        <img src="../assets/user1.svg" alt="" class="image-user">
                        <div class="info">
                            Hadid Khan
                            <span class="title">
                                UIUX Designer
                            </span>
                        </div>
                    </div>
                </li>
                <li class="lifeed">
                    <img src="../assets/feednum.svg" alt="" class="feednum">
                    "It's is both attractive and highly adaptable. It's exactly what I've been looking forefinitely wo
                    lorem ipsum dolorth the investment."
                    <div class="user">
                        <img src="../assets/user2.svg" alt="" class="image-user">
                        <div class="info">
                            Wade Warren
                            <span class="title">
                                Web Designer
                            </span>
                        </div>
                    </div>
                </li>
                <li class="lifeed">
                    <img src="../assets/feednum.svg" alt="" class="feednum">
                    "I am really satisfied with it. I'm good to go. It really saves me time and effort. It's is exactly
                    what our business has been lacking. "
                    <div class="user">
                        <img src="../assets/user3.svg" alt="" class="image-user">
                        <div class="info">
                            Jenny Wilson
                            <span class="title">
                                Trust Administrator
                            </span>
                        </div>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>
<script setup>
import { onMounted } from 'vue';

onMounted(() => {
const elements = document.querySelectorAll('.ulfeed');


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
})
</script>
<style scoped>
.containerf {
    width: 100%;
    display: flex;
    justify-content: center;
    margin-top: 220px;
}

.feedbackcont {
    width: 80%;
    max-width: 1240px;
}

.ulfeed {
    display: flex;
    gap: 32px;
    align-items: center;
    justify-content: center;
}

.lifeed {
    max-width: 344px;
    width: 90%;
    min-height: 264px;
    padding: 48px 24px;
    display: flex;
    gap: 32px;
    background-color: rgba(39, 50, 47, 0.24);
    border-radius: 32px;
    backdrop-filter: blur(16px);
    font-size: 15px;
    line-height: 24px;
    color: white;
    flex-direction: column;
    text-align: left;
    font-weight: 400;
    opacity: 0;
    scale: 0.8;
    transition: all 1s ease;
}
.ulfeed.visible > .lifeed {
    opacity: 1;
    scale: 1;
}
.feednum {
    width: 56px;
}

.image-user {
    width: 48px;
}

.user {
    display: flex;
    width: 90%;
    gap: 10px;
}

.info {
    font-size: 16px;
    line-height: 24px;
    color: white;
    font-weight: 400;
    display: flex;
    flex-direction: column;
}

.title {
    color: #ADB2B1;
    font-size: 12px;
    line-height: 20px;
    font-weight: 400;
}
@media (max-width:1100px) {
    .ulfeed {
        flex-wrap: wrap;
    }
}
</style>