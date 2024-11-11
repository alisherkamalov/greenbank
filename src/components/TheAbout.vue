<template>
    <div class="containerab">
        <div class="about">
            <ul class="ulabout">
                <li class="liabout">16y<span class="titleabout">Experience</span></li>
                <li class="liabout">250+<span class="titleabout">Merchant Partner</span></li>
                <li class="liabout">18+<span class="titleabout">Years Experience</span></li>
                <li class="liabout">10.2k+<span class="titleabout">Worldwide Clients</span></li>
            </ul>
        </div>
    </div>
</template>
<script setup>
import { onMounted } from 'vue';

onMounted(() => {
    // Выбираем элементы, которые хотим отслеживать
const elements = document.querySelectorAll('.about');

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
.containerab {
    width: 100%;
    display: flex;
    justify-content: center;
    margin-top: 100px;
}
.about {
    width: 80%;
    max-width: 1176px;
    padding: 64px 64px;
    background-color: rgba(61, 84, 77, 0.25);
    backdrop-filter: blur(16px);
    -webkit-backdrop-filter: blur(16px);
    border-radius: 32px;
    opacity: 0;
    scale: 0.8;
    transition: all 1s ease;
}
.about.visible {
    opacity: 1;
    scale: 1;
}
.ulabout {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
}
.liabout {
    width: 278px;
    height: 88px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 10px;
    font-family: 'M PLUS 1';
    font-weight: bold;
    font-size: 48px;
    line-height: 56px;
    letter-spacing: -0.32px;
    color: white;
}
.titleabout {
    font-family: 'M PLUS 1';
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    letter-spacing: 0%;
    color: #2BB32A;
}
@media(max-width:800px) {
    .about {
        width: 60%;
    }
}
</style>