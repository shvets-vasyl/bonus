<template>
	<footer class="footer">
            <div class="footer-container">
                <div class="footer-payments">
                    <img src="/images/visa.png" class="visa" alt="">
                    <img src="/images/mastercard.png" class="mastercard" alt="">
                    <img src="/images/crypto-icon-1.svg" class="crypto-icon crypto-icon-1" alt="">
                    <img src="/images/crypto-icon-2.svg" class="crypto-icon crypto-icon-2" alt="">
                    <img src="/images/crypto-icon-3.svg" class="crypto-icon crypto-icon-3" alt="">
                    <img src="/images/crypto-icon-4.svg" class="crypto-icon crypto-icon-4" alt="">
                    <img src="/images/crypto-icon-5.svg" class="crypto-icon crypto-icon-5" alt="">

                </div>
                <div class="footer-socials">
                    <a href="https://www.instagram.com/parik24_official/" target="_blank">
                        <img src="/images/inst.svg" alt="" class="age">
                    </a>
                    <a href="https://t.me/+W06frZ2VCFw4YzRi" target="_blank">
                        <img src="/images/telegram.svg" alt="" class="age">
                    </a>
                    <img src="/images/social-icon-1.png" alt="" class="age">
                </div>
            </div>
        </footer>
</template>
<script setup lang='ts'>
</script>
<style scoped lang='scss'>
.footer {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100vw;
    z-index: 999;
    height: 5.5vh;
    padding: 0 3.7vh;
    display: flex;
    align-items: center;
		@include mobile {
			padding: 0 7.2vw;
			height: 10.6vw;
			justify-content: center;
		}
}
.footer-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex: 1 0 auto;
}
.footer-payments {
    justify-content: flex-start;
		position: relative;
}
.footer-payments, .footer-apps, .footer-socials {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex
;
    align-items: center;
    flex: 1 1 33.33%;
}

.footer-payments .visa {
    height: 1.4vh;
		@include mobile {
			height: 3.8vw;
		}
}
.footer-payments img {
    margin-right: 3.7vh;
		@include mobile {
			margin-right: 5.3vw;
		}
}
.footer-payments .mastercard {
    height: 2.2vh;
		@include mobile {
			height: 5.2vw;
		}
}
.footer-payments .crypto-icon {
    height: 2.22vh;
		@include mobile {
			height: 5.3vw;
		}
}
.footer-payments .crypto-icon-4, .footer-payments .crypto-icon-5, .footer-payments .crypto-icon-2 {
	@include mobile {
		display: none;
	}
}
.footer-socials {
    justify-content: flex-end;
}

.footer-payments, .footer-apps, .footer-socials {
    display: flex;
    align-items: center;
    flex: 1 1 33.33%;
}
.footer-socials a {
    margin-right: 2.7vh;
		@include mobile {
			margin-right: 5vw !important;
		}
}
.age {
    height: 2.5vh;
    vertical-align: middle;
		@include mobile {
			height: 5.3vw;
		}
}


</style>