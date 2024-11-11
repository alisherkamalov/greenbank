<template>
    <div class="containerb">
        <div class="frame-one">
            <span class="title">
                Discover the Perfect Credit Card for You
                <img src="../assets/line.svg" alt="line" class="line">
            </span>
            <span class="desc">
                Discover the power of our secure and rewarding credit cards. Explore our range of credit cards and take
                control of your finances today.
            </span>
            <button class="btn-start">Get Started <img src="../assets/go.svg" alt="" class="go"></button>
            <div class="active">
                <img src="../assets/users.svg" alt="avatar users" class="users">
                <div class="active-info">
                    10.2k+
                    <span class="title-active">
                        Active users around the wordls
                    </span>
                </div>
            </div>
        </div>
        <div class="frame-two">
            <div class="card">
                <div class="card-info">
                    <img src="../assets/cardlogot.svg" alt="logo card two" class="cardlogo-two">
                    <img src="../assets/wifi.svg" alt="" class="wifi">
                    <img src="../assets/cardlogo.svg" alt="logo card" class="cardlogo-one">
                    <span class="title-num">Credit Card No.</span>
                    <span class="card-num">1602 0911 2019 2024</span>
                    <div class="name-exp">
                        <div class="name">
                            Name
                            <span class="user-name">DWAYNE JOHNSON</span>
                        </div>
                        <div class="exp">
                            Exp.
                            <span class="date">15/01</span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="circle"></div>
        </div>
    </div>
</template>
<script setup>

</script>
<style scoped>
@keyframes animatecircle {
    from {
        opacity: 0;
        scale: 0.9;
    }

    to {
        opacity: 1;
        scale: 1;
    }
}

@keyframes animateactive {
    from {
        opacity: 0;
        translate: -125px 0px;
    }

    to {
        opacity: 1;
        translate: 0px 0px;
    }
}

@keyframes animatebtn {
    from {
        opacity: 0;
        translate: 0px -50px;
        scale: 0.9;
    }

    to {
        opacity: 1;
        translate: 0px 0px;
        scale: 1;
    }
}

@keyframes animatetext {
    from {
        opacity: 0;
        translate: 0px -100px;
        scale: 0.9;
    }

    to {
        opacity: 1;
        translate: 0px 0px;
        scale: 1;
    }
}

@keyframes animatecard {
    from {
        opacity: 0;
        translate: 1250px 0px;
        rotate: 150deg;
    }

    to {
        opacity: 1;
        translate: 0px 0px;
        rotate: 15deg;
    }
}

.containerb {
    max-width: 1240px;
    width: 100%;
    min-height: 539px;
    height: auto;
    padding-top: 142px;
    color: rgb(173, 178, 177);
    text-align: left;
    display: flex;
    flex-wrap: wrap;
}

.title {
    display: flex;
    position: relative;
    max-width: 604px;
    width: 100%;
    color: white;
    font-weight: bold;
    font-size: 56px;
    line-height: 64px;
    letter-spacing: -2.5%;
    animation: animatetext 1s ease;
}

.line {
    position: absolute;
    left: -10px;
    top: 62px;
    width: 359px;
}

.desc {
    max-width: 438px;
    display: flex;
    width: 100%;
    animation: animatetext 1.5s ease;
}

.frame-one {
    display: flex;
    flex-direction: column;
    gap: 30px;
}

.btn-start {
    padding: 16px 32px;
    max-width: 195.5px;
    background-color: #2BB32A;
    border-radius: 64px;
    font-weight: 400;
    display: flex;
    gap: 15px;
    color: white;
    font-size: 16px;
    line-height: 24px;
    letter-spacing: 0%;
    cursor: pointer;
    border: 0;
    transition: 0.3s ease;
    animation: animatebtn 1s ease;
}

.btn-start:active {
    scale: 0.9;
}

.go {
    width: 22.5px;
    position: relative;
    top: 3px;
}

.active {
    display: flex;
    gap: 15px;
    animation: animateactive 1s ease;
}

.users {
    width: 120px;
}

.active-info {
    max-width: 177px;
    width: 100%;
    display: flex;
    flex-direction: column;
    font-weight: bold;
    font-size: 16px;
    line-height: 24px;
    letter-spacing: 0%;
    color: white;
}

.title-active {
    color: rgb(173, 178, 177);
    font-weight: 400;
    font-size: 12px;
    line-height: 16px;
    letter-spacing: 0%;
}

.frame-two {
    display: flex;
    margin-top: 80px;
    position: relative;
    left: 35px;
}

.card {
    width: 511.3px;
    height: 328.19px;
    border-radius: 32px;
    -webkit-box-shadow: 0px 0px 24px 8px black;
    -moz-box-shadow: 0px 0px 24px 8px black;
    box-shadow: 0px 0px 24px 8px black;
    position: relative;
    left: -10px;
    padding-left: 40px;
    padding-right: 40px;
    rotate: 15deg;
    border: 1px solid rgb(183, 192, 183);
    background: linear-gradient(to bottom right, rgba(255, 255, 255, 0.5), rgba(255, 255, 255, 0));
    backdrop-filter: blur(15px);
    -webkit-backdrop-filter: blur(15px);
    box-shadow: 0px 0px 0px 1px rgb(141, 155, 142);
    animation: animatecard 1s ease;
    transition: all 0.3s ease;
}

.card:hover {
    rotate: 0deg;
}

.card-info {
    position: relative;
    top: -30px;
    rotate: -15deg;
    display: flex;
    z-index: 2;
    flex-direction: column;
}

.title-num {
    font-weight: bold;
    font-size: 14px;
    rotate: 15deg;
    top: 90px;
    left: 0px;
    position: relative;
    line-height: normal;
    letter-spacing: 0%;
    color: #B9BEBD;

}

.card-num {
    position: relative;
    top: 110px;
    left: -15px;
    color: white;
    font-weight: bold;
    font-size: 32px;
    font-family: 'M PLUS 1 Code';
    line-height: 24px;
    letter-spacing: 0%;
    rotate: 15deg;
}

.cardlogo-one {
    width: 58.37px;
    position: relative;
    top: 10px;
    left: 20px;
}

.wifi {
    width: 25.32px;
    position: absolute;
    top: 130px;
    right: 10px;
}

.name-exp {
    rotate: 15deg;
    display: flex;
    position: relative;
    top: 160px;
    left: -30px;
    gap: 100px;
}

.name {
    display: flex;
    gap: 15px;
    flex-direction: column;
}

.exp {
    display: flex;
    gap: 15px;
    flex-direction: column;
}

.user-name {
    color: white;
    font-family: 'M PLUS 1';
    font-size: 12px;
    line-height: normal;
}

.date {
    color: white;
    font-family: 'M PLUS 1';
    font-size: 12px;
    line-height: normal;
}

.cardlogo-two {
    position: absolute;
    width: 58.43px;
    bottom: -240px;
    right: 50px;
}

.circle {
    width: 492px;
    height: 492px;
    border-radius: 100%;
    background-color: #2BB32A;
    position: absolute;
    z-index: -1;
    top: -60px;
    right: -150px;
    animation: animatecircle 1s ease;
}

@media (max-width:1220px) {
    .frame-one {
        margin-left: 50px;
    }

    .frame-two {
        scale: 0.8;
    }
}

@media(max-width:900px) {
    .containerb {
        justify-content: center;
    }

    .frame-two {
        display: none;

    }

    .frame-one {
        align-items: center;
        margin-left: 00px;
    }

    .title {
        text-align: center;
    }
    .desc {
        width: 90%;
    }
    .line {
        display: none;
    }
}
</style>