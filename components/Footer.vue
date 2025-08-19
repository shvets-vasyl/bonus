<template>
	<footer class="footer">
            <div class="footer-container">
                <div class="footer-payments">
                   <img src="/images/icons.png" alt="">
                </div>
                <div class="footer-socials">
                    <a href="https://www.instagram.com/spartans/?igsh=MTE2dGZobmpwZGxqOA%3D%3D#" target="_blank">
                        <img src="/images/inst.svg" alt="" class="age">
                    </a>
                    <a href="https://t.me/SpartansBetOfficial" target="_blank">
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
		padding-bottom: 1vh;
		@include mobile {
			padding-bottom: 1vw;
		}
}

.footer-payments img {
	width: 55vh;
	@include mobile {
		width: 50vw;
	}
}


.footer-socials {
    justify-content: flex-end;
		display: flex;
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