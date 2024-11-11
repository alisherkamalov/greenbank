<template>
    <div class="containerf">
        <div class="features">
            <span class="titlefeat">What do we offer?</span>
            <div class="sizedbox"></div>
            <ul class="ulfeat">
                <li class="lifeat">
                    <img src="../assets/sec.svg" alt="" class="icon">
                    <div class="infofeat">
                        Security Guarantee 
                        <span class="featdesc">Your data and funds will be securely protected.</span>
                    </div>
                </li>
                <li class="lifeat">
                    <img src="../assets/inv.svg" alt="" class="icon">
                    <div class="infofeat">
                        Investing
                        <span class="featdesc">Your data and funds will be securely protected.</span>
                    </div>
                </li>
                <li class="lifeat">
                    <img src="../assets/met.svg" alt="" class="icon">
                    <div class="infofeat">
                        Multiple Method
                        <span class="featdesc">Your data and funds will be securely protected.</span>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>
<script setup>
import { onMounted } from 'vue';

onMounted(() => {
    // Выбираем элементы, которые хотим отслеживать
const elements = document.querySelectorAll('.features');

// Создаем новый наблюдатель
const observer = new IntersectionObserver((entries, observer) => {
  entries.forEach(entry => {
    // Проверяем, пересекается ли элемент с областью видимости
    if (entry.isIntersecting) {
      // Добавляем класс, если элемент видим
      entry.target.classList.add('visible');
      // Если больше не нужно отслеживать этот элемент, отменяем наблюдение
      observer.unobserve(entry.target);
    }
  });
}, {
  root: null,         // область просмотра по умолчанию — весь видимый экран
  rootMargin: '0px',  // отступы вокруг области просмотра
  threshold: 0.1      // процент видимости элемента (10%)
});

// Подключаем наблюдатель к каждому элементу
elements.forEach(element => observer.observe(element));

})
</script>
<style scoped>
.containerf {
    width: 100%;
    display: flex;
    justify-content: center;
    margin-top: 147px;
}
.features {
    width: 90%;
    max-width: 1240px;
    display: flex;
    flex-direction: column;
    align-items: center;
    opacity: 0;
    scale: 0.8;
    transition: all 1s ease;
}
.features.visible {
    scale: 1;
    opacity: 1;
}
.ulfeat {
    width: 100%;
    display: flex;
    gap: 20px;
}
.lifeat {
    display: flex;
    gap: 15px;
    align-items:start;
}
.icon {
    width: 64px;
}
.infofeat {
    display: flex;
    flex-direction: column;
    font-weight: 400;
    font-size: 24px;
    gap: 10px;
    text-align: left;
    color: white;
}
.featdesc {
    font-weight: 400;
    font-size: 24px;
    color: #ADB2B1;
}
.titlefeat {
    font-weight: bold;
    font-size: 40px;
    color: white;

}
.sizedbox {
    height: 64px;
}
@media(max-width:900px) {
    .ulfeat {
        flex-wrap: wrap;
    }
}
</style>