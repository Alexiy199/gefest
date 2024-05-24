<script>
const bodyStyles = window.getComputedStyle(document.body)

export default {
  methods: {
    reload() {
      location.reload()
    },
    toggleTheme() {
      const bgColor = bodyStyles.getPropertyValue('--bg-color')
      // const bgContent = bodyStyles.getPropertyValue('--bg-content')
      // const txtColor = bodyStyles.getPropertyValue('--txt-color')
      // const bgArticle = bodyStyles.getPropertyValue('--bg-article')

      if (bgColor === 'black') {
        document.body.style.setProperty('--bg-color', 'whitesmoke')
        document.body.style.setProperty('--bg-content', 'white')
        document.body.style.setProperty('--txt-color', 'black')
        document.body.style.setProperty('--bg-article', 'white')
      } else {
        document.body.style.setProperty('--bg-color', 'black')
        document.body.style.setProperty('--bg-content', 'hsl(0, 0%, 15%)')
        document.body.style.setProperty('--txt-color', 'white')
        document.body.style.setProperty('--bg-article', 'hsla(0, 10%, 10%, 0.7)')
      }
    }
  }
}
</script>

<template>
  <header>
    <button class="button header__btn" id="btn-theme" @click="toggleTheme()">&#127767;</button>
    <div class="box-logo" @click="reload()">
      <svg class="icon-svg">
        <use xlink:href="@/assets/sprite.svg#gefest-logo"></use>
      </svg>
      <span class="txt-logo">ГЕФЕСТ</span>
    </div>
    <a href="#contacts" class="link" id="link-contacts">контакты &#128381;</a>
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
  background-color: var(--bg-color);
  border-bottom: 1px solid hsla(170, 0%, 25%, 0.5);
  box-shadow: 0px 2px 4px 3px #00000050;
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
}
</style>
