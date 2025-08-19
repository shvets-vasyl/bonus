<template>
  <header class="header">
    <div class="o-container">
      <div class="header-left">
        <div
          data-id="logo"
          class="logo pm-external-reg-btn-header"
          data-toggle="modal"
          data-target="#modalRegistration"
          data-dismiss="modal"
        >
          <img
            src="/logo.webp"
            alt="Ставки на спорт ᐉ Онлайн Парі на Гроші в Україні Parik24"
          />
        </div>
      </div>
      <div class="header-right"></div>
    </div>
  </header>
</template>
<script setup lang="ts"></script>
<style scoped lang="scss">
.header {
  padding: 2vh 0 0;
  position: absolute;
  z-index: 5;
  width: 100%;

	@include mobile {
		padding-top: 3.46667vw;
	}
}
.header .o-container,
.logo {
  display: -ms-flexbox;
  display: flex;
  position: relative;
}
.header .o-container {
  align-items: flex-start;
  justify-content: space-between;
  z-index: 2;
}
.header .o-container {
  padding-left: 3.7037vh;
	@include mobile {
		padding: 0;
		padding-right: 5vw;
	}
}
.header-left,
.header-right {
  display: flex;
  align-items: center;
}
.header-left {
  justify-content: flex-start;
}
.logo {
  cursor: pointer;
}
.logo img {
  width: auto;
  height: 5vh;
  display: block;
  image-rendering: -webkit-optimize-contrast;
	@include mobile {
		height: 7.46667vw;
		margin-left: 5.33333vw;
	}
}
</style>
