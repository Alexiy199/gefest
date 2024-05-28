<script setup>
import IconSvg from './IconSvg.vue'
</script>

<template>
    <section id="contacts">
        <div class="wraper-content">
            <article>
                <h1 class="title">контакты</h1>
                <h2 class="sub-title">с нами можно связаться:</h2>
            </article>

            <br />
            <br />
            <address class="phone-num">+7-938-401-11-46</address>
            <br />
            <br />

            <a href="#" class="link">
                <IconSvg icon="vk" />
            </a>
            <a href="https://t.me/akkuratnei" class="link">
                <IconSvg icon="telegram" />
            </a>
        </div>
    </section>
</template>

<style scoped>
#contacts {
    & .wraper-content {
        padding: 1em;
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
