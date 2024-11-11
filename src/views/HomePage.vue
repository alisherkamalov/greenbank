<template>
<div class="container">
    <div class="background">
        <section class="thebanner">
            <TheBanner />
        </section>
        <section class="theabout">
            <TheAbout />
        </section>
        <section class="thelogo">
            <TheLogo />
        </section>
        <section class="thefeatures">
            <TheFeatures />
        </section>
        <section class="thedesign">
            <TheDesign />
        </section>
        <section class="theperfect">
            <ThePerfect />
        </section>
        <section class="thefeedback">
            <TheFeedback />
        </section>
        <section class="thefaq">
            <TheFaq />
        </section>
        <footer>
            <TheFooter />
        </footer>
    </div>
</div>
</template>
<script setup>
import TheAbout from '@/components/TheAbout.vue';
import TheBanner from '@/components/TheBanner.vue';
import TheDesign from '@/components/TheDesign.vue';
import TheFaq from '@/components/TheFaq.vue';
import TheFeatures from '@/components/TheFeatures.vue';
import TheFeedback from '@/components/TheFeedback.vue';
import TheFooter from '@/components/TheFooter.vue';
import TheLogo from '@/components/TheLogo.vue';
import ThePerfect from '@/components/ThePerfect.vue';
</script>
<style scoped>
.thebanner {
    width: 100%;
    height: auto;
    display: flex;
    align-items: center;
    flex-direction: column;
}

.background {
    width: 100%;
    max-width: 1440px;
    height: 5076px;
    position: absolute;
    z-index: -1;
    display: flex;
    flex-direction: column;
    background-size: 100% 5076px;
    background-image: url(../assets/bg.svg);
    box-shadow: 0px 0px 150px rgba(0, 0, 0, 0.4) inset;
    filter: drop-shadow(0px 0px 56px rgba(26, 30, 28, 0.2));
}

.container {
    width: 100%;
    display: flex;
    justify-content: center;
    position: relative;
    top: -84px;
}
</style>