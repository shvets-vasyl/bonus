<template>
<div class="modal-wrap victory">
        <div class="modal-b">
            <div class="modal__content" data-toggle="modal" data-target="#modalRegistration" data-dismiss="modal">
            <div class="modal-slogan">Щасливчик!<span>Забирай свій бонус</span></div>
                <div class="modal-bonus victiory">
                    <div class="modal-bonus-amount win">
                        50 000
                        <span class="modal-bonus-currency">грн</span>
                    </div>
                    <div class="modal-bonus-amount small">+100 FREESPINS</div>
                </div>
                <div class="btn-main">забрати</div>
            </div>
            <img src="/images/steps.png" alt="" class="steps-modal" data-toggle="modal" data-target="#modalRegistration" data-dismiss="modal">
        </div>
    </div>
</template>
<script setup lang='ts'>
</script>
<style scoped lang='scss'>
.modal-wrap {
	width: 100%;
	height: 100%;
	position: fixed;
	top: 0;
	left: 0;
	background: rgba(15, 0, 22, .85);
	-webkit-backdrop-filter: blur(10px);
	backdrop-filter: blur(10px);
	z-index: 1000;
	display: none;
}
.modal-wrap.show {
    display: inline-block;
}

.modal-b, .modal-b:after {
    position: absolute;
    left: 50%;
    top: 50%;
}

.modal-b {
    width: 109.25926vh;
    height: 53.14815vh;
    transform: translate(-50%, -68%);
}

.modal-slogan, .modal__content {
    position: relative;
    display: -ms-flexbox;
    display: flex
;
    -ms-flex-direction: column;
    flex-direction: column;
    -ms-flex-align: center;
    align-items: center;
}

.modal__content {
    width: 100%;
    height: 100%;
    cursor: pointer;
}

.steps-modal {
    position: absolute;
    bottom: -28vh;
    left: 50%;
    transform: translateX(-50%);
    height: 16.66667vh;
    width: auto;
    cursor: pointer;
}
.modal-b, .modal-b:after {
    position: absolute;
    left: 50%;
    top: 50%;
}
.modal-b:after {
    content: "";
    background: url(images/modal-bg.webp) no-repeat 50% / cover;
    width: 100%;
    height: 100%;
    transform: translate(-50%, -50%);
    z-index: -1;
}
.modal-slogan, .modal__content {
    position: relative;
    display: -ms-flexbox;
    display: flex
;
    -ms-flex-direction: column;
    flex-direction: column;
    -ms-flex-align: center;
    align-items: center;
}
.modal-slogan {
    color: #fff;
    text-align: center;
    font-family: Fira, sans-serif;
    font-size: 7.40741vh;
		font-family: var(--font-italic);
    line-height: 1;
    z-index: 1;
    text-transform: uppercase;
    margin: 8vh 0 2vh;
}

.btn-main {
    background-image: url("/images/btn-start-bg.png");
    font-family: Fira, sans-serif;
    background-repeat: no-repeat;
    background-size: contain;
    font-family: var(--font-italic);
    color: #000;
    text-transform: uppercase;
    text-align: center;
    width: 42.5vh;
    height: 11.2963vh;
    font-size: 5.55556vh;
    line-height: 11.5vh;
    display: inline-block;
    cursor: pointer;
    position: absolute;
    left: 50%;
    top: 107%;
    transform: translate(-50%, -50%);
    z-index: 1;
    animation: pulse 2s linear infinite;
}

@keyframes pulse {
  0% {
    transform: translate(-50%, -50%) scale(0.95);
  }

  50% {
    transform: translate(-50%, -50%) scale(1);
  }
  100% {
    transform: translate(-50%, -50%) scale(0.95);
  }
}
.modal-slogan span {
    font-size: 3.7037vh;
    color: #f2ff00;
}


.modal-bonus .modal-bonus-amount {
    display: -ms-flexbox;
    display: flex
;
    -ms-flex-direction: column;
    flex-direction: column;
    -ms-flex-align: center;
    align-items: center;
    color: #fff;
    font-size: 20.37037vh;
    font-family: var(--font-italic);
    line-height: 1;
    text-align: center;
    text-transform: uppercase;
    line-height: 76%;
}
.modal-bonus .modal-bonus-amount {
    display: flex
;
    -ms-flex-direction: column;
    flex-direction: column;
    -ms-flex-align: center;
    align-items: center;
    color: #fff;
    font-size: 20.37037vh;
    font-family: var(--font-italic);
    line-height: 1;
    text-align: center;
    text-transform: uppercase;
    line-height: 76%;
}

.modal-bonus .modal-bonus-amount.win {
    -ms-flex-direction: row;
    flex-direction: row;
    -ms-flex-align: end;
    align-items: flex-end;
    margin-bottom: 1vh;
}

.modal-bonus .modal-bonus-amount.small {
    font-size: 7.40741vh;
    color: #f2ff00;
}
.modal-bonus .modal-bonus-currency {
    font-size: 3.7037vh;
    display: inline-block;
    letter-spacing: 0;
    line-height: 100%;
}
</style>