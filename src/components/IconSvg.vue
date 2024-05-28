<script setup>
const props = defineProps(['icon'])

const { icon } = props

const path = () => {
    return `./sprite.svg#${icon}`
}
</script>

<template>
    <svg class="icon-svg">
        <use :xlink:href="path()"></use>
    </svg>
</template>
