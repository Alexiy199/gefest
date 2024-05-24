<template>
  <section id="contacts">
    <div class="wraper-content">
      <article>
        <h1 class="title">контакты</h1>
        <h2 class="sub-title">с нами можно связаться:</h2>
      </article>

      <br />
      <br />
      <span class="phone-num">+7-999-111-22-33</span>
      <br />
      <br />

      <span class="phone-num">+7-888-000-11-22</span>
      <br />
      <br />

      <a href="#" class="link">
        <svg class="icon-svg icon-contact">
          <use xlink:href="@/assets/sprite.svg#vk"></use>
        </svg>
      </a>
      <a href="#" class="link">
        <svg class="icon-svg icon-contact">
          <use xlink:href="@/assets/sprite.svg#telegram"></use>
        </svg>
      </a>
    </div>
  </section>
</template>

<script>
export default {
  methos: {
    read() {
      console.log('read')
    }
  }
}
</script>

<style scoped>
#contacts {
  & .wraper-content {
    align-content: center;
  }
  a:hover {
    background-color: rgba(0, 0, 0, 0);
  }
}
@media (hover: hover) {
  .icon-contact:hover {
    fill: #af0000;
  }
}

@media (hover: none) {
  .icon-contact:active {
    fill: #af0000;
  }
}
</style>
