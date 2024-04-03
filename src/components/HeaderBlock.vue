<script>
export default {
  methods: {
    reload() {
      location.reload()
    }
  }
}
</script>

<template>
  <header>
    <button class="button header__btn" id="btn-thene">&#128294;</button>
    <div class="box-logo" @click="reload()">
      <svg class="icon-svg">
        <use xlink:href="@/assets/sprite.svg#gefest-logo"></use>
      </svg>
      <span class="txt-logo">ГЕФЕСТ</span>
    </div>
    <a href="#contacts" class="link" id="link-contacts">написать</a>
    <a href="#phone" class="link" id="link-phone">&#128381;</a>
  </header>
</template>

<style>
header {
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1em;
  width: 100vw;
  height: 4em;
  background-color: hsl(0, 0%, 15%);
  border-bottom: 1px solid hsl(170, 0%, 25%);
}

@media (max-width: 426px) {
  header {
    gap: 0.3em;
  }
}

.box-logo {
  display: flex;
  align-items: center;
  gap: 10px;
  width: fit-content;
  height: fit-content;
  overflow: hidden;
  background-color: #af0000;
  padding: 5px;
  margin: auto 10px;
  cursor: pointer;
}

.txt-logo {
  font-size: 1em;
  font-weight: 700;
  letter-spacing: 4px;
  color: white;
}

.header__btn {
  width: 1.5em;
  height: 1.5em;
  padding: 2px;
  font-weight: 700;
  font-size: 2em;
  background-color: rgba(0, 0, 0, 0);
  color: #fff;
}
</style>
