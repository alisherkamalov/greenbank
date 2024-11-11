<template>
    <div class="containerfoot">
        <div class="cta">
            <div class="leftcta">
                Easy Way to manage your finances
                <span class="title">Easy to use mobile app that support on android and ios.</span>
                <div class="buttons">
                    <button class="btn"><img src="../assets/as.svg" alt="" class="as-img"></button>
                    <button class="btn"><img src="../assets/gp.svg" alt="" class="gp-img"></button>
                </div>
            </div>
            <div class="rightphone">
                <img src="../assets/phone.svg" alt="" class="phone">
            </div>
        </div>
        <div class="footer">
            <div class="content">
                <div class="logotitle">
                    <div class="logo">
                        <div class="logoname">
                            <img src="../assets/logo.svg" alt="" class="logosvg">
                            GBank
                        </div>
                        
                        <span class="logotitle">Discover the power of our secure and rewarding credit cards</span>
                    </div>

                </div>
                <div class="bottomtext">
                    copyright 2023 DoraDesign All Rights Reserved
                    <span>This page uses cookies. See cookies details here</span>
                </div>
                
            </div>

        </div>
    </div>
</template>
<script setup>

</script>
<style scoped>
.containerfoot {
    width: 100%;
    min-height: 843px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-end;
}

.cta {
    max-width: 1240px;
    width: 90%;
    min-height: 472px;
    display: flex;
    align-items: center;
    margin-top: auto;
}

.logotitle {
    max-width: 392px;

}

.leftcta {
    max-width: 575px;
    width: 90%;
    min-height: 252.02px;
    font-weight: bold;
    font-size: 48px;
    text-align: left;
    line-height: 56px;
    letter-spacing: -0.48px;
    color: white;
    display: flex;
    gap: 15px;
    flex-direction: column;
    margin-bottom: 150px;
}

.title {
    font-size: 18px;
    line-height: 24px;
    font-weight: 400;
    letter-spacing: -3%;
    color: #ADB2B1;
}

.btn {
    border: 0;
    background-color: transparent;
    cursor: pointer;
    transition: all 0.3s ease;
}

.btn:active {
    scale: 0.9;
}

.buttons {
    display: flex;
    gap: 15px;
}

.footer {
    max-width: 1440px;
    width: 100%;
    background-color: rgba(40, 52, 48, 1);
    height: 371px;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1;
}

.phone {
    width: 536px;
}

.logo {
    font-size: 18px;
    line-height: 24px;
    font-weight: bold;
    color: white;
    display: flex;
    flex-direction: column;
    gap: 10px;
}
.logoname {
    display: flex;
    align-items: center;
    gap: 10px;
}
.logotitle {
    text-align: left;
    font-size: 16px;
    line-height: 24px;
    font-weight: 400;
    color: #ADB2B1;
    max-width: 287px;
}
.content {
    max-width: 1240px;
    width: 90%;
    min-height: 276px;
    position: relative
}
.bottomtext {
    position: absolute;
    font-size: 12px;
    line-height: 20px;
    font-weight: 400;
    width: 100%;
    display: flex;
    bottom: 0;
    justify-content: space-between;
    flex-wrap: wrap;
    color: #ADB2B1;
}
@media (max-width:1100px) {
    .rightphone {
        display: none
    }
}
</style>