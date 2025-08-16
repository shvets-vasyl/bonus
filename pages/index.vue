<template>
  <main class="main-page">
		<img class="inner-img" src="/images/bg.webp" alt="">

		<Header />
		<GameBlock />

		<img src="/images/left.svg" alt="" class="left "></img>
		<img src="/images/left.webp" class="bg-left desk" alt="">
		<img src="/images/right.webp" class="bg-right" alt="">
		<img src="/images/right.svg" alt="" class="right for-desk">

		<Modal />
		<Footer />

  </main>
</template>
<script setup lang="ts">

onMounted(() => {
	gsap.to(".main-page", {
		opacity: 1,
	})
})
</script>
<style scoped lang="scss">
.main-page {
	position: relative;
	opacity: 0;
	height: 100vh;
}
.bg-right {
    right: 0;
    bottom: 8vh;
    height: 19.16667vw;
}
.bg-left, .bg-right {
    display: block;
    position: absolute;
    width: auto;
    z-index: 3;
    pointer-events: none;
}
.bg-left {
    left: -4vh;
    bottom: 0;
    height: 22.8125vw;
}
.right {
    position: absolute;
    right: 0;
    bottom: 0;
    height: 7.8vh;
    width: auto;
    z-index: 2;
}
.left {
    position: absolute;
    left: 0;
    top: 0;
    height: 11.3vh;
    width: auto;
}
</style>
