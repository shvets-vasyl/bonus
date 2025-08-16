<template>
  <div class="game-block">
    <div class="slogan">
      <span>Крути барабан - </span><span>вигравай бонуси</span>
    </div>
    <img src="/images/game-bg.png" class="game-bg" alt="" />

    <div class="slots__wrap" @click="playGame">
      <video ref="slotVideo" preload="auto" playsinline muted src="/animation.mov" />
    </div>

    <div class="btn-start active start" @click="playGame">крутити</div>
    <img src="/images/steps.png" alt="" class="steps start" />
  </div>
</template>
<script setup lang="ts">
const slotVideo = ref<HTMLVideoElement | null>(null)
let audio: HTMLAudioElement

onMounted(() => {
  audio = new Audio("/mus.mp3")
  audio.preload = "auto"
  audio.loop = true

	const modal = document.querySelector(".modal-wrap.victory")

	slotVideo.value?.addEventListener("ended", () => {
    modal?.classList.add("show")
  })
})

const playGame = () => {
  slotVideo.value?.play()
  audio.play()
	audio.loop = true
}
</script>
<style scoped lang="scss">
.game-block {
  position: absolute;
  top: 54.5%;
  left: 50%;
  width: 99.16667vh;
  height: 62.77778vh;
  transform: translate(-49%, -62%);
  transition: all 0.3s;
  z-index: 2;
	@include mobile {
		width: 100vw;
		height: 64.8vw;
		position: relative;
		top: 45vw;
		left: 50%;
		transform: translate(-50%);
		font-size: 100vw;
	}
}
.slogan {
  top: -7vh;
  left: 50%;
  transform: translateX(-50%);
  font-family: var(--font-italic);
  text-transform: uppercase;
  white-space: nowrap;
  font-size: 5.55556vh;
  position: absolute;
  z-index: 2;
	@include mobile {
		display: flex;
		flex-direction: column;
		align-items: center;
		font-size: 8vw;
		top: -22vw;
		line-height: 1.2;
	}
}
.slogan span:nth-child(2) {
  color: #f2f740;
}
.game-block .game-bg {
  display: block;
  width: auto;
  height: 100%;
}
.steps {
  position: absolute;
  bottom: -19vh;
  left: 50%;
  transform: translateX(-50%);
  height: 16.66667vh;
  width: auto;
  cursor: pointer;
	@include mobile {
		height: 27.2vw;
		bottom: -35vw;
	}
}
.btn-start {
  background-image: url("/images/btn-start-bg.png");
  font-family: Fira, sans-serif;
  background-repeat: no-repeat;
  background-size: contain;
  color: #000;
  text-transform: uppercase;
  text-align: center;
	font-family: var(--font-italic);
  width: 42.5vh;
  height: 11.2963vh;
  font-size: 5.55556vh;
  line-height: 11.5vh;
  display: inline-block;
  cursor: pointer;
  position: absolute;
  left: 48%;
  top: 95%;
  transform: translate(-50%, -50%);
  z-index: 1;
  animation: pulse 2s linear infinite;
	@include mobile {
		width: 49.06667vw;
		height: 13.06667vw;
		font-size: 6.4vw;
		line-height: 14vw;
		top: 100%;
	}
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

.game-block .slots__wrap {
  position: absolute;
  left: 48.6%;
  transform: translateX(-50%);
  top: calc(241 / var(--desk-height) * 100vh);
  height: calc(386 / var(--desk-height) * 100vh);
  width: calc(760 / var(--desk-height) * 100vh);
  display: -ms-flexbox;
  display: flex;
  justify-content: space-between;
  cursor: pointer;
	@include mobile {
		top: calc(88 / var(--mob-width) * 1em);
		height: calc(135 / var(--mob-width) * 1em);
		width: calc(273 / var(--mob-width) * 1em);
		left: 49.7%;
	}
}
.game-block .slots__wrap video {
  width: 100%;
}
</style>
