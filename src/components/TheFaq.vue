<template>
    <div class="containerfaq">
        <div class="faqcont">
            FAQs
            <ul class="ulfaq">
                <li class="lifaq" v-for="(item, index) in faqItems" :key="index">
                    {{ item.question }}
                    <span class="plus" @click="toggleAnswer(index)">
                        {{ item.isOpen ? '-' : '+' }}
                    </span>
                    <div :style="getAnswerStyle(item)" class="answer">
                        {{ item.answer }}
                    </div>
                    <div class="line"></div>
                </li>
            </ul>
        </div>
    </div>
</template>

<script setup>
import { onMounted, ref } from 'vue';

const faqItems = ref([
    {
        question: 'What credit score do I need to apply for a credit card?',
        answer: 'The required credit score may vary depending on the specific credit card. Generally, a good to excellent credit score (typically 670 or above) increases your chances of approval for premium credit cards.',
        isOpen: false
    },
    {
        question: ' How can I apply for a credit card online?',
        answer: ' Applying for a credit card online is simple. Just visit our website, select the desired credit card, and click on the "Apply Now" button. Follow the instructions, provide your information, and submit your application securely.',
        isOpen: false
    },
    {
        question: 'What are the benefits of having a credit card?',
        answer: 'Credit cards offer rewards such as cash back, points, or travel miles. They also help build your credit history.',
        isOpen: false
    },
    {
        question: 'Are there any annual fees associated with the credit card?',
        answer: "Annual fees may apply to some credit cards, but not all. Our credit card details page will specify if there are any annual fees associated with the card you're interested in.",
        isOpen: false
    },
    {
        question: 'How long does it take to receive the credit card once approved?',
        answer: ' Once your credit card application is approved, it typically takes 7 to 10 business days to receive your physical card by mail. You can start using your virtual card immediately after approval for online purchases.',
        isOpen: false
    },
    {
        question: 'How can I check my credit card balance and transactions?',
        answer: 'You can easily check your credit card balance and transactions through our secure online banking portal or mobile app. Simply log in to your account to access your credit card information.',
        isOpen: false
    },
    {
        question: 'What should I do if my credit card is lost or stolen?',
        answer: 'If your credit card is lost or stolen, please notify us immediately through our customer support line or online banking. We will assist you in securing your account and issuing a replacement card.',
        isOpen: false
    },
    {
        question: 'Is my credit card information secure?',
        answer: 'Yes, we prioritize the security of your information. Our credit card systems use encryption and industry-standard security measures to protect your data, ensuring a safe and seamless experience.',
        isOpen: false
    }
]);

const toggleAnswer = (index) => {
    faqItems.value[index].isOpen = !faqItems.value[index].isOpen;
};

const getAnswerStyle = (item) => {
    return {
        maxHeight: item.isOpen ? '100px' : '0',
        overflow: 'hidden',
        transition: 'all 0.3s ease'
    };
};
onMounted(() => {
    const elements = document.querySelectorAll('.faqcont');

    
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
.containerfaq {
    width: 100%;
    display: flex;
    justify-content: center;
    margin-top: 110px;
}

.faqcont {
    max-width: 1020px;
    width: 90%;
    min-height: 666px;
    font-weight: bold;
    font-size: 40px;
    color: white;
    opacity: 0;
    scale: 0.8;
    transition: all 1s ease;
}
.faqcont.visible {
    opacity: 1;
    scale: 1;
}
.ulfaq {
    padding: 0;
    margin-top: 50px;
}

.lifaq {
    display: flex;
    flex-direction: column;
    font-size: 24px;
    font-weight: bold;
    line-height: 32px;
    margin-bottom: 20px;
    color: white;
    text-align: left;
    position: relative;
}

.answer {
    font-size: 16px;
    font-weight: normal;
    line-height: 24px;
    color: #dddddd;
    margin-top: 8px;
}

.plus {
    width: 10px;
    position: absolute;
    top: 0;
    right: 0;
    padding-left: 10px;
    cursor: pointer;
}

.line {
    width: 100%;
    height: 1px;
    background-color: rgb(173, 178, 177);
    margin-top: 15px;
}
</style>
